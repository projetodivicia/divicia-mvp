# DIV-PROT-001

# Blueprint de Materialização do MVP — Trilha Despertar

| Campo | Valor |
|---|---|
| Status | Completo para o escopo Trilha Despertar, sem Lumi e sem Memória — as 12 etapas do Primeiro Encontro à Reflexão Guiada estão definidas, com conteúdo, regras e fontes reais. Uma pendência técnica real permanece em aberto (ver lista consolidada ao final), a cargo da Engenharia. |
| Natureza | Especificação de Materialização (camada de Construção — não é Documento Fundador, não gera ADR) |
| Domínio | 03 · Produto |
| Local na Biblioteca | `03-produto/prototipo/trilha-do-despertar/` |
| Origem da estrutura | DIV-MA-009 (Primeiro Encontro), DIV-MA-010 (Pesquisa de Chegada) — Fluxo Arquitetural oficial |
| Método de construção | Preenchimento dos 8 blocos por etapa, puxando conteúdo já decidido em outros documentos, para que o briefing chegue coeso à ferramenta de materialização |

---

## Objetivo

Este documento descreve, de forma sequencial, toda a experiência da mulher
na Trilha Despertar. Seu propósito é permitir que qualquer ferramenta de
materialização consiga construir o MVP preservando a arquitetura, a
experiência da mulher, a identidade visual, os princípios de UX, as regras
de produto e as regras técnicas já decididas.

Este documento segue prioritariamente os conceitos publicados em Mesas
Arquiteturais e Notas Arquiteturais. Quando aborda temas ainda não
institucionalizados, apresenta propostas de materialização destinadas à
validação durante o MVP — é o caso, por exemplo, do Registro de Entrada,
formalizado em Nota Arquitetural própria.

**Nesta revisão:** os ingredientes já existiam espalhados por DIV-MA-009,
DIV-MA-010, DIV-PROT-JURIDICO-001/002 e DIV-PROT-CONFORMIDADE-JURIDICA-001. Esta versão monta o
prato — cada etapa passa a ter seus 8 blocos preenchidos com o que já foi
decidido, em vez de fragmentos remetendo a documentos diferentes.

---

## Como ler este documento

Cada etapa é descrita sob a mesma estrutura de 8 blocos: Objetivo,
Experiência da Mulher, Objetivo de Produto, Orientações de UX, Direção de
Criação, Conteúdo, Regras Arquiteturais, Implementação.

**Disciplina do bloco 7 (Regras Arquiteturais):** cita decisões já
publicadas — nunca decide. Pergunta sem resposta vira pendência
registrada, nunca decisão inventada ali.

---

## Princípios Gerais de Materialização

**Com respaldo já publicado em Mesa:**

- A plataforma nunca julga, nunca diagnostica, nunca interpreta emoção ou
  intenção da mulher. *(Bloco A §6, Home; Princípio Fundador, DIV-MA-010)*
- Nenhuma pergunta existe por curiosidade da plataforma — toda pergunta
  contribui para uma experiência mais legítima. *(Princípio Fundador,
  DIV-MA-010)*
- A plataforma nunca comunica encerramento de experiência, nunca mede
  ausência, nunca cobra retorno. *(Bloco A §6 e §11, Home)*
- A plataforma sempre oferece continuidade. *(DIV-MA-014)*
- O silêncio é elemento legítimo de design. *(C.6/E.3, Home)*
- A identidade visual segue o sistema publicado em `07-identidade-visual/`.
- A mulher compreende primeiro quem é a Divícia, antes da Divícia procurar
  compreender o momento dela. *(Tese Arquitetural, DIV-MA-009)*
- Nomes técnicos de Trilha (Despertar/Descoberta/Integração) não
  aparecem antes da Etapa 06 — a mulher só os vê quando já está diante
  da escolha em si, nunca durante a Apresentação (Etapa 01). *(Princípio
  Narrativo, DIV-MA-009; ajuste de alcance nesta revisão — ver Etapa 06)*
- Vocabulário arquitetural ≠ vocabulário de interface: um mesmo conceito
  pode ter nome técnico diferente do nome mostrado à mulher, sem que isso
  seja inconsistência. *(Princípio da Dupla Camada de Linguagem,
  DIV-MA-009)*
- Rejeitado explicitamente, com base em benchmark de mercado: testes com
  nota/score diagnóstico; narrativa de personagem manipuladora vinculada a
  paywall. *(DIV-MA-009 §2)*
- Nenhum dado pessoal deve ser coletado antes de aviso mínimo de
  privacidade. *(DIV-PROT-CONFORMIDADE-JURIDICA-001 §2; ver pendência crítica, Etapa 01.5,
  abaixo)*
- O estado de ativação de cada módulo (Lumi, Diário, Memória, IA,
  Pagamentos, Assinaturas, Books, Ritual, Explorações) é definido
  exclusivamente em DIV-PROT-MODULOS-001. Nenhuma etapa deste Blueprint deve
  restatar esse estado. *(DIV-PROT-MODULOS-001)*
- **Princípio da Conta da Mulher e do Registro de Entrada:** o Registro de Entrada nasce na Etapa 02 e armazena
  identificação, respostas e Trilha escolhida até ser **promovido** a
  Conta, quando a titularidade do e-mail é confirmada (checkpoint na
  Escolha da Trilha, ver Etapa 06). A Conta é a identidade persistente
  da mulher na plataforma — não é experiência, não é memória, não é
  Instância. Toda Instância de Experiência sempre pertence a uma Conta.
  Autenticação é apenas o mecanismo que comprova titularidade — o
  mecanismo específico (e-mail, login social, passkey ou outro) é
  decisão de Engenharia, não de Arquitetura. *(ver Etapa 02, bloco 4-7;
  Nota Arquitetural — Registro de Entrada)*

---

## Roteiro das Etapas (estrutura oficial, DIV-MA-010)

| # | Nome | Status | Fonte |
|---|---|---|---|
| 01 | Apresentação da Divícia | ✅ Completa (conteúdo, sem cortes) | DIV-MA-009 Cap. 1–3, 6 |
| — | **Aviso de Privacidade (Etapa 01.5)** | ✅ Completa (3 checkboxes definidos, revisada colaborativamente) | DIV-PROT-CONFORMIDADE-JURIDICA-001 §2, §9; DIV-PROT-JURIDICO-001 §4 |
| 02 | Identificação | ✅ Completa; já existe em protótipo anterior, requer atualização (campo de e-mail + Cadastro Técnico) | DIV-MA-010 Etapa 1; protótipo anterior existente |
| 03 | Boas-vindas | ✅ Completa; já existe em protótipo anterior | DIV-MA-010 Etapa 2; protótipo anterior existente |
| 04 | Pesquisa de Chegada | ✅ Completa; já existe em protótipo anterior | DIV-MA-010 Etapa 3; protótipo anterior existente |
| 05 | Voz Movimento | ✅ Completa; já existe em protótipo anterior | DIV-MA-010 Etapa 4; protótipo anterior existente |
| 06 | Escolha do Caminho (3 Trilhas, fusão com antiga Etapa 07) | ✅ Completa (conteúdo); ⚠️ protótipo requer atualização (descrição completa nos cards) | DIV-MA-010 Etapas 5 e 6; conteúdo fundido nesta revisão |
| — | **Confirmação de Titularidade (Etapa 06.5)** | ✅ Completa (conceito, fluxo e mecanismo: código por e-mail); ⚠️ parâmetros operacionais pendentes de Engenharia | Blueprint |
| 08 | Boas-vindas da Trilha (Despertar) | ✅ Completa (conteúdo) | DIV-MA-010 Etapa 8; conteúdo fornecido jul/2026 |
| — | ~~Cadastro (técnico)~~ | ✅ Resolvido — integrado à Etapa 02 (Identificação e Cadastro Técnico); não é mais etapa separada | Ver Etapa 02 |
| — | Confirmação de Acesso / Pagamento | Fora de escopo — "exclusivo Descoberta/Integração"; não ativo nesta fase | DIV-MA-010 Etapa 7; DIV-PROT-MODULOS-001 |
| — | Mapa de Reflexão (3 Movimentos) | Fora de escopo — "exclusivo Trilha Integração"; possível redundância com DIV-MA-008, a resolver depois | DIV-MA-010 Etapa 9 |
| **09** | **Home** | ⚠️ Regras completas (DIV-MA-013); texto literal completo nas 6 seções; sem protótipo | Blocos A–E (DIV-MA-013); Registro Rápido de Conteúdo; `Explore-Algo-Novo-Convites-Reflexoes-Guiadas.json` |
| **10** | **Iniciar a Travessia** | ✅ Completa — regras (DIV-EXP-001, DIV-CON-001), conteúdo (Patrimônio), direção de criação (Brandbook por Pilar); protótipo existe e ativo | DIV-EXP-001, DIV-CON-001; protótipo `travessia-da-voz/`; `03-produto/patrimonio/` |
| **11** | **Próximos Caminhos (Hub de Continuidade)** | ⚠️ Conteúdo literal completo (5 opções, 2 rótulos corrigidos); protótipo implementado mas com bug confirmado ("Continuar meu dia" não leva à Home) | DIV-CON-001, DIV-EXP-001; protótipo `travessia-da-voz/` |
| **12** | **Reflexão Guiada** | ✅ Completa — estrutura, conteúdo literal das 15 Reflexões e texto de compartilhamento; sem protótipo | DIV-MA-012; `DIV-REFLEXOES-GUIADAS-Conteudo-Autoral-Completo-v1.0.md` |

---
---

# ETAPA 01 — Apresentação da Divícia

## 1. Objetivo

Comunicar quem é a Divícia, por que existe, e como acredita que o
autoconhecimento acontece — antes de pedir qualquer dado da mulher.

## 2. Experiência da Mulher

Sente que está conhecendo uma visão de mundo, não uma lista de
funcionalidades. Os nomes técnicos das Trilhas nunca aparecem aqui.
*(Princípio Narrativo, DIV-MA-009 §5)*

## 3. Objetivo de Produto

Validar se a mulher compreende o propósito da Divícia sem precisar
perguntar "o que exatamente eu faço aqui".

## 4. Orientações de UX

Sequência de telas curtas, uma ideia por tela, bastante respiro. Nenhum
campo de dado, nenhum aceite, nenhum aviso — esta etapa é puramente
institucional.

## 5. Direção de Criação

Contemplação antes de tecnologia. Tipografia editorial. Cores como
narrativa, nunca decoração.

**Destaque visual dentro do texto existente:** em cada capítulo (1, 2, 3,
6), uma sentença já existente no texto — marcada em negrito no bloco 6
abaixo — deve receber destaque visual (tipografia maior ou peso
diferenciado), tratada como o ponto alto da tela, não como mais uma
linha de texto corrido. Não são frases novas: são as próprias palavras
de DIV-MA-009, apenas com tratamento visual diferente. Objetivo:
mulheres que não leem o capítulo inteiro ainda saem com o essencial.

## 6. Conteúdo (literal, completo, DIV-MA-009 — sem cortes)

**Capítulo 1 — Por que a Divícia existe?**

> Há momentos em que nossos pensamentos, emoções e atitudes parecem
> seguir caminhos diferentes.
>
> Nem sempre compreendemos o que sentimos, por que reagimos como
> reagimos ou o que realmente está nos movendo.
>
> Quando essas partes deixam de conversar entre si, também nos
> afastamos de nós mesmas.
>
> O autoconhecimento não elimina os desafios da vida. Mas amplia nossa
> capacidade de atravessá-los com mais clareza, presença e consciência.
>
> **A Divícia nasceu para acompanhar cada mulher nesse reencontro consigo
> mesma, oferecendo experiências que ampliam sua capacidade de
> reconhecer aquilo que talvez ainda não estivesse visível.** *(destaque
> visual — bloco 5, Direção de Criação)*
>
> Esse reconhecimento pertence sempre à própria mulher. A Divícia apenas
> preserva o espaço onde ele pode acontecer.

**Capítulo 2 — Como acreditamos que esse caminho acontece?**

> **Acreditamos que o autoconhecimento não acontece de uma única vez.**
>
> **Ele acontece em movimentos.** *(as duas linhas acima: destaque
> visual)*
>
> Alguns nos aproximam de nós mesmas. Outros nos desafiam. Outros nos
> convidam a transformar.
>
> Nenhum deles é definitivo. Todos fazem parte do caminho.
>
> Foi dessa compreensão que nasceu a Trilha Divícia — construída sobre
> cinco movimentos: Presença, Conexão, Aprendizado, Ressignificação,
> Transformação.
>
> Não como etapas obrigatórias, mas como diferentes formas de caminhar
> em direção a si mesma.

**Capítulo 3 — Como isso ganha vida?** (três caminhos, sem nomes
técnicos ainda)

> **A Trilha pode ser vivida de diferentes maneiras. Cada experiência
> revela uma nova forma de percorrê-la.** *(destaque visual)*
>
> Um caminho mais leve — Conhecer as Vozes. Iniciar a Travessia.
> Refletir sobre cada encontro. Sempre disponível.
>
> Um caminho de maior presença — Percorrer Rituais. Explorar novos
> olhares. Ampliar significados. Conversar com a Lumi.
>
> Um caminho de construção contínua — Registrar o próprio caminho.
> Construir memória. Perceber continuidades. Fortalecer o processo de
> autoconhecimento ao longo do tempo.

**Capítulo 6 — Nosso compromisso**

> Na Divícia acreditamos que cada mulher é a maior especialista sobre
> sua própria vida.
>
> Por isso assumimos alguns compromissos.
>
> Nunca diremos quem você é. Nunca interpretaremos sua história por
> você. Nunca ofereceremos respostas prontas para perguntas que
> pertencem apenas à sua experiência.
>
> **Respeitaremos o seu tempo, o seu silêncio e a sua liberdade para
> escolher como deseja caminhar.** *(destaque visual)*
>
> Estaremos ao seu lado oferecendo experiências, perguntas, reflexões e
> caminhos. Mas o significado de cada passo será sempre construído por
> você.
>
> Porque acreditamos que o reconhecimento pertence sempre à própria
> mulher.
>
> Cada experiência pode ser vivida de forma independente. Você escolhe
> por onde começar, quando seguir e quantas vezes deseja voltar.
>
> Esta trilha é gratuita e estará sempre disponível para você.

Os Capítulos 4 e 5 de DIV-MA-009 não pertencem a esta etapa — o
Capítulo 4 é a transição para a Pesquisa de Chegada (ver Etapa 04) e o
Capítulo 5 é a base da Escolha da Jornada (ver Etapa 06). Ambos já
localizados e incorporados nas etapas correspondentes.

## 7. Regras Arquiteturais

Não gera Instância, não gera evento — conteúdo institucional estático.
*(DIV-MA-009 §13)*

Nenhum dado é coletado nesta etapa — a mulher apenas lê. A coleta começa
na Etapa 02, e só deve começar depois da Etapa 01.5 (ver abaixo).
*(DIV-PROT-CONFORMIDADE-JURIDICA-001 §2)*

**"Já tenho uma conta":** ao final da
Apresentação, duas opções: **Começar agora** e **Já tenho uma conta**.
A segunda opção é para quem já tem Registro de Entrada ou Conta e está
retornando (outro dispositivo, ou mesmo dispositivo depois de um
tempo). Ao informar o e-mail nesse fluxo, a plataforma **nunca revela
diretamente** se existe Conta, Registro de Entrada, ou nada — a
confirmação de titularidade (mesmo mecanismo da Etapa 06.5) ocorre
antes de qualquer revelação. Só depois da confirmação a mulher é
levada de volta ao ponto exato onde parou.

## 8. Implementação

Conteúdo pronto para uso literal, sem corte, sem decisão pendente.
O fluxo "Já tenho uma conta" ainda não implementado — depende do mesmo
mecanismo de confirmação de titularidade da Etapa 06.5.

---
---

# ETAPA 01.5 — Aviso de Privacidade

## 1. Objetivo

Dar base legal mínima para a coleta de dados pessoais que começa na
Etapa 02 (nome e pronome já são dado pessoal por si só, independente do
e-mail — LGPD Art. 5º, I: qualquer informação relacionada a pessoa
natural identificada ou identificável), sem antecipar o Cadastro técnico
completo.

## 2. Experiência da Mulher

Uma tela curta, sem fricção — não é a leitura integral dos Termos, é um
aviso objetivo com acesso aos documentos completos.

## 3. Objetivo de Produto

Fechar a lacuna identificada em DIV-PROT-CONFORMIDADE-JURIDICA-001 §2 antes que qualquer
dado pessoal seja coletado.

## 4. Orientações de UX

Não deve interromper o fluxo de onboarding de forma pesada — um aviso
objetivo, checkbox de aceite, link para Política e Termos completos
(DIV-PROT-JURIDICO-001), sem desviar a mulher para fora da sequência.

## 5. Direção de Criação

Mesmo tom editorial das demais telas de onboarding — este aviso não deve
parecer clausulado ou "jurídico" na forma, mesmo sendo obrigatório no
conteúdo.

## 6. Conteúdo

**Versão final de texto (redação fechada, enxuta — revisada
colaborativamente):**

> **Antes de começarmos**
>
> Para continuar, vamos pedir algumas informações e usá-las para
> personalizar seu caminho.
>
> `[ ] Li e concordo com os Termos de Uso e declaro que tive acesso à
> Política de Privacidade da Divícia.` *(obrigatório, nunca pré-marcado
> — DIV-PROT-JURIDICO-001 §4.2)* — (Termos de Uso) (Política de Privacidade)
>
> `[ ] Declaro que tenho 18 anos ou mais.` *(obrigatório — DIV-PROT-JURIDICO-001
> §4.4; DIV-PROT-CONFORMIDADE-JURIDICA-001 §9 exige que ocorra no mesmo momento do aceite)*
>
> `[ ] Quero receber novidades e conteúdos da Divícia. Sei que posso
> mudar essa escolha a qualquer momento.` *(opcional, nunca pré-marcado,
> não bloqueia o prosseguimento — DIV-PROT-JURIDICO-001 §4.3)*
>
> **[Continuar]**

**Links:** Termos de Uso e Política de Privacidade abrem em documentos
independentes, sem retirar a mulher do fluxo; ao retornar, ela continua
exatamente no ponto onde estava. *(DIV-PROT-CONFORMIDADE-JURIDICA-001 §4)*

**Cuidado editorial deliberado:** evitar frases genéricas sem conteúdo
jurídico real ("sua privacidade é importante para nós", "levamos sua
segurança a sério", "garantimos proteção total") — nenhuma delas informa
algo verificável, e a última contraria a nota de governança de LEG-001
(nenhum sistema é absolutamente seguro).

**Todos os elementos e a redação estão fechados** — três checkboxes,
ordem, e texto revisado colaborativamente (Mesa Arquitetural +
Bibliotecária + Fundadora), incluindo a distinção Termos/Política, a
correção de consentimento implícito e a remoção de afirmações
tecnicamente incorretas. Pronto para a ferramenta de materialização construir a tela completa.

## 7. Regras Arquiteturais

- Posição no fluxo: entre a Etapa 01 e a Etapa 02 — **confirmado**, não
  há mais conflito de posicionamento com EM-002 (ver nota no Roteiro:
  EM-002 posiciona Cadastro antes de tudo por premissa que não se
  sustenta mais — a razão real da posição atual é o Princípio Narrativo
  de DIV-MA-009 §5, não limitação técnica de PWA; pendência de correção
  formal do EM-002 registrada separadamente, não afeta esta etapa).
  *(DIV-PROT-CONFORMIDADE-JURIDICA-001 §2)*
- Aceite obrigatório de Termos e Política, checkbox único, nunca
  pré-marcado. *(DIV-PROT-JURIDICO-001 §4.2; DIV-PROT-CONFORMIDADE-JURIDICA-001 §3)*
- Registro de aceite: versão, idioma, timestamp, identificador de sessão,
  IP quando disponível. *(DIV-PROT-CONFORMIDADE-JURIDICA-001 §3)*

## 8. Implementação

Conteúdo completo, pronto para uso literal.

---
---

# ETAPA 02 — Identificação e Cadastro Técnico

## 1. Objetivo

Permitir que a mulher informe como deseja ser reconhecida durante sua
experiência e criar seu **Registro de Entrada** — a estrutura que
armazena, desde este momento, tudo que ela produz no Primeiro Encontro,
até ser promovida a Conta quando sua titularidade sobre o e-mail for
confirmada. *(ver Nota Arquitetural — Registro de Entrada)*

A etapa reúne, numa única experiência de interface, duas capacidades
distintas — Identificação narrativa (nome, pronome) e criação do
Registro de Entrada (e-mail, base para a futura Conta) — sem que isso
as torne o mesmo conceito arquitetural. *(Princípio da Conta da Mulher,
ver Princípios Gerais)*

## 2. Experiência da Mulher

Continuidade natural do acolhimento iniciado na Apresentação da Divícia
— nunca sensação de formulário administrativo. A linguagem explica de
forma simples por que o e-mail é pedido, sem expor Registro de Entrada,
Conta, autenticação ou banco de dados como conceitos técnicos.

## 3. Objetivo de Produto

Criar um Registro de Entrada antes do início da Pesquisa de Chegada,
garantindo que as respostas sejam associadas à mulher desde a origem,
que experiências futuras sejam recuperáveis, que ela possa retornar por
outro dispositivo, que acesso/exportação/exclusão sejam atendíveis desde
a promoção a Conta, e que a Home funcione como ponto permanente de
continuidade a partir dali.

## 4. Conceitos Arquiteturais

**Regra compartilhada:** nem o Registro de Entrada nem a Conta são
experiência, Instância de Experiência, ou Memória Experiencial — os
dois pertencem à camada de identificação, não à camada de conteúdo
vivido.

- **Registro de Entrada** — estrutura que nasce na Etapa 02 e armazena
  identificação, respostas da Pesquisa de Chegada, Trilha escolhida e
  aceite jurídico, até ser promovida a Conta. Ainda não é uma Conta.
- **Conta** — identidade persistente da mulher, resultado da promoção do
  Registro de Entrada após confirmação de titularidade. Não é o
  mecanismo de autenticação, não depende de pagamento, não define a
  Trilha escolhida.
- **Identificação narrativa** — nome de tratamento e pronome.
- **Autenticação** — mecanismo que comprova titularidade do e-mail
  informado. O mecanismo específico (e-mail, login social, passkey ou
  outro) é decisão de Engenharia — ver Pendências.
- **Validação do e-mail** — confirma posse do endereço; é o evento que
  promove o Registro de Entrada a Conta.

## 5. Momento de criação do Registro de Entrada e promoção a Conta

O Registro de Entrada nasce na confirmação da Etapa 02. Nesse momento, o
sistema deve: criar identificador interno único; registrar e-mail, nome
e pronome (quando informado); associar o aceite jurídico já registrado
na Etapa 01.5; associar a esse Registro todos os eventos e respostas
gerados a partir desse momento (Pesquisa de Chegada, Voz Movimento,
Escolha da Trilha).

A **promoção a Conta** ocorre no checkpoint de confirmação de
titularidade, após a Escolha da Trilha (ver Etapa 06) — não nesta
etapa. Não há migração: o mesmo identificador interno passa a ser
reconhecido institucionalmente como Conta.

## 6. Conteúdo (base: DIV-MA-010 Etapa 1 — pergunta de pronome com
variação proposta, ver Pendências)

> Como você gostaria de ser chamada durante seu caminho?
> *(campo livre)*

> Qual pronome você usa?
> - A [Nome]
> - O [Nome]
> - Prefiro não especificar.

> Qual e-mail você deseja usar para acessar a Divícia?
> *(campo obrigatório)*
>
> Texto de apoio: "Usaremos este e-mail para preservar sua experiência e
> permitir que você volte à Divícia com segurança."

Nenhuma confirmação de titularidade ocorre nesta etapa — ela é
solicitada, junto com a mensagem correspondente, apenas na Etapa 06.5
(Confirmação de Titularidade), depois da Escolha da Trilha.

O e-mail não deve ser utilizado para comunicações promocionais sem
autorização específica e separada — o aceite de marketing (Etapa 01.5)
permanece a única base para isso.

## 7. Regras Arquiteturais

- O Registro de Entrada nasce na Etapa 02. Toda Pesquisa de Chegada,
  Voz Movimento e Escolha da Trilha pertencem ao Registro de Entrada até
  a promoção; depois, pertencem à Conta. Toda Instância de Experiência
  (que só existe depois da promoção, dentro da Trilha) pertence sempre a
  uma Conta.
- O e-mail é o dado inicial usado para confirmar titularidade, não a
  identidade arquitetural da mulher. Nome e pronome não são credenciais
  de acesso.
- A validação do e-mail é o que promove o Registro de Entrada a Conta —
  não existe Conta antes disso. Pagamento não promove a Conta. A
  escolha de Trilha não promove a Conta (só antecede o checkpoint que
  promove). A Conta, uma vez promovida, existe independentemente da
  Trilha — inclusive Despertar, gratuita, passa por esse mesmo processo.
- Segregação: e-mail funciona como meio de confirmação; internamente, a
  relação entre Registro de Entrada/Conta e as respostas usa
  identificador técnico próprio, não o e-mail diretamente. *(reforça
  DIV-PROT-CONFORMIDADE-JURIDICA-001 §5)* **Esta regra é o que protege a Pesquisa de
  Chegada de e-mail digitado errado — ver Etapa 06.5, Confirmação de
  Titularidade.**
- A promoção do Registro de Entrada a Conta **não ocorre nesta etapa** —
  ocorre na Etapa 06.5 (Confirmação de Titularidade), logo após a
  Escolha da Trilha. Ver detalhamento completo lá.

**Estados do Registro de Entrada e da Conta:** `iniciado` (Registro de
Entrada criado, titularidade não confirmada — cobre todo o percurso até
o checkpoint) → promoção → `ativa` (agora Conta) → `exclusao_solicitada`
→ `excluida` (dados eliminados/dissociados, ressalvada retenção legal).

**Eventos mínimos:** `registro_entrada_criado`,
`confirmacao_titularidade_enviada`, `confirmacao_titularidade_reenviada`,
`email_corrigido`, `conta_promovida`, `cadastro_abandonado` (quando
mensurável — Registro de Entrada sem promoção após período de
inatividade). Nomenclatura genérica de propósito — o mecanismo concreto
(link, código, OTP) é decisão de Engenharia. Eventos não armazenam
conteúdo completo de dado pessoal em campos analíticos.

**Segurança:** e-mail armazenado com segurança, sem exposição pública;
conexão criptografada; credencial de confirmação (qualquer que seja o
mecanismo escolhido pela Engenharia) não registrada em logs acessíveis;
invalidada após uso ou vencimento; limite de tentativas de reenvio;
impossível acessar Registro de Entrada/Conta só pelo conhecimento do
e-mail.

## 8. Implementação

**Status: parcialmente implementado, requer atualização substancial.**
Evento anterior `identificacao_registrada` precisa ser decomposto nos
eventos mínimos acima. Fonte atual:
`03-produto/prototipo/pesquisa-de-chegada/index.html`.

**Critérios de conclusão do Registro de Entrada e da promoção a
Conta:** criação do Registro de Entrada, identificador interno, registro
de nome/pronome/e-mail, vínculo com aceite jurídico, envio/reenvio/
expiração do mecanismo de confirmação, correção de e-mail, promoção a
Conta, recuperação de acesso, associação da Pesquisa de Chegada ao
Registro/Conta, exclusão, tratamento de registros nunca promovidos,
proteção contra tentativas abusivas. **Enquanto esses critérios não
estiverem implementados, a etapa não é considerada tecnicamente
encerrada.**

**Pendências de Engenharia (fora do escopo deste Blueprint):** provedor
de autenticação, duração do link, limite de reenvios, política de
sessão, armazenamento de tokens, múltiplas abas/dispositivos, prevenção
de abuso, prazo de retenção de conta não confirmada, tratamento de
e-mail já cadastrado, alteração futura de e-mail, mensagens de erro.
Essas decisões não alteram os princípios arquiteturais acima.

---
---

# ETAPA 03 — Boas-vindas

## 6. Conteúdo (literal, DIV-MA-010 Etapa 2)

> Olá, [Nome].
>
> É uma alegria receber você.
>
> Antes de iniciarmos sua primeira experiência, gostaríamos de conhecer
> um pouco mais sobre o momento que você está vivendo.
>
> Não existem respostas certas.
>
> Apenas aquilo que fizer sentido para você hoje.

## 8. Implementação — já existente no protótipo

**Status: implementado.** Evento registrado: `boas_vindas_vista`.

---
---

# ETAPA 04 — Pesquisa de Chegada

## 1. Objetivo

Compreender como a mulher chega para viver este momento — nunca quem ela
é. *(Princípio da Pesquisa, DIV-MA-010)*

**Texto de transição (Capítulo 4, DIV-MA-009 — encontrado nesta
revisão):**

> Somente após compreender a natureza da Divícia inicia-se a Pesquisa de
> Chegada.
>
> Ela não procura responder: "Quem é esta mulher?"
>
> Ela procura compreender: "Como ela chega para viver sua primeira
> experiência?"

## 2. Experiência da Mulher

Nenhuma pergunta tem resposta certa. Nenhuma resposta a classifica.

## 6. Conteúdo — as 9 perguntas literais (DIV-MA-010 Etapa 3)

**Todas as 9 perguntas são obrigatórias** — não há opção de pular ou
avançar sem responder.

**P1 — Múltipla escolha.** Como você sente que chega para este momento
com a Divícia?
Sobrecarregada · Ansiosa · Confusa · Sem energia · Tensa · Frustrada ·
Triste · Em paz · Reflexiva · Motivada · Grata

**P2 — Escolha única.** O que despertou seu interesse pela Divícia neste
momento?
Quero me conhecer melhor · Estou vivendo um momento desafiador · Quero
compreender melhor minhas emoções · Quero cuidar mais de mim · Estou
buscando mais sentido para minha vida · Curiosidade

**P3 — Múltipla escolha.** Neste momento, o que mais ocupa espaço dentro
de você?
Meus pensamentos · Minhas emoções · Meu trabalho · Minha família · Meus
relacionamentos · Minha saúde · Meu futuro · Meu vazio · Não consigo
identificar

**P4 — Escolha única.** Quando algo importante acontece com você, qual
destas situações mais se parece com o que costuma viver?
Primeiro sinto, depois consigo compreender · Demoro um pouco para
entender o que estou vivendo · Muitas vezes sigo em frente sem entender
direito o que aconteceu · Às vezes percebo apenas muito tempo depois ·
Cada situação acontece de um jeito diferente

**P5.** Hoje, quando pensa em cuidar de você, qual frase faz mais
sentido?
Tenho dificuldade de encontrar espaço para mim · Estou tentando criar
esse espaço · Já encontrei formas que funcionam para mim · Meu cuidado
muda conforme o momento da vida

**P6.** Se tivesse que descrever este momento da sua vida, qual frase faz
mais sentido?
Estou buscando um novo começo · Estou atravessando mudanças importantes
· Estou tentando encontrar mais equilíbrio · Estou aprofundando quem já
sou · Estou vivendo um momento de plenitude

**P7.** Como você imagina que a Divícia poderá fazer parte da sua
rotina?
Alguns minutos quando sentir necessidade · Pequenos momentos ao longo da
semana · Quero construir um hábito constante · Ainda não sei

**P8 — Faixa etária indireta.** Há quanto tempo você caminha por este
mundo?
- Ainda descobrindo os primeiros contornos da própria história. *(até 24
  anos)*
- Construindo raízes e testando caminhos possíveis. *(25–34)*
- Aprofundando escolhas e sustentando o que já foi plantado. *(35–44)*
- Colhendo e ressignificando o que a vida ensinou até aqui. *(45–54)*
- Vivendo com a clareza de quem já atravessou muitas estações. *(55+)*

**P9.** Qual destas descrições mais se parece com o momento da sua
história que você está vivendo hoje?
- Estou construindo meu caminho.
- Estou conciliando muitas prioridades.
- Estou revisitando minha história.
- Estou abrindo espaço para um novo capítulo.

## 7. Regras Arquiteturais

- Ocorre uma única vez, independente da trilha escolhida depois.
  *(DIV-MA-009 §13)*
- P8 nunca pode ser exibida de volta como rótulo, nem cruzada com P9 para
  gerar julgamento, nem pedida como idade exata em outra tela.
- P6 e P9 nunca definem Pilar, Movimento ou classificação — só registro
  para reflexões futuras.

## 8. Implementação — já existente no protótipo

**Status: implementado**, incluindo a lógica correta de múltipla vs.
única escolha por pergunta. Eventos registrados:
`pesquisa_chegada_pergunta_respondida` (uma vez por pergunta),
`pesquisa_chegada_concluida` (com total de perguntas).

---
---

# ETAPA 05 — Voz Movimento

## 6. Conteúdo (literal, DIV-MA-010 Etapa 4)

> Todo caminho começa antes do primeiro passo. Ele começa quando
> permitimos que algo dentro de nós se mova.
>
> Hoje você escolheu olhar para si. Compartilhou um pouco do momento que
> está vivendo. E abriu espaço para iniciar uma nova experiência.
>
> Obrigada por confiar esse começo à Divícia.
>
> Agora é você quem escolhe como deseja caminhar. Não existe uma forma
> melhor. Existe apenas aquela que faz sentido para você hoje.

## 8. Implementação — já existente no protótipo

**Status: implementado.** Evento registrado: `voz_movimento_vista`.

---
---

# ETAPA 06 — Escolha do Caminho

## 1. Objetivo

Convidar a mulher a conhecer cada Trilha — nome, essência e o que ela
encontra — e escolher qual caminho seguir, com informação suficiente
para decidir de olhos abertos, não às cegas.

## 2. Experiência da Mulher

Ela pode conhecer as três Trilhas antes de decidir — abrir e ler sobre
cada uma quantas vezes quiser, sem que isso a comprometa. A confirmação
da escolha é um ato separado e explícito, não uma consequência de ter
espiado o conteúdo.

## 4. Orientações de UX

Duas camadas de interação, não uma:

1. **Explorar** — ela vê os três cards com nome e frase curta; toca em
   qualquer um pra abrir a descrição completa. Pode abrir as três,
   voltar, abrir de novo, em qualquer ordem, sem compromisso.
2. **Confirmar** — dentro da descrição completa (ou no próprio card),
   um botão explícito de escolha ("Escolher esta Trilha" ou
   equivalente) — só esse toque efetivamente seleciona a Trilha e
   dispara `jornada_escolhida`. Abrir a descrição não escolhe nada.

## 6. Conteúdo

**Nomes de Trilha em destaque nos cards:** o Princípio Narrativo
(DIV-MA-009 §5) trata de não antecipar nomes técnicos **antes** da
mulher entender por que as Trilhas existem — vale para a Etapa 01
(Apresentação), onde os nomes seguem ausentes. Aqui, ela já está diante
da escolha em si; nomear a Trilha em cada card, com destaque visual, é
necessário para que ela reconheça e lembre a qual Trilha pertence.

**Estrutura de cada Trilha — dois níveis, não um texto corrido:**

---

### TRILHA DESPERTAR

**Card (sempre visível na tela de Escolha do Caminho):**
> Quero conhecer a Divícia no meu ritmo. Conhecer as Vozes. Iniciar
> minhas primeiras Travessias. Refletir no meu próprio tempo. Sempre
> disponível.

**Ao clicar no card — modal ou componente equivalente (solução de
interface a critério da ferramenta de materialização):**
> A trilha Despertar reúne experiências criadas para favorecer o
> reconhecimento de si. Ao longo desse caminho, você poderá iniciar
> novas Travessias, receber diferentes perspectivas sobre a sua
> experiência, aprofundar reflexões e encontrar pequenos convites à
> presença no dia a dia.
>
> **[Escolher esta Trilha]**

---

### TRILHA DESCOBERTA

**Card (sempre visível):**
> Quero aprofundar meu caminho desde o início. Percorrer Rituais. Viver
> novas experiências. Conversar com a Lumi. Ampliar meus olhares.

**Ao clicar no card — modal ou componente equivalente:**
> A trilha Descoberta amplia a forma como você vive cada experiência.
> Novos caminhos de reflexão, experiências mais profundas e um espaço
> para guardar aquilo que faz sentido para você transformam encontros
> isolados em uma caminhada contínua. Ao longo desse percurso, você
> receberá o Retrato das Experiências, que integra diferentes
> experiências e revela novas conexões sobre o seu caminho. É também
> nessa trilha que a Lumi passa a acompanhar você, oferecendo novas
> perspectivas construídas a partir das experiências que você escolheu
> viver e preservar.
>
> *Esta trilha está em desenvolvimento e será disponibilizada em breve.*
>
> *(Sem botão de escolha nesta fase — módulo não ativo, ver
> DIV-PROT-MODULOS-001)*

---

### TRILHA INTEGRAÇÃO

**Card (sempre visível):**
> Quero construir um caminho contínuo. Tudo da Trilha Descoberta.
> Registrar minhas reflexões no Diário dos Saberes. Integração com o
> Mapa de Reflexão. Memória dos Caminhos.

**Ao clicar no card — modal ou componente equivalente:**
> A trilha Integração foi criada para quem deseja construir uma relação
> contínua com o próprio caminho. Ao registrar pensamentos, descobertas
> e reflexões, você passa a criar uma memória viva da sua caminhada. Com
> o tempo, essa história também permite que a Divícia compreenda melhor
> a forma como você percebe o mundo, tornando cada nova experiência mais
> conectada àquilo que você escolheu compartilhar.
>
> *Esta trilha está em desenvolvimento e será disponibilizada em breve.*
>
> *(Sem botão de escolha nesta fase — módulo não ativo, ver
> DIV-PROT-MODULOS-001)*

---

**Investimento (quando Descoberta/Integração estiverem ativas):**
demonstrado com sutileza dentro do modal de cada uma, junto da
descrição completa — não no card, não em tela separada. Ex.: menção
discreta de "assinatura mensal, semestral ou anual" (ver Regras
Arquiteturais), sem destaque comercial pesado. Redação final do valor
pendente de decisão comercial.

## 7. Regras Arquiteturais

- Trilha e Acesso são conceitos independentes. *(ADR-005, DIV-MA-009)*
- Sem pré-requisito entre trilhas — pode-se iniciar direto em Integração.
- Despertar não tem custo associado; Descoberta e Integração têm,
  com assinatura mensal, semestral ou anual, por envolverem Diário,
  Memória Experiencial, Interpretação da Lumi.
- Descoberta e Integração são clicáveis e mostram a descrição completa
  com o aviso "em desenvolvimento" — sem gerar tela, lógica ou dado de
  módulo não ativo (DIV-PROT-MODULOS-001). Tratar como condicional
  simples no estado da aplicação (switch/case pelo ID da Trilha
  escolhida) — sem lógica adicional além de exibir o texto estático.
- **Explorar ≠ Escolher.** Abrir a descrição completa de qualquer
  Trilha (inclusive repetidamente, em qualquer ordem) não gera o
  evento `jornada_escolhida` nem qualquer efeito no Registro de
  Entrada. Só o toque explícito no botão de confirmação dispara a
  escolha.

## 8. Implementação — já existente no protótipo, requer atualização

**Status: parcialmente implementado.** Evento registrado:
`jornada_escolhida` (com a trilha selecionada) — mantido; o protótipo
atual mostra só os cards curtos, precisa incorporar a descrição
completa de cada Trilha nesta mesma tela.

---
---


# ETAPA 06.5 — Confirmação de Titularidade

## 1. Objetivo

Confirmar que a mulher é titular do e-mail informado na Identificação
(Etapa 02), promovendo o Registro de Entrada a Conta — sem pedir
nenhum dado em branco de novo, e sem revelar a existência de qualquer
registro antes dessa confirmação.

## 2. Experiência da Mulher

Ela vê o e-mail que já informou, pré-preenchido — não um formulário em
branco. Confirma ou corrige. Não precisa entender o que está
acontecendo por trás (Registro de Entrada virando Conta) — só sente
que está confirmando algo que já começou.

## 3. Objetivo de Produto

Formalizar a Conta da Mulher a partir do Registro de Entrada, no
primeiro momento em que a continuidade da experiência realmente exige
identidade persistente confirmada — sem antecipar isso nem atrasá-lo
além do necessário.

## 4. Orientações de UX

Tela única, e-mail pré-preenchido e editável, botão de confirmação.
Sem fricção adicional — não é um novo cadastro, é uma confirmação.

## 6. Conteúdo

**Mecanismo (decidido nesta revisão):** código de confirmação por
e-mail, digitado na própria tela — sem sair do app. WhatsApp registrado
como candidato forte para a versão 2 (ver Pendência Técnica).

> Enviamos um código para o seu e-mail. Digite abaixo para confirmar.
>
> `[______]` *(campo de código, 6 dígitos)*
>
> **[Confirmar]**

Fluxo:

```
Escolha da Trilha (Etapa 06)
        ↓
Confirmação do e-mail (exibido, não em branco)
        ↓
Correção do e-mail, se necessário
        ↓
Código enviado por e-mail, digitado na tela
        ↓
Registro de Entrada promovido a Conta
```

## 7. Regras Arquiteturais

- **Não é uma nova tela de cadastro em branco** — exibe o e-mail já
  registrado no Registro de Entrada, permitindo confirmar ou corrigir.
  Correção dispara `email_corrigido` no mesmo Registro (mesmo
  identificador interno); confirmação do código dispara
  `conta_promovida`. Como as respostas já pertencem ao Registro pelo
  ID, não ao e-mail, nada se perde e ela não precisa responder a
  Pesquisa de Chegada novamente.
- **Mecanismo definido para o MVP: código por e-mail.** Parâmetros
  (tempo de expiração, número de reenvios, tratamento de código
  incorreto) permanecem decisão de Engenharia — este Blueprint define
  o mecanismo em alto nível, não os parâmetros operacionais. *(ver
  Pendência Técnica)*
- **Para o protótipo: simular, não implementar de verdade.**
  Qualquer código digitado é aceito (ou um código fixo funciona sempre)
  — sem conectar a provedor de e-mail real. A ferramenta de
  materialização usada nesta fase é voltada a design/prototipagem, sem
  backend; a implementação funcional real (envio e validação de
  verdade) só ocorre quando o produto migrar para uma ferramenta
  full-stack ou desenvolvimento próprio.
- **A plataforma nunca informa se existe ou não uma Conta ou Registro
  de Entrada apenas com base no e-mail informado.** Quando houver
  necessidade de recuperação de acesso ou continuidade (ver "Já tenho
  uma conta", Etapa 01), a confirmação da titularidade deve ocorrer
  **antes** da revelação de qualquer informação relacionada à
  existência daquele Registro ou Conta.
- **O Registro de Entrada não depende do dispositivo.** A pergunta
  arquitetural correta não é "como recuperar em outro aparelho", é
  "como confirmar que quem voltou é realmente a titular daquele
  Registro". O Registro não está associado ao navegador — está
  associado à identidade que será confirmada neste checkpoint (ou,
  antes disso, pelo fluxo "Já tenho uma conta").
- **Risco distinto, não resolvido por esta regra:** perda total de
  vínculo local com o Registro de Entrada (outro dispositivo/navegador
  sem identificador salvo) não é uma falha de segurança — é
  justamente o cenário que o fluxo "Já tenho uma conta" (Etapa 01)
  existe para cobrir, sempre exigindo confirmação de titularidade antes
  de revelar qualquer coisa.

## 8. Implementação

Não implementada. Mecanismo já decidido (código por e-mail) — falta a
Engenharia definir os parâmetros operacionais antes da construção
(provedor de envio, expiração, reenvio — ver Pendência Técnica).

---
---

# ETAPA 08 — Boas-vindas da Trilha (recorte Despertar)

## 1. Objetivo

Acolher a mulher especificamente na Trilha Despertar, já com o nome
técnico revelado, reforçando a ausência de ritmo obrigatório.

## 6. Conteúdo (fornecido jul/2026)

> Bem-vinda à trilha Despertar.
>
> Este é um espaço para explorar novas perspectivas sobre aquilo que
> você vive, sente e percebe.
>
> Não existe um ritmo ideal nem um caminho obrigatório. Cada experiência
> acontece no seu tempo, e este caminho permanecerá sempre aberto para
> quando você desejar voltar.
>
> **[Começar]**

**Transição para a Home (Etapa 09):** o botão leva diretamente à Home,
sem tela intermediária. Não há confirmação adicional nem mensagem de
transição — a Home é o próximo destino natural depois da boas-vindas.

## 7. Regras Arquiteturais

- Esta etapa só existe para a Trilha Despertar nesta fase do MVP — as
  demais Trilhas não chegam a este ponto do fluxo enquanto "em
  desenvolvimento" (Etapa 06 já as intercepta antes, com o aviso
  correspondente nos próprios cards).

## 8. Implementação

Conteúdo completo, pronto para uso literal.

---
---

# ETAPA 09 — Home

## 1. Objetivo

Oferecer à mulher um ponto permanente de reencontro com sua caminhada na
Divícia, organizando as possibilidades disponíveis no presente.

## 2. Experiência da Mulher

Acolhimento sem pressão — a Home nunca comunica encerramento nem cobra
retorno. Ela funciona como Hub determinístico e baseado em regras, não
como feed algorítmico — o que aparece e onde aparece segue lógica
fixa, previsível, não personalização opaca.

## 3. Objetivo de Produto

Estabelecer a Home como o destino permanente de retorno depois de
qualquer experiência — sem depender de Lumi ou Memória nesta fase
(módulos não ativos, DIV-PROT-MODULOS-001). A arquitetura já prevê um
"Motor de Possibilidades" desacoplado, preparado para integração futura
com a Lumi, mas nesta fase opera só com regras fixas.

## 4. Orientações de UX

Seis seções organizam a tela: Sopro do Dia, Iniciar Travessia, Explore
algo novo, Meu Espaço, Novidades, Loja. Cada uma tem regra própria de
exibição (permanente ou condicional) — nenhuma decisão de exibição é
arbitrária ou aleatória.

Dois princípios regem a montagem da tela:
- **Princípio da Independência da Origem das Possibilidades** — cada
  possibilidade (card, sugestão, convite) é avaliada por sua própria
  regra, independente de onde ela vem no sistema.
- **Princípio da Autoridade Final da Home** — a Home decide o que
  exibir e em que ordem; nenhum módulo externo pode forçar exibição
  fora das regras da própria Home.

## 5. Direção de Criação

**Fonte de referência visual — hierarquia (aplica-se a toda direção de
criação deste Blueprint):** o Brandbook (PDF) foi a origem de tudo, mas
é pouco detalhado — mostra a cor como imagem, não como código exato.
A referência que deve ser seguida com prioridade são os **4 documentos
MD** em `07-identidade-visual/` (`DIV-MANUAL-CROMATICO-v1.0`,
`DIV-GUIA-CONCEITUAL-v1.0`, `DIV-GLOSSARIO-TOM-DE-VOZ-v1.0`,
`DIV-IDENTIDADE-VISUAL-v1.0`), que detalham o que o Brandbook só
mostra em imagem — incluindo código Pantone exato por Pilar. As artes
de referência (símbolos dos Pilares, arte de cada Pilar, Coleção Vozes
do Silêncio, Diário, Ritual) estão salvas como PDF nas subpastas de
`07-identidade-visual/` (`simbolos-pilares/`, `fundo-de-vozes/`,
`colecao-vozes-do-silencio/`, `diario-dos-saberes/`,
`ritual-da-consciencia/`).

**Ícones de navegação (barra inferior):**

Princípio geral: nunca reaproveitar os símbolos dos 5 Pilares (Presença,
Conexão, Aprendizado, Ressignificado, Transformação) como ícone de
navegação — eles carregam significado filosófico; navegação exige
ícones funcionais e neutros, sem sobrecarga de sentido. Estilo de linha
simples (stroke ~1.5–2px), monocromático (dourado, coerente com
símbolos e tipografia), sem preenchimento, sobre fundo claro. Este é um
briefing de direção, não uma especificação fechada — a materialização
exata fica a critério de quem construir a tela.

| Área | Natureza | Iconografia sugerida | Estado nesta fase | Tratamento visual |
|---|---|---|---|---|
| Home | Funcional | Casa, ou equivalente | Ativo | Padrão — cor plena |
| Explorações | Funcional | Bússola, lupa ou equivalente (descoberta) | Não ativo (DIV-PROT-MODULOS-001) | "Em modo prévia" — mesmo tratamento visual usado para Descoberta/Integração |
| Ritual | Funcional | Ícone próprio da funcionalidade — nunca símbolo de Pilar | Não ativo | "Em modo prévia" |
| Diário | Funcional | Caderno ou livro | Não ativo | "Em modo prévia" |
| Reflexões Guiadas | Funcional | Ícone próprio da funcionalidade — nunca símbolo de Pilar | Ativo (Despertar) | Padrão — cor plena |
| Meu Espaço | Funcional | Perfil ou espaço pessoal estilizado — nunca símbolo de Pilar | Ativo (Despertar) | Padrão — cor plena |

Itens marcados "não ativo" existem visualmente na barra (a Home já
prevê acesso "em modo prévia" a eles), mas não geram tela, lógica ou
dado — apenas o mesmo indicador visual de indisponibilidade já usado
em outros pontos do produto. Nenhum ícone novo deve ser inventado por
etapa; a barra usa o mesmo conjunto em toda a navegação.

**Chrome de interface (elementos que não são Pilares nem produto):**
botão de voltar, seta de avançar, fechar modal, spinner de
carregamento, ícone de Configurações — mesmo direção dos ícones de
navegação acima (linha simples, monocromático dourado, sem
preenchimento) — briefing, não especificação fechada.

## 6. Conteúdo

**Mensagem ao tocar num item não ativo da barra (decidido nesta
revisão) — mesmo texto reutilizado nas experiências avulsas da Etapa
11, Próximos Caminhos:**

> **O Ritual da Consciência**
> Uma experiência mais profunda para quem desejar ampliar sua reflexão
> por meio dos cinco Pilares da Divícia.
> Em breve, este espaço estará disponível para você.

> **Explorações**
> Novas experiências de autoconhecimento para aprofundar temas
> específicos da sua jornada, com diferentes formas de ampliar seu
> campo de visão.
> Em breve, este espaço estará disponível para você.

> **Diário dos Saberes**
> Um espaço pessoal para registrar percepções, reconhecer aprendizados
> e acompanhar, ao longo do tempo, aquilo que faz sentido preservar da
> sua trajetória.
> Em breve, este espaço estará disponível para você.

**Seções permanentes/condicionais** (ordem de exibição na tela), com
status real de texto literal, confirmado pela Bibliotecária:

**Sopro do Dia — decidido:**
> **Sopro do Dia**
> [frase rotativa, sorteada do banco em `sopros-do-dia.json`, seguindo
> as regras já definidas — rotatividade aleatória pura nesta fase, sem
> checagem de repetição de 90 dias]

**Iniciar a Travessia — decidido:** texto clicável em destaque, sem
texto complementar.

> **[Iniciar a Travessia]**

**Explore algo novo — decidido, escopo Despertar MVP:**

Nesta fase, só Reflexões Guiadas são divulgadas neste card — Ritual e
Explorações não aparecem aqui, porque não estão ativos nesta fase
(DIV-PROT-MODULOS-001).

Título do card: **"Explorar Algo Novo"**.

Formato: rotação de uma Reflexão por vez, nunca repetindo a última
mostrada (mesma regra de D.1.1, DIV-MA-013).

**As 15 Reflexões disponíveis para rotação, com texto completo:**

> **SILÊNCIO INTERNO**
> Conheça a Reflexão Guiada SILÊNCIO INTERNO
> Nesta reflexão, o convite não é encontrar respostas.
> É apenas observar como você tem se relacionado com os momentos em que o ruído diminui.
> Talvez exista algo esperando para ser escutado.
>
> **CUIDADO**
> Conheça a Reflexão Guiada CUIDADO
> Nem sempre percebemos onde nosso cuidado tem sido direcionado.
> Às vezes ele alcança tudo ao nosso redor, menos nós mesmas.
> Nesta reflexão, o convite é reconhecer o que, hoje, está pedindo mais atenção na sua vida.
>
> **MUDANÇAS**
> Conheça a Reflexão Guiada MUDANÇAS
> Toda mudança atravessa um tempo próprio.
> Algumas chegam de repente. Outras começam silenciosamente, antes mesmo de serem percebidas.
> Nesta reflexão, o convite é reconhecer como você tem vivido os ciclos de mudança da sua vida.
>
> **O QUE ME MOVE**
> Conheça a Reflexão Guiada O QUE ME MOVE
> Por trás de cada escolha existe algo que nos impulsiona.
> Nem sempre percebemos o que realmente está conduzindo nossos passos.
> Nesta reflexão, o convite é reconhecer o que tem inspirado suas escolhas neste momento.
>
> **MOVIMENTO INTERNO**
> Conheça a Reflexão Guiada MOVIMENTO INTERNO
> Nem tudo o que acontece dentro de nós encontra palavras imediatamente.
> Alguns movimentos apenas começam a pedir espaço.
> Nesta reflexão, o convite é perceber o que está buscando ganhar voz dentro de você.
>
> **MINHA HISTÓRIA**
> Conheça a Reflexão Guiada MINHA HISTÓRIA
> A vida é feita de capítulos.
> Alguns encerram ciclos. Outros anunciam começos que ainda não conseguimos enxergar por completo.
> Nesta reflexão, o convite é reconhecer o capítulo que você sente estar vivendo hoje.
>
> **RELAÇÕES**
> Conheça a Reflexão Guiada RELAÇÕES
> Cada relação revela algo sobre quem somos.
> Algumas fortalecem. Outras desafiam. Todas podem nos ensinar.
> Nesta reflexão, o convite é observar como você tem vivido os vínculos que fazem parte da sua vida.
>
> **ESSÊNCIA VIVA**
> Conheça a Reflexão Guiada ESSÊNCIA VIVA
> Por trás dos papéis, das expectativas e das circunstâncias, existe algo em você que permanece.
> Nesta reflexão, o convite é aproximar-se do que faz sentido para quem você é.
>
> **SUSTENTAÇÃO**
> Conheça a Reflexão Guiada SUSTENTAÇÃO
> A forma como sustentamos nossos dias influencia silenciosamente tudo o que vivemos.
> Nesta reflexão, o convite é reconhecer o que hoje fortalece — ou fragiliza — a base da sua vida.
>
> **ENERGIA DA SEMANA**
> Conheça a Reflexão Guiada ENERGIA DA SEMANA
> Cada semana traz um ritmo diferente.
> Percebê-lo pode ajudar você a atravessar esse momento com mais consciência.
> Nesta reflexão, o convite é reconhecer qual energia tem ocupado mais espaço em você.
>
> **FOCO DA SEMANA**
> Conheça a Reflexão Guiada FOCO DA SEMANA
> Nossa atenção revela muito sobre o momento que estamos vivendo.
> Nem sempre ela está onde gostaríamos.
> Nesta reflexão, o convite é perceber para onde sua atenção tem sido naturalmente direcionada.
>
> **PESO E LEVEZA**
> Conheça a Reflexão Guiada PESO E LEVEZA
> Há dias em que tudo parece mais leve.
> Em outros, algo pesa, mesmo sem conseguirmos explicar.
> Nesta reflexão, o convite é reconhecer o que predomina em você neste momento.
>
> **DECISÃO EM ABERTO**
> Conheça a Reflexão Guiada DECISÃO EM ABERTO
> Nem toda decisão precisa ser tomada imediatamente.
> Às vezes, compreender como nos relacionamos com uma escolha já transforma a forma de atravessá-la.
> Nesta reflexão, o convite é observar onde você está diante de uma decisão ainda em aberto.
>
> **ENTRE O SIM E O NÃO**
> Conheça a Reflexão Guiada ENTRE O SIM E O NÃO
> Ao longo da vida, nossos "sins" e "nãos" moldam caminhos, relações e possibilidades.
> Nem sempre percebemos como essas escolhas acontecem.
> Nesta reflexão, o convite é reconhecer como você tem vivido suas escolhas mais recentes.
>
> **O PILAR DO MEU DIA**
> Conheça a Reflexão Guiada O PILAR DO MEU DIA
> Mesmo nos dias mais comuns, um movimento costuma se destacar.
> Às vezes ele passa despercebido até o momento em que olhamos para trás.
> Nesta reflexão, o convite é reconhecer qual Pilar esteve mais presente no seu dia.

Fonte: `Explore-Algo-Novo-Convites-Reflexoes-Guiadas.json`.

**Distinção importante (esclarecida nesta revisão):** "Explore Algo
Novo" é só a vitrine rotativa — mostra **uma** Reflexão por vez, a que
estiver sendo divulgada no momento. A **entrada oficial** para
Reflexões Guiadas — onde ficam disponíveis todas as 15, ou o
subconjunto que for definido — é o botão próprio "Reflexões Guiadas"
na barra de navegação (ver tabela de ícones acima), não este card.

**Pendência de conteúdo/decisão:** o botão "Reflexões Guiadas" mostra
todas as 15, ou um subconjunto curado? Ainda não definido.

**Nota de UX (registrada, não resolvida):** com Reflexões Guiadas
somando-se a Home/Explorações/Ritual/Diário/Meu Espaço, a barra de
navegação passa a ter 6 áreas — vale considerar com quem materializa
se cabe tudo numa barra inferior padrão, ou se algum item precisa de
outro tratamento (ex.: dentro de um menu, não na barra principal).

**Meu Espaço — texto literal (estado vazio, primeira visita, Despertar):**

> Este espaço aguarda por você. Você está na trilha Despertar, o
> primeiro encontro com a Divícia, onde a Travessia da Voz e as
> Reflexões Guiadas já estão disponíveis para você viver.
>
> Na trilha Descoberta, a Lumi chega para caminhar ao seu lado: suas
> interpretações passam a acompanhar as experiências que você já
> conhece, o Ritual se torna parte da sua trilha, e novas experiências,
> como as Explorações, se abrem para você.
>
> Na trilha Integração, tudo isso se aprofunda, e o Diário nasce como
> espaço contínuo de registro. A Lumi passa a te conhecer mais de
> perto, acompanhando sua voz ao longo da caminhada.
>
> A partir daí, este espaço passa a guardar o histórico das
> experiências que você escolher salvar, e a reunir Books, suas
> experiências consolidadas, interpretadas pela Lumi, prontas para
> você revisitar sempre que desejar.

**Novidades — três textos, rotação decidida: 1 por vez, rotativo**
(mesmo padrão do Sopro do Dia e do Explore algo novo):

> **Em breve: novas formas de viver sua caminhada**
> Além da Travessia Despertar, estamos preparando novas experiências
> para acompanhar diferentes momentos da sua jornada.

> **O Ritual da Consciência está chegando**
> Uma experiência mais profunda para quem desejar ampliar sua reflexão
> através dos cinco pilares da Divícia.

> **Seu espaço também vai crescer**
> Em breve você poderá guardar suas experiências, acompanhar sua
> caminhada e reencontrar seus registros sempre que desejar.

**Loja — texto de estado vazio (dentro da tela da Loja, catálogo ainda
sem oferta; a Loja em si permanece sempre presente e clicável na Home):**

> Novas experiências estão sendo preparadas para você.
> Em breve você encontrará aqui experiências que poderão ampliar sua
> caminhada com a Divícia.

**Acessos permanentes na barra de navegação:** Ritual, Explorações,
Diário em modo prévia; Reflexões Guiadas funcional.

## 7. Regras Arquiteturais

- Princípio da Independência da Origem das Possibilidades e Princípio
  da Autoridade Final da Home regem toda a montagem da tela (ver bloco
  4). *(DIV-MA-013, Blocos C–E)*
- Módulos não ativos (Lumi, Diário, Memória, Ritual, Explorações) não
  geram tela, lógica ou dado nesta fase — só o indicador visual "em
  modo prévia". *(DIV-PROT-MODULOS-001)*
- A Home nunca comunica encerramento de experiência, nunca mede
  ausência, nunca cobra retorno. *(Princípio Geral de Materialização)*
- "Explore algo novo" seleciona por rotatividade — nunca repete a
  última experiência mostrada. Nesta fase (Despertar MVP), só
  Reflexões Guiadas são elegíveis para rotação — Ritual e Explorações
  ficam de fora por não estarem ativos. *(DIV-MA-013, Bloco C-D, D.1.1;
  escopo Despertar decidido nesta revisão)*
- "Novidades" também roda 1 por vez, mesma lógica de rotatividade —
  nunca os três simultâneos.

## 8. Implementação

Não existe protótipo da Home — precisa ser construída do zero.

---
---

# ETAPA 10 — Iniciar a Travessia

## 1. Objetivo

Permitir que a mulher, a partir da Home, inicie uma Travessia da Voz —
uma **Experiência** completa, no vocabulário de DIV-EXP-001 — e viva o
encontro com uma Voz do Patrimônio no seu próprio ritmo.

## 2. Experiência da Mulher

Ela escolhe um número, uma Voz é revelada. A partir daí, ela está em um
dos **Estados Navegacionais** reconhecidos pela Arquitetura da
Navegação: **Em Exploração** (percorrendo livremente) ou **Em
Aprofundamento** (caso opte por ampliar via Mapa do Despertar/Para
Refletir). Nenhum desses estados é interpretado — a plataforma só
reconhece o estado observável, nunca a intenção ou emoção por trás
dele. (DIV-EXP-001, secao 6)

## 3. Objetivo de Produto

Registrar o evento `voz_revelada` no momento em que a Voz aparece — que
já é, por definição, o suficiente para considerar a Travessia
**concluída** (`travessia_concluida`). Qualquer interação posterior
(Mapa do Despertar, Para Refletir) é **Aprofundamento** no sentido
arquitetural do termo — "ampliação qualitativa da experiência já
iniciada... sem alterar o protagonismo da mulher" (DIV-EXP-001,
Glossário, secao 3) — rastreada separadamente, nunca condição para
conclusão.

## 4. Orientações de UX

Protótipo já existe e está ativo — ver bloco 8. A experiência é
organizada em **Etapas** internas (no sentido de DIV-EXP-001, secao
5.2): Revelação da Voz, Mapa do Despertar, Para Refletir, Próximos
Caminhos — cada uma com objetivo próprio, nenhuma limitando a liberdade
da mulher de ir direto ao final se quiser. Cada Chave do Mapa do
Despertar é uma **Subetapa** — exploração interna sempre opcional.

## 5. Direção de Criação

Nenhuma direção de criação específica foi definida quando o protótipo
foi construído. A orientação para esta e para as próximas etapas:

- Seguir os 4 documentos MD de `07-identidade-visual/`
  (`DIV-MANUAL-CROMATICO-v1.0`, `DIV-GUIA-CONCEITUAL-v1.0`,
  `DIV-GLOSSARIO-TOM-DE-VOZ-v1.0`, `DIV-IDENTIDADE-VISUAL-v1.0`) como
  referência principal — mais detalhados que o Brandbook em PDF
  (origem de tudo, mas só mostra a cor como imagem; os MD trazem o
  código Pantone exato por Pilar).
- **Toda Voz pertence a um Pilar.** No momento em que a Voz é revelada,
  a arte exibida deve seguir o Pantone e a arte definidos nesses
  documentos para aquele Pilar especificamente — nunca um tratamento
  genérico. Arte de referência de cada Pilar disponível em PDF nas
  subpastas de `07-identidade-visual/` (`simbolos-pilares/`,
  `fundo-de-vozes/`).
- As demais telas (fora do momento de revelação da Voz) seguem a
  mesma direção visual do restante do app — briefing, não
  especificação fechada; conta-se com a leitura de quem materializa.
- Regra permanente, válida para toda etapa que exibir conteúdo de uma
  Voz: sempre verificar a qual Pilar ela pertence antes de aplicar
  qualquer padronização visual.

## 6. Conteúdo

Sem pendência. O conteúdo já existe integralmente no protótipo (textos
fixos) e no Patrimônio, em `03-produto/patrimonio/`: Pilares, Mapa das
Dimensões, Coleção Vozes do Silêncio, Mapa do Despertar (ver pastas já
confirmadas: `pilares/`, `mapa-das-dimensoes/`,
`colecao-vozes-do-silencio/`, `mapa-do-despertar/`).

## 7. Regras Arquiteturais

- A navegação organiza possibilidades, nunca determina percursos; a
  Travessia pertence à mulher, não à plataforma. (DIV-EXP-001, secoes
  4.1 e 4.2)
- A plataforma nunca comunica encerramento — ao final da Travessia, ela
  reorganiza possibilidades de continuidade, nunca apresenta a
  experiência como "terminada". (DIV-EXP-001, secao 4.3)
- `voz_revelada` = `travessia_concluida` — sem etapa intermediária
  obrigatória.
- Card Compartilhável **não** existe na Travessia — exclusivo de
  Reflexões Guiadas.
- **Retorno** (revisitar etapas já percorridas dentro da mesma
  Instância) preserva integralmente o contexto e nunca reinicia a
  Instância nem altera eventos já registrados. (DIV-EXP-001, secao 5.7)
- Fonte arquitetural: DIV-EXP-001 (Navegação das Experiências),
  DIV-CON-001 (Continuidade) — ambos Documentos Fundadores, lidos
  integralmente nesta revisão.

## 8. Implementação

**Protótipo existe e está funcionalmente ativo:**
`03-produto/prototipo/travessia-da-voz/`. Status literal do LEIA-ME:
*"Ativo — protótipo em revisão visual, aguardando confirmação final
antes de commit definitivo do código."* Não é Documento Fundador.

**Importante — o protótipo não é referência visual.** Quando foi
construído, o objetivo não era estabelecer padrão visual — a "revisão
visual" mencionada no LEIA-ME não significa que o resultado deva
orientar o estilo da ferramenta de materialização. A referência visual
correta é sempre os documentos de Identidade Visual (ver Etapa 09,
bloco 5) — o protótipo serve só como referência de **fluxo e lógica**,
não de aparência.

Ver Etapa 11 para a correção de rótulo em duas das opções de "Próximos
Caminhos".

---
---

# ETAPA 11 — Próximos Caminhos (Hub de Continuidade)

## 1. Objetivo

Organizar, ao final da Travessia, possibilidades legítimas de
continuidade — nunca determinar um percurso obrigatório. É a
materialização, para o MVP, do que DIV-CON-001 chama de "Hub de
Continuidade", e que DIV-EXP-001 já lista nominalmente como exemplo de
Hub: "Próximos Caminhos".

## 2. Experiência da Mulher

Ela vê caminhos, não instruções. Nenhuma opção é apresentada como mais
correta ou mais completa que outra — inclusive "continuar meu dia" é
continuidade legítima, não abandono. (DIV-EXP-001, secao 2.4 e secao 7)

## 3. Objetivo de Produto

Construir o conjunto de possibilidades autorizadas para este momento
específico. Nesta fase, isso inclui tanto o que está incluído na
Trilha quanto o que está disponível como experiência **avulsa** — uma
categoria de disponibilidade que ainda não está registrada em
DIV-PROT-MODULOS-001 (ver Pendências).

## 4. Orientações de UX

Um Hub, por definição arquitetural, "organiza possibilidades... nunca
determina percursos... cada possibilidade possui propósito claro...
nenhuma representa continuidade obrigatória." (DIV-EXP-001, secao 5.5)

## 5. Direção de Criação

Mesma diretriz da Etapa 10 — seguir o Brandbook e a linguagem visual já
adotada no app; sem tratamento específico adicional para esta tela.

## 6. Conteúdo (literal, protótipo confirmado)

> PRÓXIMOS CAMINHOS
>
> **Como você quer continuar?**
>
> Um convite para decidir como cuidar do que surgiu.
>
> - Reflexões Guiadas →
> - Explorações (Avulsa) →
> - Ritual da Consciência (Avulso) →
> - Receber uma nova Voz →
> - Continuar meu dia →

**Correção de rótulo decidida nesta revisão:** "Explorações" passa a
"Explorações (Avulsa)"; "Jornadas Temáticas" é substituída por "Ritual
da Consciência (Avulso)" — não é remoção de opções, é atualização de
rótulo. As 5 opções permanecem.

**Matriz Voz → Reflexões:** cada uma das 40 Vozes tem 3 Reflexões
sugeridas — associação disponível em
`Matriz-Vozes-Reflexoes-referencia.json` (fonte oficial: Patrimônio de
Reflexões Guiadas, Parte 3). Aplica-se só aos Territórios (9
Reflexões); os 6 Instantâneos (Energia da Semana, Foco da Semana, Peso
e Leveza, Decisão em Aberto, Entre o Sim e o Não, O Pilar do Meu Dia)
não têm vínculo com nenhuma Voz — ficam disponíveis só via Home.

**Reflexões Guiadas é módulo ativo** (DIV-PROT-MODULOS-001) — o aviso
"em breve" que aparece hoje no protótipo não deveria estar aqui; é
resíduo de um momento em que o conteúdo ainda não existia. Ao tocar em
"Reflexões Guiadas", deveria abrir uma tela real mostrando as 3
Reflexões sugeridas pela Matriz para a Voz revelada na Travessia —
ainda não implementado.

**Desdobramento ao toque em cada opção:**

- **Reflexões Guiadas →** leva para uma tela nova (não modal),
  mostrando as 3 Reflexões sugeridas pela Voz revelada — consultar
  `Matriz-Vozes-Reflexoes-referencia.json` pelo número/nome da Voz.
  Cada uma das 3 Reflexões sugeridas exibe seu próprio "texto convite
  de apresentação" (mesmo texto de `Explore-Algo-Novo-Convites-Reflexoes-Guiadas.json`,
  reutilizado aqui — ver Etapa 09, bloco 6, para o texto completo das
  15 Reflexões). Ainda não implementado — hoje só mostra "em breve".
- **Explorações (Avulsa) →** ao tocar, exibe (mesmo texto definido na
  Etapa 09, Home):
  - **Explorações**
  - Corpo: *Novas experiências de autoconhecimento para aprofundar
    temas específicos da sua jornada, com diferentes formas de ampliar
    seu campo de visão.*
  - Linha final: *Em breve, este espaço estará disponível para você.*
- **Ritual da Consciência (Avulso) →** ao tocar, exibe (mesmo texto
  definido na Etapa 09, Home):
  - **O Ritual da Consciência**
  - Corpo: *Uma experiência mais profunda para quem desejar ampliar
    sua reflexão por meio dos cinco Pilares da Divícia.*
  - Linha final: *Em breve, este espaço estará disponível para você.*
- **Receber uma nova Voz →** como já está no protótipo — volta para a
  tela de escolha de um novo número/Voz (repete a Travessia).
- **Continuar meu dia →** deveria levar para a Home. **Bug confirmado**
  (ver bloco 8) — hoje o protótipo leva de volta para a escolha de Voz.

## 7. Regras Arquiteturais

- O Hub de Continuidade **não pertence à Home** — são arquiteturas
  diferentes (Navegação vs. Continuidade). A Home consome a
  Continuidade, não é parte dela. (DIV-CON-001, secao 5.2)
- A Continuidade só constrói possibilidades quando a experiência
  alcança um estado que a autoriza — ela "não monitora experiências
  continuamente". Aqui, esse estado é `travessia_concluida`
  (`voz_revelada`). (DIV-CON-001, secao 6)
- A Continuidade consulta a Última Instância, a Trilha e o Patrimônio
  Intelectual para construir possibilidades — nunca decide sozinha,
  nunca produz conhecimento próprio, nunca decide pela mulher.
  (DIV-CON-001, secao 4)
- Nesta fase, sem Lumi e sem Memória Elegível ativas, a construção das
  possibilidades é puramente por regra fixa — não há personalização
  algorítmica.
- **Pendência registrada:** "Explorações (Avulsa)" e "Ritual da
  Consciência (Avulso)" sugerem um mecanismo de compra individual,
  distinto da lógica de módulo ativo/inativo por Trilha que
  DIV-PROT-MODULOS-001 já define. Esse mecanismo ainda não está
  registrado em nenhum documento jurídico ou de módulos — ver
  Pendências.
- Fonte arquitetural: DIV-CON-001 (Continuidade), DIV-EXP-001
  (Navegação) — ambos Documentos Fundadores, lidos integralmente nesta
  revisão.

## 8. Implementação

Já implementado no protótipo da Travessia, como a tela "Próximos
Caminhos" (`CAMINHOS_POR_TRILHA`). Precisa da correção de rótulo do
bloco 6.

**Bug confirmado, com explicação histórica:** o botão "Continuar meu
dia" hoje leva de volta para a escolha de um novo número (repete o
fluxo da Travessia), em vez de levar para a Home. Isso é comportamento
desatualizado, não decisão de arquitetura errada: quando esse
protótipo foi construído, a Home ainda nem existia — não havia lugar
pra onde levar. Agora que a Home está definida, o botão precisa ser
atualizado para levar até ela.

---
---

# ETAPA 12 — Reflexão Guiada

## 1. Objetivo

Permitir que a mulher viva uma Reflexão Guiada — reconhecer um aspecto
de sua experiência através de alternativas legítimas, sem diagnóstico,
recebendo uma devolutiva que amplia sua observação sem interpretá-la.

## 2. Experiência da Mulher

Ela é convidada a um território de observação, responde a uma pergunta
que não induz resposta certa, reconhece a alternativa que mais se
aproxima do que vive, e recebe uma devolutiva construída a partir
dessa escolha — nunca um diagnóstico sobre quem ela é.

## 3. Objetivo de Produto

Registrar a conclusão da Reflexão no momento em que a mulher acessa a
devolutiva correspondente à alternativa escolhida — esse é o ponto de
conclusão da experiência, por definição arquitetural (DIV-MA-012,
B.9). Qualquer aprofundamento posterior (Território de Observação) é
Instância própria, independente, que não altera essa conclusão.

## 4. Orientações de UX

Fluxo interno, na mesma ordem para as 15 Reflexões, sem exceção:

1. **Convite Inicial** — apresenta o propósito da Reflexão e situa a
   mulher no território a ser observado. Mesmo texto já usado como
   prévia no card "Explore Algo Novo" e no botão "Reflexões Guiadas"
   da Home (`Explore-Algo-Novo-Convites-Reflexoes-Guiadas.json`) —
   reaproveitado, sem redação nova.
2. **Pergunta Fundadora** — convida ao reconhecimento, sem induzir
   resposta nem sugerir interpretação.
3. **Alternativas de Reconhecimento** — diferentes formas legítimas de
   viver o mesmo fenômeno; sem caráter diagnóstico ou hierárquico
   (cada Reflexão tem entre 5 e 6 alternativas).
4. **Devolutiva** (ao escolher uma alternativa) — Essência, Frase
   Síntese, Microgesto, Card Compartilhável.
5. **Conclusão** — atingida automaticamente ao acessar a devolutiva.
6. **Território de Observação** (opcional, pós-conclusão) —
   oferecido especificamente quando a mulher não se identifica com
   nenhuma alternativa oferecida, ou se identifica simultaneamente com
   mais de uma (ambivalência genuína) — não é uma 6ª alternativa de
   resposta, é experiência própria, com sua própria devolutiva
   completa (Essência, Frase Síntese, Microgesto, Card).

**Dois pontos de entrada, ambos válidos:** via convite após a
Travessia (Etapa 11) ou acesso direto pela Home (botão "Reflexões
Guiadas", Etapa 09). Quando vem por convite da Voz, a Voz é só
contexto inicial — a mulher pode escolher qualquer uma das 15
Reflexões, não só as 3 sugeridas pela Matriz.

## 5. Direção de Criação

Mesma diretriz das etapas anteriores — seguir os documentos MD de
identidade visual (ver Etapa 09, bloco 5); se a Reflexão selecionada
tiver vínculo com Pilar (via Matriz Voz→Reflexão), considerar a mesma
atenção ao Pilar já aplicada na revelação da Voz (Etapa 10).

## 6. Conteúdo

O Patrimônio v1.0 completo (`DIV-REFLEXOES-GUIADAS-Conteudo-Autoral-Completo-v1.0.md`,
já no repositório) tem, para cada uma das 15 Reflexões: Convite
Inicial, Pergunta Fundadora, 5 a 6 Alternativas de Reconhecimento (com
rótulo), devolutiva completa por alternativa (Essência, Frase
Síntese, Microgesto, Card), devolutiva do Território de Observação, e
a Pergunta de Registro Livre (Trilha Integração).

**Card Compartilhável — layout e texto:**

O Card ocupa todo o protagonismo da tela. Só depois dele, um pequeno
bloco de texto:

> Talvez esta reflexão também encontre lugar na experiência de outra
> mulher.
>
> Se fizer sentido para você, compartilhe este card.
>
> **[Compartilhar Card]**

**Mecanismo de compartilhamento (decidido): Web Share API
(`navigator.share()`).** Um toque abre a bandeja de compartilhamento
nativa do sistema (WhatsApp, Instagram, Mensagens, Salvar imagem — o
que estiver instalado no aparelho aparece ali), sem navegar pra fora
do app. Funciona em iOS Safari e Android Chrome — coerente com PWA
(LAB-TEC-001). Fallback (navegadores sem suporte): botão "Baixar
imagem do Card". Instagram não tem API confiável de postagem direta
pela web — o caminho é ela salvar a imagem e postar manualmente.

Fontes disponíveis, todas já no repositório:
- Conteúdo completo de cada Reflexão: `DIV-REFLEXOES-GUIADAS-Conteudo-Autoral-Completo-v1.0.md`
- Nome e família de cada Reflexão, texto convite, Vozes que sugerem
  cada uma: `Reflexoes-Guiadas-Consolidado.json`
- Matriz Voz → 3 Reflexões sugeridas: `Matriz-Vozes-Reflexoes-referencia.json`

## 7. Regras Arquiteturais

- Anatomia mínima de toda Reflexão Guiada: Convite Inicial, Pergunta
  Fundadora, Alternativas de Reconhecimento, Devolutiva, Território de
  Observação, Conclusão da Experiência. (DIV-MA-012, B.1)
- Os 4 elementos da devolutiva (Essência, Frase Síntese, Microgesto,
  Card Compartilhável) são fixos e universais, independente da
  Trilha. (DIV-MA-012, B.4)
- **Nesta fase (Despertar, sem Lumi ativa):** a devolutiva não recebe
  camada interpretativa da Lumi — só os 4 elementos fixos. A camada
  Lumi é exclusiva de Descoberta/Integração. (DIV-MA-012, B.4;
  DIV-PROT-MODULOS-001)
- **Pergunta de Registro Livre é exclusiva da Trilha Integração** —
  fora de escopo nesta fase. (DIV-MA-012, B.1)
- Alternativas de reconhecimento nunca têm caráter diagnóstico nem
  hierárquico — nenhuma é "mais certa" que outra. (DIV-MA-012, B.3)
- A Essência amplia o campo de observação, nunca interpreta quem a
  mulher é. (DIV-MA-012, B.5)
- O Microgesto nunca resolve um problema nem propõe tarefa — é convite
  de experimentação, preservando o protagonismo da mulher. (DIV-MA-012,
  B.7)
- Conclusão da experiência = acesso à devolutiva. Aprofundamentos
  posteriores (Território de Observação) são Instâncias próprias, não
  alteram nem substituem essa conclusão. (DIV-MA-012, B.9)
- **Confirmado (C.4, C.5):** na Trilha Despertar, a devolutiva é
  composta **integralmente** pelo patrimônio intelectual autoral —
  sem qualquer atuação da Lumi. Os 4 elementos fixos nascem só do
  patrimônio da própria Reflexão, nunca de patrimônio externo.
- A Reflexão pode ser repetida quantas vezes a mulher quiser — cada
  repetição é uma nova Instância, sem limite. (DIV-MA-012, C.9)
- O ponto de entrada (via Travessia ou direto pela Home) não altera a
  natureza arquitetural nem a autonomia da experiência. (DIV-MA-012,
  C.1, C.2)
- Fonte: DIV-MA-012, Blocos A (Natureza Arquitetural), B (Estrutura da
  Experiência) e C (Continuidade) — todos "Ata de Bloco", fechados e
  validados individualmente; a Mesa como um todo (Blocos D e E) ainda
  em aberto, não é Documento Fundador ainda.

## 8. Implementação

Não existe protótipo de Reflexões Guiadas — precisa ser construída do
zero.

---
---

## Anexo — Fora de Escopo Nesta Trilha (registrado, não descartado)

- **Confirmação de Acesso/Pagamento** (DIV-MA-010 Etapa 7) — exclusivo
  Descoberta/Integração; não ativo nesta fase (DIV-PROT-MODULOS-001).
  **Não é aqui que o Registro de Entrada é promovido a Conta** — isso
  ocorre na Etapa 06.5 (Confirmação de Titularidade), logo após a
  Escolha da Trilha, para qualquer Trilha, inclusive Despertar. O que
  ocorre nesta etapa (Confirmação de Acesso/Pagamento) é só a
  **cobrança**, para quem escolhe trilha paga — Promoção e Pagamento
  são capacidades distintas, não a mesma etapa.
  Nesta fase do MVP (Despertar, gratuita), esta etapa nem chega a ser
  acionada.
- **Mapa de Reflexão, 3 Movimentos** (DIV-MA-010 Etapa 9) — exclusivo
  Trilha Integração. Conteúdo extenso já existe no documento de origem,
  não reproduzido aqui por não pertencer ao escopo Despertar.

---

## Pendências consolidadas desta revisão

1. **Pendência Técnica — Parâmetros do Código por E-mail (mecanismo já
   decidido, ver Etapa 06.5, Confirmação de Titularidade).** Mecanismo
   definido: código de confirmação por e-mail, digitado na tela.
   **WhatsApp OTP registrado como candidato forte para versão 2** —
   penetração e confiabilidade de entrega altas no público brasileiro,
   coerente com WhatsApp já cogitado como canal de engajamento em
   LAB-TEC-001.

   **Distinção entre protótipo e implementação real:** a ferramenta
   de materialização usada nesta fase é voltada a design/prototipagem
   — gera interface, sem backend, autenticação ou banco de dados.
   Nesta fase, o código de confirmação deve ser **simulado** no
   protótipo (qualquer código aceito, ou um código fixo), sem tentar
   conectar a um provedor real de e-mail dentro dela. A implementação funcional de verdade
   (envio real, validação real) só faz sentido quando o produto migrar
   para uma ferramenta full-stack (ex.: Lovable) ou para desenvolvimento
   próprio — momento em que a especificação de Engenharia deverá
   definir, no mínimo: provedor de envio (ex.: Resend, já usado para
   e-mail transacional — LAB-TEC-001 — ou serviço de autenticação
   dedicado, ex.: Supabase Auth); tempo de expiração do código; número
   máximo de reenvios; tratamento de código incorreto; política para
   Registros de Entrada nunca promovidos; critérios de segurança e
   prevenção de abuso. Essas definições não podem alterar: o momento de
   criação do Registro de Entrada, o momento de promoção a Conta, o
   conceito de Conta, os estados do Registro/Conta, ou a política de
   continuidade da experiência — todos já fixados neste Blueprint.

---

*Divícia — DIV-PROT-001 — Blueprint de Materialização do MVP — Trilha
Despertar — Jul 2026 — 8 blocos preenchidos por etapa.*
