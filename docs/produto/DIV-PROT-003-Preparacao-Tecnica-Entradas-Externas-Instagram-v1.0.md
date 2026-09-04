<!--
NOTA DE STATUS DESTE DOCUMENTO
Este arquivo NÃO é um Artefato Derivado da Biblioteca Arquitetural — é um
documento de preparação técnica redigido diretamente neste repositório, a
pedido explícito da responsável pelo produto, como próxima ação mínima
recomendada pelo item 23 de DIV-PROT-002.

Duas seções deste documento (7 e 9) registram regras arquiteturais NOVAS
— a separação física entre `eventos_experiencia` e `eventos_aquisicao`, e
o mecanismo de sessão anônima ligado à pendência MA-004 — que ainda não
foram localizadas nem ratificadas na Biblioteca Arquitetural a partir
deste repositório. Elas estão registradas aqui como especificação de
trabalho, não como patrimônio institucional consolidado. Ver seção 14.
-->

# DIV-PROT-003

# Preparação Técnica do Protótipo para Entradas Externas via Instagram

| Campo | Valor |
|---|---|
| Versão | v1.0 |
| Data | 04/09/2026 |
| Status | Especificação de preparação; implementação pendente de stack técnica confirmada |
| Natureza | Especificação técnica (URLs, sessão, persistência de origem, instrumentação) |
| Domínio | 03 · Produto |
| Documento relacionado | `DIV-PROT-002-Estudo-Boas-Vindas-Instagram-ManyChat-v1.0.md` |
| Documento relacionado | `Nota-Arquitetural-Registro-de-Entrada.md` |
| Origem desta preparação | Instrução direta da responsável pelo produto, registrada em sessão de trabalho de 04/09/2026 |

---

## 1. Objetivo

Formalizar, em nível de especificação (sem código), a preparação necessária
para que o protótipo Divícia receba entradas externas vindas do Instagram —
via Direct/ManyChat e via link da bio — preservando origem, permitindo
retomada de onboarding e mantendo separação estrita entre telemetria de
aquisição e a matriz de eventos de experiência.

Este documento **não decide stack técnica**. Ele especifica o que a
implementação precisa fazer, para que Engenharia possa executá-la quando a
stack estiver confirmada (ver lacuna registrada em DIV-PROT-002 §18.4 e
nota de status acima).

---

## 2. Contexto

A Divícia terá duas formas iniciais de entrada no app a partir do Instagram:

1. link enviado por mensagem direta, conduzido pelo ManyChat;
2. link disponibilizado na bio do perfil da Divícia.

Arquitetura já registrada em DIV-PROT-002 §6.1:

```text
Instagram → ManyChat → URL pública identificada → App Divícia
```

**O ManyChat não é incorporado ao app.** Não deve ser instalado como SDK,
biblioteca ou componente interno. Nesta fase, o ManyChat é apenas a
ferramenta externa responsável por receber o evento no Instagram, conduzir a
conversa inicial e enviar uma URL pública identificada para o app. O fluxo de
conversa no ManyChat (mensagens, botões, janela de 24h) está fora do escopo
de implementação no app e está documentado em DIV-PROT-002 §6.3 e §8 — citado
aqui apenas para justificar por que a origem precisa ser preservada com
precisão desde o primeiro clique.

**Aviso operacional, fora do escopo técnico:** confirmar diretamente no
painel do ManyChat se o gatilho *Follow to DM* já está liberado para a conta
da Divícia — a Meta trata esse gatilho como beta por conta, e a
disponibilidade pode variar (já registrado como lacuna em DIV-PROT-002 §18.3).
Não assumir que está ativo sem checar.

---

## 3. Escopo desta preparação

1. Garantir uma URL pública e estável para entrada no app.
2. Permitir que essa URL receba e preserve parâmetros UTM, especialmente:
   `utm_source`, `utm_medium`, `utm_campaign`, `utm_content`.
3. Preparar dois endereços identificáveis (já definidos em DIV-PROT-002
   §10.1–§10.2):
   - Entrada pelo Direct/ManyChat: `?utm_source=instagram&utm_medium=dm&utm_campaign=boas_vindas`
   - Entrada pela bio: `?utm_source=instagram&utm_medium=bio&utm_campaign=perfil_divicia`
4. Preservar a origem da entrada durante todo o onboarding, mesmo que a
   mulher navegue por várias telas antes de se identificar ou concluir o
   cadastro.
5. Aplicar a lógica de estado já registrada em DIV-PROT-002 §6.4:
   - visitante nova → iniciar na T01, Apresentação;
   - onboarding (Registro de Entrada) iniciado → retomar do ponto em que
     parou;
   - mulher já autenticada (Conta) → encaminhar para a Home;
   - mulher já vinculada (possui Conta), mas não autenticada → manter
     disponível a opção **Já faço parte da Divícia**.
6. Preparar pontos de instrumentação para os sete eventos de aquisição
   listados na seção 10.
7. Não registrar, em telemetria de aquisição, ManyChat ou qualquer
   ferramenta externa: respostas reflexivas, conteúdo escrito pela mulher,
   escolhas íntimas, interpretações da Lumi, ou qualquer dado sensível da
   experiência (regra já registrada em DIV-PROT-002 §11.4).

---

## 4. Fora do escopo nesta fase

- integração por API com o ManyChat;
- instalação de SDK do ManyChat;
- envio de dados pessoais do app para o ManyChat;
- integração com CRM;
- automações posteriores de relacionamento;
- desenvolvimento de landing page intermediária;
- escolha ou confirmação de stack técnica (framework, hospedagem, banco de
  dados) — ver nota de status no topo deste documento;
- ratificação das regras arquiteturais novas descritas nas seções 7 e 9 —
  ver seção 14.

---

## 5. Preservação de origem durante o onboarding

A origem de entrada (`instagram_dm`, `instagram_bio`, `acesso_direto`, e
origens futuras) precisa sobreviver à navegação entre telas do onboarding,
mesmo antes de qualquer identificação. O mecanismo que torna isso possível é
a sessão anônima descrita na seção 7 — sem ela, não há onde anexar a origem
entre o primeiro clique e a identificação da mulher.

Regra de não sobrescrita (já registrada em DIV-PROT-002 §10.3): não
sobrescrever a primeira origem registrada sem uma regra analítica explícita.
`first_touch` e `last_touch`, se necessários, são uma decisão de arquitetura
analítica ainda em aberto (DIV-PROT-002 §18.6) — este documento assume
`first_touch` como comportamento padrão até decisão em contrário.

---

## 6. Lógica de estado no app

Tabela já registrada em DIV-PROT-002 §6.4, repetida aqui como requisito de
implementação:

| Estado reconhecido | Comportamento esperado |
|---|---|
| Visitante nova | Iniciar na T01, Apresentação da Divícia |
| Registro de Entrada em andamento | Retomar o ponto em que parou |
| Mulher com Conta, autenticada | Encaminhar para a Home |
| Mulher com Conta, não autenticada | Oferecer **Já faço parte da Divícia** |

O mecanismo de "Já tenho uma conta" já existe como botão na Etapa 01 do
Blueprint (`DIV-PROT-001`), mas está marcado como **ainda não implementado**.
A atualização de microcopy para **Já faço parte da Divícia** está registrada
em DIV-PROT-002 §7.3 como pendente de aplicação controlada ao Blueprint —
este documento não a aplica.

---

## 7. Sessão anônima e mecanismo de retomada

> Conteúdo desta seção é regra arquitetural nova. Ver nota de status no
> topo do documento.

- Uma sessão anônima é criada **desde o primeiro clique** no link, antes de
  qualquer identificação ou cadastro.
- A origem (UTM completa) é anexada a essa sessão no momento da criação, e
  não depois.
- Essa sessão anônima é o mecanismo que permite retomar o onboarding entre
  telas (seção 6) e é o identificador de sessão referenciado nos eventos de
  aquisição (seção 10).
- Quando a mulher se identifica (submissão da Etapa 02, conforme
  `Nota-Arquitetural-Registro-de-Entrada.md`), a sessão anônima **converte**
  para Registro de Entrada / Conta — mesmo identificador interno, sem
  duplicar registro, sem tocar na matriz `eventos_experiencia`.

### 7.1 Relação com MA-004

A pendência **MA-004** (resolução de identidade entre sessões) foi citada
como referência para este mecanismo. Ela **não foi localizada em nenhum
documento deste repositório** — provavelmente existe apenas na Biblioteca
Arquitetural externa. Antes de implementar, confirmar na Biblioteca:

- o conteúdo exato de MA-004;
- se o mecanismo de sessão anônima aqui descrito é compatível com o que
  MA-004 já resolve ou pretende resolver;
- para evitar desenhar dois sistemas de sessão paralelos e não comunicantes,
  a sessão anônima de aquisição e a resolução de identidade de MA-004 devem
  ser o mesmo mecanismo, não dois mecanismos coexistentes.

### 7.2 Webview do Instagram — ponto de atenção técnico

O Instagram normalmente abre links dentro de um navegador embutido
(webview), com armazenamento isolado do navegador padrão do celular. Se a
mulher sair do Instagram e depois abrir o app fora do webview (Safari/Chrome
direto), a sessão pode não persistir.

**Implicação de implementação:** um mecanismo de sessão baseado
exclusivamente em armazenamento local do navegador (cookie/localStorage)
pode não ser suficiente para este caso, dado o isolamento do webview do
Instagram. Recomenda-se investigar mecanismos que sobrevivam à troca de
navegador (ex.: token na URL) — a decisão final de implementação pertence
à Mesa/engenharia quando a stack for definida. Este comportamento deve ser
testado explicitamente antes de qualquer publicação (ver seção 12).

---

## 8. URLs e parâmetros

Já definidos em DIV-PROT-002 §10.1–§10.2 (domínio ainda a confirmar):

```text
https://app.divicia.com.br/?utm_source=instagram&utm_medium=dm&utm_campaign=boas_vindas&utm_content=follow_to_dm
https://app.divicia.com.br/?utm_source=instagram&utm_medium=bio&utm_campaign=perfil_divicia
```

Regras (DIV-PROT-002 §10.3): letras minúsculas; nenhum dado pessoal nos
parâmetros; nomenclatura estável; origem preservada durante o onboarding
(seção 5); nenhuma sobrescrita silenciosa da origem original.

---

## 9. Separação obrigatória: telemetria de aquisição ≠ matriz de eventos de experiência

> Conteúdo desta seção é regra arquitetural nova, análoga à já aplicada a
> `travessia_iniciada` (removido da matriz de eventos por ser telemetria de
> navegação, sem relevância para experiência, memória ou inteligência). Esse
> precedente **não foi localizado neste repositório** — provavelmente vive
> apenas na Biblioteca Arquitetural. Ver nota de status no topo do
> documento.

**Duas estruturas fisicamente separadas — nunca a mesma tabela com um campo
"tipo":**

- **`eventos_experiencia`** (já existente na arquitetura institucional):
  eventos como `voz_revelada`, `travessia_parcial`, `travessia_concluida` e
  demais eventos já fixados na matriz institucional. Alimenta memória, Mapa
  de Reflexão, interpretação da Lumi. Regra de entrada: só o que tem
  relevância para experiência, memória ou inteligência.
- **`eventos_aquisicao`** (nova, objeto desta preparação): os sete eventos
  da seção 10. Puramente analítica — a Lumi nunca lê esta estrutura
  diretamente, e ela nunca vira memória da mulher.

**Ponte entre as duas, sem misturar:** a origem de aquisição pode ficar
disponível como atributo de contexto no perfil da mulher (categoria
"Permanente" da arquitetura de contexto) — nunca como evento replicado na
matriz de experiência. Se a Lumi precisar saber que a mulher veio do
Instagram, isso é lido do perfil, não da estrutura de aquisição.

---

## 10. Eventos de aquisição

Lista mínima (já registrada em DIV-PROT-002 §11.2, repetida aqui como
especificação de estrutura de dados):

| Evento | Finalidade |
|---|---|
| `entrada_no_app` | Registrar abertura da porta de entrada |
| `apresentacao_iniciada` | Confirmar início da T01 |
| `identificacao_concluida` | Medir avanço no Primeiro Encontro |
| `escolha_do_caminho_concluida` | Medir conclusão da escolha disponível |
| `trilha_iniciada` | Registrar ativação da Trilha |
| `primeira_experiencia_iniciada` | Registrar ativação comportamental |
| `primeira_experiencia_concluida` | Registrar conclusão da primeira experiência |

Cada evento, quando disponível, carrega a origem da entrada: `instagram_dm`,
`instagram_bio`, `acesso_direto`, outras origens futuras.

### 10.1 Campos sugeridos de `eventos_aquisicao`

- `evento` — enum dos sete listados acima;
- `origem` — `instagram_dm` / `instagram_bio` / `acesso_direto` / futuras;
- `utm_source`, `utm_medium`, `utm_campaign`, `utm_content`;
- `sessao_id` — referência à sessão anônima descrita na seção 7;
- `timestamp`.

Este é um conjunto sugerido de campos, não um schema fechado — a definição
final de tipos e constraints é decisão de implementação de Engenharia.

### 10.2 Propriedades proibidas

Já registrado em DIV-PROT-002 §11.4 — repetido aqui como restrição de
implementação, aplicável tanto a `eventos_aquisicao` quanto a qualquer
ferramenta externa (ManyChat incluído):

- texto escrito pela mulher;
- resposta reflexiva;
- escolha íntima em campo aberto;
- interpretação da Lumi;
- conteúdo do Diário dos Saberes;
- conteúdo de Ritual, Voz, Reflexão ou Exploração associado nominalmente;
- informação sensível usada para segmentação no Instagram ou no ManyChat.

---

## 11. Fora do escopo, reafirmado

Ver seção 4. Nenhuma integração adicional (API do ManyChat, CRM, webhook,
SDK) deve ser executada sem validação prévia.

---

## 12. Critérios de validação

- [ ] o link do Direct abre corretamente o app;
- [ ] o link da bio abre corretamente o app;
- [ ] ambos iniciam a experiência visual adequada (T01);
- [ ] a origem de cada acesso permanece identificável, com o registro caindo
      exclusivamente em `eventos_aquisicao`, nunca em `eventos_experiencia`;
- [ ] a mulher autenticada não precisa repetir o onboarding;
- [ ] a mulher que interrompeu o percurso pode retomá-lo, **inclusive saindo
      do webview do Instagram e reabrindo o link fora dele** (ver seção
      7.2 — testar esse caminho explicitamente, não presumir que funciona);
- [ ] nenhuma resposta reflexiva é enviada para ferramentas externas.

Não executar integrações adicionais sem validação prévia.

---

## 13. Responsabilidades

| Frente | Responsabilidade |
|---|---|
| Produto | Preservar coerência do percurso e critérios de sucesso |
| Desenvolvimento | Stack técnica, URL pública, roteamento, sessão anônima, persistência e eventos |
| Privacidade/Jurídico | Confirmar que `eventos_aquisicao` e a sessão anônima não capturam dado pessoal além do necessário |

Herdado de DIV-PROT-002 §15 para as frentes de Marketing, Conteúdo/Marca e
Atendimento, não repetido aqui por não terem responsabilidade técnica nesta
preparação.

---

## 14. Pendências que dependem da Biblioteca Arquitetural

Este documento registra, mas **não ratifica**, as seguintes decisões — elas
devem ser confirmadas ou formalizadas na Biblioteca Arquitetural antes da
implementação, conforme regra permanente deste repositório
(`FONTES-ARQUITETURAIS.md`: *"Se não existir nenhum dos quatro [Documento
Fundador, Especificação, Blueprint, Artefato Derivado oficial], interrompa a
implementação"*):

1. Conteúdo e status atual da pendência **MA-004**, e confirmação de que o
   mecanismo de sessão anônima da seção 7 é o mesmo mecanismo que MA-004
   resolve — não dois sistemas paralelos.
2. Ratificação institucional da separação física
   `eventos_experiencia` / `eventos_aquisicao`, incluindo o precedente de
   remoção de `travessia_iniciada` citado como analogia — este documento não
   encontrou esse precedente registrado neste repositório.
3. Confirmação da stack técnica do MVP (framework, hospedagem, banco de
   dados) — atualmente indefinida (DIV-PROT-001 trata a ferramenta de
   prototipagem em uso como sem backend, autenticação ou banco de dados).
4. Domínio público final e ferramenta de analytics — já registrados como
   lacunas em DIV-PROT-002 §18.4–§18.5.

Nenhuma dessas pendências deve ser preenchida por suposição.

---

## 15. Referências

- `DIV-PROT-002-Estudo-Boas-Vindas-Instagram-ManyChat-v1.0.md` — tese de
  produto, URLs, microcopy, lógica de estado, eventos mínimos.
- `Nota-Arquitetural-Registro-de-Entrada.md` — mecanismo de promoção de
  Registro de Entrada para Conta.
- `DIV-PROT-001-Blueprint-Materializacao-MVP-Trilha-Despertar.md` — estado
  atual do botão "Já tenho uma conta" (não implementado) e limites da
  ferramenta de prototipagem em uso.
- `FONTES-ARQUITETURAIS.md` — regra de autoridade e verificação antes de
  implementar.
