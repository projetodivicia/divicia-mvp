<!--
ARTEFATO DERIVADO
Origem: 03-produto/prototipo/trilha-do-despertar/DIV-PROT-002-Estudo-Boas-Vindas-Instagram-ManyChat-v1.0.md
Versão da origem: v1.0 | commit c47ffa6f76938c4303659ff0502e7dc83922b6f0
Tipo: derivado fiel operacional
Finalidade: orientar a implementação do recurso de boas-vindas do Instagram e das entradas identificadas no MVP
Fonte oficial: Biblioteca Arquitetural da Divícia

Este arquivo é um artefato derivado do patrimônio intelectual da
Divícia. A fonte oficial é exclusivamente o documento publicado na
Biblioteca Arquitetural. Alterações realizadas neste arquivo não
modificam o patrimônio institucional e poderão ser sobrescritas por
futuras sincronizações.
-->

# DIV-PROT-002

# Estudo do Recurso de Boas-vindas no Instagram e Entrada no App Divícia

| Campo | Valor |
|---|---|
| Versão | v1.0 |
| Data | 04/09/2026 |
| Status | Estudo aplicado ao MVP; implantação pendente de elegibilidade técnica, URL pública e instrumentação |
| Natureza | Benchmark aplicado, tese de produto, especificação de experiência e orientação técnica |
| Domínio | 03 · Produto |
| Local na Biblioteca | `03-produto/prototipo/trilha-do-despertar/` |
| Benchmark de origem | Recurso de boas-vindas observado no Instagram do The Skin Deep |
| Canal | Instagram Direct e link da bio |
| Ferramenta recomendada | ManyChat, condicionada à elegibilidade da conta pela Meta |
| Relação com o app | ManyChat externo ao app; conexão realizada por URL pública identificada |
| Documento relacionado | `DIV-PROT-001-Blueprint-Materializacao-MVP-Trilha-Despertar.md` |

---

## 1. Objetivo

Este documento registra o estudo conceitual e técnico do recurso de
boas-vindas observado no perfil do Instagram do The Skin Deep e sua possível
aplicação à Divícia.

O objetivo não é copiar a mensagem, o tom ou a lógica comercial do benchmark.
O objetivo é compreender o mecanismo, identificar a oportunidade para a
Divícia e especificar uma primeira implantação coerente com:

- a experiência da mulher;
- o posicionamento da Divícia;
- a Trilha Despertar;
- a arquitetura do MVP;
- a privacidade dos dados;
- a necessidade de medir aquisição e ativação sem invadir a experiência
  reflexiva.

Este documento também diferencia explicitamente:

- decisões já tomadas;
- benchmark observado;
- inferências técnicas;
- hipóteses a testar;
- lacunas ainda não resolvidas;
- premissas a validar no Real.

---

## 2. Síntese executiva

O benchmark revelou uma oportunidade de transformar o ato de seguir a Divícia
em uma primeira passagem para o ecossistema, sem reduzir essa passagem a uma
oferta comercial.

Na experiência observada, uma nova seguidora recebe uma mensagem automática de
boas-vindas. A mensagem reconhece a possível origem do interesse, oferece um
pequeno presente e pede uma manifestação simples antes de entregá-lo.

Para a Divícia, o valor estratégico do recurso não está em automatizar um
“olá”. Está em criar uma continuidade coerente entre dois ambientes:

1. o Instagram desperta interesse, reconhecimento e curiosidade;
2. o app acolhe, apresenta a Divícia e conduz a mulher até sua primeira
   experiência.

A recomendação para o MVP é:

- conectar o Instagram profissional da Divícia ao ManyChat;
- usar o recurso **Follow to DM**, se a Meta declarar o perfil elegível;
- enviar uma primeira mensagem de acolhimento com botão de resposta;
- entregar o link do app somente após a manifestação de interesse;
- disponibilizar também o link do app na bio;
- usar URLs identificadas para diferenciar `instagram_dm` e `instagram_bio`;
- não instalar ManyChat no app;
- não compartilhar com ManyChat respostas reflexivas ou dados sensíveis;
- validar o fluxo inicialmente com uma amostra real antes de ampliá-lo.

---

## 3. Evidência observada no benchmark

### 3.1 Perfil observado

**The Skin Deep**, perfil `@the_skindeep` no Instagram.

### 3.2 Sequência observada

Após começar a seguir o perfil, a nova seguidora recebeu uma mensagem privada
com os seguintes elementos:

1. acolhimento imediato;
2. reconhecimento de como ela possivelmente encontrou a marca;
3. explicação curta do que a marca produz;
4. convite para experimentar algo;
5. promessa de um pequeno presente de boas-vindas;
6. botão de confirmação antes da entrega.

### 3.3 O que o benchmark faz bem

- aproveita um momento de interesse já existente;
- reduz a distância entre conteúdo observado e experiência da marca;
- pede uma ação pequena e voluntária;
- não entrega um texto institucional longo;
- cria continuidade sem exigir pesquisa ativa da seguidora;
- transforma audiência em conversa;
- oferece valor antes de solicitar uma conversão maior.

### 3.4 O que não devemos copiar

- a redação e a estrutura literal da mensagem;
- o uso de “presente” quando o que entregaremos é a própria entrada no app;
- o tom promocional ou excessivamente entusiasmado;
- a tentativa de capturar e-mail, telefone ou outro dado dentro do Instagram;
- sequências longas de mensagens;
- pressão para compra, assinatura ou escolha de plano;
- perguntas reflexivas íntimas dentro do Direct;
- qualquer promessa de personalização que ainda não esteja materializada.

### 3.5 Limite da evidência

A imagem observada permite afirmar que houve uma mensagem de boas-vindas após o
início do acompanhamento do perfil. Ela não permite comprovar qual ferramenta
foi utilizada.

O funcionamento coincide com o recurso **Follow to DM** do ManyChat. Portanto,
a identificação da ferramenta é uma **inferência técnica apoiada pelo
funcionamento documentado**, e não um fato confirmado sobre a operação do The
Skin Deep.

---

## 4. Tese conceitual para a Divícia

### 4.1 A função do Instagram

O Instagram não precisa explicar toda a Divícia. Sua função nesse fluxo é:

- reconhecer a chegada;
- acolher sem presumir necessidade;
- despertar curiosidade;
- oferecer uma passagem voluntária para o ambiente proprietário.

### 4.2 A função do app

O app é o ambiente adequado para:

- apresentar a visão de mundo da Divícia;
- explicar como o autoconhecimento ganha forma na plataforma;
- permitir que a mulher se identifique;
- conduzir a Pesquisa de Chegada;
- apresentar os caminhos possíveis;
- permitir a escolha da Trilha;
- oferecer a primeira experiência.

O Instagram abre a porta. O app preserva e conduz a experiência.

### 4.3 Por que a oportunidade é coerente

A aplicação é coerente porque:

- parte de uma ação voluntária da mulher, que decidiu seguir o perfil;
- não interpreta por que ela chegou;
- não diagnostica seu momento;
- não captura respostas reflexivas em um ambiente de terceiros;
- oferece escolha antes de continuidade;
- cria uma passagem para a Trilha Despertar;
- permite medir aquisição e ativação sem medir intimidade.

### 4.4 O risco conceitual

Uma mensagem automática pode ser percebida como invasiva, artificial ou
comercial. Esse risco aumenta quando:

- chega imediatamente após o follow;
- presume uma dor;
- usa intimidade não autorizada;
- oferece venda antes de vínculo;
- contém texto excessivo;
- envia novas mensagens sem manifestação da mulher.

Por isso, a Divícia deve aplicar automação como **gesto de acolhimento com
limites**, não como funil agressivo.

---

## 5. Princípios da experiência de boas-vindas

1. **Reconhecer sem interpretar.** A mensagem reconhece a chegada, mas não
   presume o que a mulher sente, busca ou precisa.
2. **Convidar sem pressionar.** O próximo passo depende de uma escolha simples.
3. **Ser breve.** A profundidade pertence ao app, não ao Direct.
4. **Entregar antes de vender.** O primeiro destino é conhecer a Divícia.
5. **Preservar o silêncio.** A ausência de resposta não gera cobrança.
6. **Não duplicar experiências.** Quem já faz parte deve poder entrar e
   continuar de onde parou.
7. **Medir movimento, não intimidade.** Medimos entrada e continuidade, nunca o
   conteúdo reflexivo.
8. **Manter a mulher no centro.** A automação oferece uma possibilidade; a
   decisão pertence a ela.

---

## 6. Arquitetura da solução

### 6.1 Arquitetura do MVP

```text
Instagram → ManyChat → URL pública identificada → App Divícia
```

O ManyChat permanece fora do app. Sua função é:

- receber o gatilho permitido pelo Instagram;
- enviar a primeira mensagem;
- registrar a manifestação no botão;
- enviar a segunda mensagem com a URL.

O app não precisa, no MVP:

- instalar SDK do ManyChat;
- consultar a API do ManyChat;
- receber webhook do ManyChat;
- enviar dados pessoais ou reflexivos ao ManyChat;
- conhecer o perfil do Instagram da mulher.

### 6.2 Duas portas de entrada

| Porta | Gatilho | Intermediação | Identificador recomendado |
|---|---|---|---|
| Direct | Novo follow e manifestação no botão | ManyChat | `instagram_dm` |
| Bio | Clique voluntário no perfil | Nenhuma | `instagram_bio` |

As duas portas podem abrir a mesma apresentação. A diferença precisa ser
preservada apenas para análise de origem.

### 6.3 Fluxo funcional

#### Entrada pelo Direct

1. mulher começa a seguir a Divícia;
2. ManyChat aguarda o intervalo definido;
3. primeira mensagem é enviada;
4. mulher toca em **Quero conhecer**;
5. a interação autoriza a continuidade da conversa;
6. segunda mensagem é enviada;
7. mulher toca em **Conhecer a Divícia**;
8. app abre e aplica a lógica de estado.

#### Entrada pela bio

1. mulher visita o perfil;
2. toca no link da bio;
3. app abre e aplica a mesma lógica de estado;
4. origem é registrada como `instagram_bio`.

### 6.4 Lógica de estado no app

| Estado reconhecido | Comportamento esperado |
|---|---|
| Visitante nova | Iniciar na T01, Apresentação da Divícia |
| Registro de Entrada em andamento | Retomar o ponto permitido pela arquitetura vigente |
| Mulher autenticada | Encaminhar para a Home |
| Mulher já vinculada, mas não autenticada | Oferecer **Já faço parte da Divícia** |

O mecanismo exato de autenticação continua pertencendo à Engenharia, conforme
o Blueprint do MVP.

---

## 7. Dupla camada de linguagem

### 7.1 Linguagem técnica

Na arquitetura interna, **Conta** continua sendo o nome correto da identidade
persistente da mulher na plataforma. Esse conceito não deve ser eliminado do
código, dos eventos técnicos ou da documentação arquitetural.

### 7.2 Linguagem de interface

Na experiência da mulher, “conta” comunica uma relação técnica e transacional.
A decisão de microcopy é utilizar linguagem de pertencimento sem sacrificar
clareza.

| Contexto | Linguagem recomendada |
|---|---|
| Atalho na apresentação | **Já faço parte da Divícia** |
| Ação final de autenticação | **Entrar** |
| Acolhimento no retorno | **Que bom ter você de volta.** |
| Orientação | **Entre para continuar sua experiência.** |
| Área pessoal, se houver | **Meu espaço**, condicionado à validação de UX |

### 7.3 Impacto documental identificado

O `DIV-PROT-001-Blueprint-Materializacao-MVP-Trilha-Despertar.md` ainda utiliza
“Já tenho uma conta” como texto de interface.

Este estudo registra a mudança para **“Já faço parte da Divícia”**, mas não
altera retroativamente o Blueprint. A atualização do documento de origem deve
ser feita por ação controlada, preservando a distinção entre:

- **Conta**, conceito técnico;
- **Já faço parte da Divícia**, linguagem apresentada à mulher.

---

## 8. Microcopy proposta

### 8.1 Primeira mensagem

> Que bom ter você por aqui. 🤍
>
> Talvez você tenha chegado até a Divícia por uma história, uma reflexão ou
> pela experiência de outra mulher.
>
> Gostaria de conhecer um pouco mais sobre o que estamos construindo?
>
> **[Quero conhecer]**

### 8.2 Segunda mensagem

> Aqui está o seu convite para conhecer a Divícia. 🤍
>
> Ao entrar, você será conduzida por uma breve experiência para conhecer nosso
> universo e encontrar a trilha que mais conversa com o seu momento.
>
> Se você já faz parte da Divícia, é só entrar e continuar de onde parou.
>
> **[Conhecer a Divícia]**

### 8.3 Regras de microcopy

- o primeiro botão é uma resposta dentro do Instagram, não uma URL;
- o segundo botão contém o link do app;
- não usar “teste”, “diagnóstico”, “perfil” ou promessa de resultado;
- não usar a palavra “conta” na comunicação apresentada à mulher;
- não citar planos pagos na primeira passagem;
- não enviar lembrete no MVP se a mulher não responder;
- não incluir mais de uma pergunta por mensagem;
- não usar nome próprio capturado automaticamente na primeira versão;
- não simular uma mensagem escrita manualmente por Andrea ou outra pessoa.

---

## 9. Funcionamento técnico do ManyChat

### 9.1 Recurso recomendado

**Follow to DM, Say Hi to New Followers**, do ManyChat.

Na documentação consultada em 04/09/2026, o recurso:

- estava em beta;
- dependia de elegibilidade determinada pela Meta;
- não estava liberado para todas as contas;
- exigia conexão pelo fluxo unificado de Instagram;
- podia ser usado por contas Free e Pro quando elegíveis;
- permitia, no plano gratuito, uma mensagem de abertura e uma mensagem
  subsequente com link;
- permitia atraso configurável entre cinco e dez minutos;
- exigia que a pessoa interagisse com uma resposta ou botão comum antes da
  continuação;
- abria uma janela de 24 horas após essa interação;
- executava o gatilho apenas uma vez por seguidora;
- estava sujeito ao limite da Meta de uma mensagem Follow to DM por pessoa por
  semana, considerando diferentes perfis que utilizem o recurso.

### 9.2 Elegibilidade

A contratação de um plano pago não garante acesso ao recurso. A elegibilidade
é controlada pela Meta e pode mudar.

Por isso, **Follow to DM disponível para o Instagram da Divícia** é uma lacuna
técnica a verificar, e não uma capacidade confirmada.

### 9.3 Pré-requisitos operacionais

- perfil profissional do Instagram;
- conexão adequada com o ambiente Meta;
- conexão do Instagram ao ManyChat pelo fluxo recomendado via Meta;
- permissão de acesso às mensagens para ferramentas conectadas;
- pessoa responsável pela administração do ManyChat;
- URL pública do app pronta e validada.

---

## 10. URLs e identificação de origem

### 10.1 URL para o Direct

```text
https://app.divicia.com.br/?utm_source=instagram&utm_medium=dm&utm_campaign=boas_vindas&utm_content=follow_to_dm
```

### 10.2 URL para a bio

```text
https://app.divicia.com.br/?utm_source=instagram&utm_medium=bio&utm_campaign=perfil_divicia
```

Os domínios acima são exemplos de arquitetura. O domínio final ainda precisa
ser confirmado.

### 10.3 Regras para os parâmetros

- usar letras minúsculas;
- não inserir nome, e-mail, identificador do Instagram ou dado pessoal;
- manter nomenclatura estável;
- preservar a origem durante o onboarding;
- não sobrescrever a primeira origem sem uma regra analítica explícita;
- definir separadamente `first_touch` e `last_touch` apenas se a arquitetura
  analítica do produto assim determinar.

### 10.4 Link de marca

Em fase posterior, a Divícia poderá utilizar links próprios e legíveis, como:

```text
https://divicia.com.br/convite
https://divicia.com.br/instagram
```

Esses endereços podem redirecionar para o app preservando a identificação de
origem. Para o MVP, o redirecionamento não é obrigatório se a URL pública do
app já for confiável e estável.

---

## 11. Instrumentação analítica

### 11.1 Princípio

Medimos passagem, ativação e continuidade. Não medimos o conteúdo íntimo da
experiência.

### 11.2 Eventos mínimos no app

| Evento | Finalidade |
|---|---|
| `entrada_no_app` | Registrar abertura da porta de entrada |
| `apresentacao_iniciada` | Confirmar início da T01 |
| `identificacao_concluida` | Medir avanço no Primeiro Encontro |
| `escolha_do_caminho_concluida` | Medir conclusão da escolha disponível |
| `trilha_iniciada` | Registrar ativação da Trilha |
| `primeira_experiencia_iniciada` | Registrar ativação comportamental |
| `primeira_experiencia_concluida` | Registrar conclusão da primeira experiência |

### 11.3 Propriedades permitidas

- `entry_source`: `instagram_dm`, `instagram_bio`, `direct`, `other`;
- `utm_source`;
- `utm_medium`;
- `utm_campaign`;
- `utm_content`;
- identificador técnico pseudonimizado, se já aprovado pela arquitetura;
- data e hora do evento;
- etapa técnica do fluxo.

### 11.4 Propriedades proibidas nessa integração

- texto escrito pela mulher;
- resposta reflexiva;
- escolha íntima em campo aberto;
- interpretação da Lumi;
- conteúdo do Diário dos Saberes;
- conteúdo de Ritual, Voz, Reflexão ou Exploração associado nominalmente;
- informação sensível usada para segmentação no Instagram ou no ManyChat.

### 11.5 Funil de acompanhamento

1. novas seguidoras potencialmente elegíveis;
2. mensagens de abertura enviadas;
3. manifestações em **Quero conhecer**;
4. segundas mensagens entregues;
5. cliques em **Conhecer a Divícia**;
6. entradas no app via `instagram_dm`;
7. entradas no app via `instagram_bio`;
8. identificações concluídas;
9. escolhas concluídas;
10. primeiras experiências iniciadas;
11. primeiras experiências concluídas.

Não há metas numéricas homologadas para esse funil. A primeira rodada deve
construir a linha de base do Real.

---

## 12. Privacidade, consentimento e limites

### 12.1 Separação dos ambientes

O Direct é ambiente de acolhimento e passagem. O app é ambiente da experiência
reflexiva.

### 12.2 Dados no ManyChat

O ManyChat pode armazenar informações de contato e histórico de conversa de
acordo com sua operação. Portanto:

- não devemos solicitar dados adicionais no fluxo inicial;
- não devemos levar perguntas reflexivas para o Direct;
- devemos definir responsável interno por solicitações de exclusão;
- a Política de Privacidade deverá mencionar ferramentas terceiras relevantes
  quando a revisão jurídica determinar;
- prazos de retenção e base legal precisam de validação jurídica.

### 12.3 Consentimento de continuidade

O toque em **Quero conhecer** permite a continuação operacional da conversa
dentro das regras da plataforma. Isso não equivale automaticamente a
consentimento para campanhas futuras, e-mail marketing, perfilamento ou
tratamento ampliado de dados.

### 12.4 Ausência de resposta

No MVP, a ausência de resposta encerra silenciosamente o fluxo. Não haverá
cobrança, interpretação de ausência ou insistência automática.

---

## 13. Plano de implantação

### Fase 0. Preparação

1. confirmar que o Instagram da Divícia é profissional;
2. confirmar o Meta Business Portfolio e as permissões administrativas;
3. criar ou configurar o ManyChat;
4. conectar o Instagram pelo fluxo recomendado via Meta;
5. verificar se **Follow to DM** está disponível;
6. confirmar a URL pública final do app;
7. confirmar a ferramenta analítica do app;
8. implementar leitura e persistência dos parâmetros;
9. validar a lógica de retorno e autenticação.

### Fase 1. Configuração do fluxo

1. selecionar **Say Hi to New Followers**;
2. configurar atraso inicial entre cinco e dez minutos como hipótese;
3. inserir a primeira mensagem;
4. criar botão comum **Quero conhecer**;
5. inserir a segunda mensagem;
6. incluir o link identificado no botão **Conhecer a Divícia**;
7. não configurar lembrete automático;
8. salvar o fluxo sem publicar até concluir a validação.

### Fase 2. Link da bio

1. inserir o link identificado da bio;
2. garantir que o texto do perfil esclareça a possibilidade de conhecer a
   Divícia;
3. testar o link dentro do navegador do Instagram;
4. testar visitante nova, retorno em andamento, autenticada e não autenticada.

### Fase 3. Qualidade

1. usar o modo de pré-visualização do ManyChat;
2. testar com perfis que ainda não sejam contatos do fluxo;
3. validar Android e iPhone;
4. validar navegadores internos e externos;
5. validar parâmetros de Direct e bio;
6. verificar se respostas reflexivas não chegam ao analytics;
7. verificar acessibilidade e legibilidade dos botões;
8. revisar ortografia e tom;
9. validar comportamento quando o app estiver indisponível;
10. documentar resultado dos testes.

### Fase 4. Teste controlado no Real

1. publicar o fluxo;
2. acompanhar as primeiras 50 a 100 novas seguidoras elegíveis;
3. observar entrega, resposta, clique e entrada no app;
4. coletar manifestações espontâneas de desconforto ou acolhimento;
5. revisar o fluxo sem alterar simultaneamente várias variáveis;
6. registrar aprendizados antes de ampliar a automação.

### Fase 5. Evolução

Somente após a validação:

- testar variações de microcopy;
- comparar tempos de envio;
- segmentar por campanhas de origem;
- avaliar CRM;
- avaliar automações de comentários, Stories e compartilhamentos;
- avaliar relacionamento posterior com consentimento específico.

---

## 14. Plano alternativo se Follow to DM não estiver disponível

Se a Meta não declarar o perfil elegível, a Divícia não deve simular o recurso
por métodos não autorizados.

A alternativa recomendada é:

1. publicar conteúdo ou Reel com convite explícito;
2. convidar a mulher a comentar uma palavra, por exemplo **DIVÍCIA**;
3. usar automação de comentário para mensagem privada;
4. enviar botão comum **Quero conhecer**;
5. após a manifestação, entregar o link do app;
6. manter o link direto disponível na bio.

Esse fluxo exige uma ação mais explícita da mulher, mas preserva a mesma tese:
conteúdo no Instagram, passagem voluntária e experiência no app.

---

## 15. Responsabilidades

| Frente | Responsabilidade |
|---|---|
| Produto | Preservar coerência do percurso e critérios de sucesso |
| Marketing | Configurar campanha, mensagens, origem e leitura do funil |
| Desenvolvimento | URL pública, roteamento, persistência e eventos |
| Conteúdo/Marca | Microcopy e fidelidade à linguagem da Divícia |
| Privacidade/Jurídico | Base legal, transparência, retenção e fornecedores |
| Atendimento | Responder quando a mulher transformar automação em conversa real |

A automação não substitui presença humana quando houver pergunta, dúvida ou
pedido de ajuda.

---

## 16. Decisões registradas

1. Adotar a tese de boas-vindas como passagem do Instagram para o app.
2. Usar o app como destino direto, sem landing page intermediária no MVP.
3. Disponibilizar entrada tanto pelo Direct quanto pela bio.
4. Usar ManyChat externamente, sem SDK ou integração interna no app.
5. Enviar o link somente na segunda mensagem do fluxo de Direct.
6. Usar **Quero conhecer** como manifestação inicial.
7. Usar **Conhecer a Divícia** como CTA do link.
8. Usar **Já faço parte da Divícia** na interface no lugar de “Já tenho uma
   conta”.
9. Manter **Conta** como conceito técnico da arquitetura.
10. Identificar separadamente acessos `instagram_dm` e `instagram_bio`.
11. Não enviar respostas reflexivas ou dados sensíveis ao ManyChat.
12. Não adicionar CRM nem automações ampliadas no MVP.

---

## 17. Hipóteses

1. A mensagem será percebida como acolhimento, não como invasão.
2. A manifestação em **Quero conhecer** criará curiosidade suficiente para a
   segunda etapa.
3. O link direto para o app produzirá menos fricção do que uma landing page.
4. A apresentação da Divícia será suficiente para contextualizar quem chega
   pela bio ou pelo Direct.
5. O intervalo de cinco a dez minutos parecerá mais natural do que o envio
   imediato.
6. **Já faço parte da Divícia** manterá compreensão funcional e ampliará a
   percepção de pertencimento.
7. A bio e o Direct atrairão mulheres com disposições diferentes para avançar.

---

## 18. Lacunas

1. O perfil do Instagram é profissional e está corretamente conectado à Meta?
2. A Divícia possui Meta Business Portfolio configurado e sob controle de quem?
3. O perfil é elegível para Follow to DM?
4. Qual será a URL pública e definitiva do app?
5. Qual ferramenta de analytics será utilizada?
6. Como o app preservará `first_touch` e `last_touch`?
7. Qual será a regra técnica de retomada de onboarding?
8. Quem administrará o ManyChat e responderá às conversas reais?
9. Qual será a política de retenção dos dados no fornecedor?
10. A Política de Privacidade atual contempla esse fornecedor e essa finalidade?
11. Qual comportamento será apresentado se o app estiver indisponível?
12. O plano gratuito atenderá ao volume e às necessidades quando o perfil for
    declarado elegível?

Nenhuma dessas lacunas deve ser preenchida por suposição.

---

## 19. Premissas a validar no Real

1. taxa de entrega da primeira mensagem;
2. taxa de manifestação em **Quero conhecer**;
3. taxa de entrega da segunda mensagem;
4. taxa de clique em **Conhecer a Divícia**;
5. diferença entre entrada por Direct e por bio;
6. avanço da T01 para Identificação;
7. conclusão da Pesquisa de Chegada;
8. escolha do caminho;
9. início e conclusão da primeira experiência;
10. relatos espontâneos sobre acolhimento, artificialidade ou invasão;
11. incidência de dúvidas humanas após a mensagem automática;
12. estabilidade técnica do recurso em beta.

Esses dados devem construir a primeira linha de base. Não há benchmark externo
suficiente para homologar metas da Divícia antes da observação do Real.

---

## 20. Critérios de aceite para o MVP

- [ ] Instagram profissional confirmado.
- [ ] Conexão via Meta validada.
- [ ] Elegibilidade Follow to DM verificada.
- [ ] URL pública do app confirmada.
- [ ] Link do Direct testado.
- [ ] Link da bio testado.
- [ ] Origem preservada durante o onboarding.
- [ ] Visitante nova inicia na T01.
- [ ] Mulher autenticada chega à Home.
- [ ] Retorno em andamento respeita a regra arquitetural vigente.
- [ ] **Já faço parte da Divícia** possui destino funcional.
- [ ] Eventos mínimos estão disponíveis.
- [ ] Nenhum conteúdo reflexivo chega ao ManyChat ou ao analytics externo.
- [ ] Mensagens aprovadas por Produto, Marca e Marketing.
- [ ] Testes em Android e iPhone concluídos.
- [ ] Plano alternativo documentado.

---

## 21. O que este documento não autoriza

Este documento não autoriza:

- instalação automática de qualquer fornecedor;
- contratação de plano pago;
- publicação imediata do fluxo;
- alteração silenciosa do Blueprint do MVP;
- coleta de dados adicionais;
- integração com CRM;
- remarketing baseado em respostas reflexivas;
- automação de mensagens posteriores;
- uso do nome da mulher para simular uma conversa pessoal;
- alteração de Termos de Uso ou Política de Privacidade sem revisão adequada.

---

## 22. Referências externas consultadas

1. ManyChat Help. **Follow to DM on Instagram: Say Hi to New Followers
   [BETA]**. Consulta em 04/09/2026.  
   <https://help.manychat.com/hc/en-us/articles/23096654243740-Follow-to-DM-on-Instagram-Say-Hi-to-New-Followers-BETA>

2. ManyChat Help. **How to connect Instagram to ManyChat**. Consulta em
   04/09/2026.  
   <https://help.manychat.com/hc/en-us/articles/14281290924444-How-to-connect-Instagram-to-Manychat>

3. ManyChat Help. **Instagram automation troubleshooting**. Consulta em
   04/09/2026.  
   <https://help.manychat.com/hc/en-us/articles/14281308423452-Instagram-automation-troubleshooting>

4. ManyChat Help. **Instagram Post and Reel Comments trigger**. Consulta em
   04/09/2026.  
   <https://help.manychat.com/hc/en-us/articles/14281316989724-Instagram-Post-and-Reel-Comments-trigger>

5. ManyChat Help. **Managing User Data / GDPR Compliance**. Consulta em
   04/09/2026.  
   <https://help.manychat.com/hc/en-us/articles/14281070595100-Managing-User-Data-GDPR-Compliance>

6. Google Analytics Help. **URL builders: Collect campaign data with custom
   URLs**. Consulta em 04/09/2026.  
   <https://support.google.com/analytics/answer/10917952>

---

## 23. Próxima ação mínima recomendada

1. executar a preparação técnica de URL, roteamento e instrumentação no
   protótipo;
2. verificar a elegibilidade do Instagram no ManyChat;
3. resolver as lacunas de domínio, analytics e responsabilidade operacional;
4. atualizar de forma controlada a microcopy do Blueprint;
5. configurar o fluxo em modo de rascunho;
6. publicar somente quando o link do app estiver pronto e validado.

