# DIV-MA-009 — Mesa de Arquitetura do Primeiro Encontro

| Campo | Valor |
|---|---|
| Versão | 1.0 |
| Status | Concluída — aguardando publicação como Documento Fundador e Especificações derivadas |
| Natureza | Mesa de Arquitetura (híbrida — arquitetural e narrativa) |
| Domínio | Produto → Relacionamento com a Mulher |
| Origem | Sessão de Mesa colegiada (Fundadora × Claude × ChatGPT) |
| Resolve | PEND-012 (confirmado: "Como Chega" e "Pesquisa de Chegada" são o mesmo assunto — nomenclatura oficial: Pesquisa de Chegada) |

---

# 1. Objetivo

Esta Mesa define a arquitetura do **Primeiro Encontro** entre a mulher e a Divícia.

O Primeiro Encontro representa o momento em que a mulher estabelece seu primeiro vínculo com o ecossistema Divícia.

Seu propósito não é realizar um cadastro, uma avaliação ou uma apresentação comercial do produto.

Seu propósito é criar as condições para que a mulher compreenda quem é a Divícia, como ela enxerga o autoconhecimento, e de que forma poderá iniciar sua própria jornada.

Somente após esse encontro a Divícia procura compreender o momento vivido pela mulher, para oferecer sua primeira experiência.

Ao término desta Mesa estão definidos os princípios arquiteturais que orientam toda a experiência inicial do aplicativo, desde a primeira tela até a entrada na Home.

---

# 2. Motivação

A Divícia nasce com uma proposta diferente da maioria das plataformas de bem-estar.

Enquanto grande parte dos aplicativos inicia sua relação com a pessoa por meio de diagnósticos, testes ou avaliações (com nota numérica, classificação de perfil, ou narrativa emocional manipuladora vinculada a paywall — padrão identificado em benchmark de mercado durante esta Mesa), a Divícia parte de outro princípio: **antes de procurar compreender a mulher, deseja permitir que ela compreenda a própria Divícia.**

Esse princípio decorre diretamente da Constituição da Inteligência Divícia (Artigos 1 e 2): a Inteligência Divícia não interpreta pessoas, não produz diagnósticos, não ocupa o lugar de sua consciência — cria condições para que cada pessoa reconheça, por si mesma, novos significados para sua própria experiência.

**Nota de benchmark (registrada, não integrada ao Documento Fundador):** apps concorrentes analisados durante esta Mesa (ex.: Cíngulo) combinam teste de perfil emocional com nota numérica diagnóstica, narrativa gamificada de personagem com storytelling manipulador, e ausência de camada gratuita real. Nenhum desses elementos é compatível com a Constituição da Divícia e nenhum foi incorporado a esta arquitetura.

---

# 3. Escopo

Esta Mesa investiga:

- o significado do Primeiro Encontro;
- a narrativa institucional de abertura;
- a arquitetura de apresentação do ecossistema (em nível de princípio, não de especificação completa de cada experiência);
- a Pesquisa de Chegada;
- a apresentação das três formas de iniciar a jornada;
- a transição para a Home.

**Não fazem parte desta Mesa** (permanecem como escopo de Mesas próprias, futuras):

- arquitetura interna da Home;
- arquitetura da Lumi;
- especificação completa de cada experiência autoral (Vozes, Ritual, Diário, Explorações, Jornadas);
- política de assinatura e precificação;
- implementação tecnológica;
- a hipótese sobre a natureza de "Trilha Divícia" vs. "modalidades de percurso" (ver Seção 9 — registrada como hipótese externa, não investigada aqui).

---

# 4. Tese Arquitetural

O Primeiro Encontro é o momento em que a mulher compreende a natureza da Divícia antes que a Divícia procure compreender a natureza dela.

Seu propósito é estabelecer a relação de confiança que sustentará todas as experiências futuras.

Ao final desse encontro, a mulher deve sentir que encontrou um espaço onde poderá caminhar sem julgamentos, sem respostas prontas e no seu próprio ritmo.

---

# 5. Princípio Narrativo

> O Primeiro Encontro revela inicialmente a visão de mundo da Divícia, depois sua arquitetura experiencial e, somente no momento da escolha, apresenta a organização dessa arquitetura em Trilhas.
>
> Os nomes técnicos das Trilhas (Despertar, Descoberta, Integração) não integram a narrativa inicial; surgem apenas quando passam a ter significado para a mulher — no momento em que ela já escolheu como deseja começar.

Este princípio governa a ordem dos Capítulos 1 a 5 abaixo: os Capítulos 1–3 não mencionam os nomes técnicos das Trilhas por escolha deliberada, não apenas por preferência de UX.

---

# 6. Princípio da Dupla Camada de Linguagem

> A arquitetura da Divícia opera com dois vocabulários conscientemente distintos: a linguagem arquitetural (destinada a documentos fundadores, especificações e Núcleos Inteligentes) e a linguagem experiencial (destinada à mulher, na interface).
>
> Um mesmo conceito pode — e deve — ser nomeado de forma diferente em cada camada, sem que isso constitua inconsistência: a inconsistência real ocorreria se a camada arquitetural adotasse termos novos e não rastreáveis aos conceitos já consolidados na Biblioteca.

**Aplicação neste documento:** o conceito de "profundidade da Trilha" (já consolidado na Arquitetura do Produto, Camada 4, e no ADR-005) permanece nomeado como **profundidade** em toda Nota Arquitetural e documento fundador. Na interface voltada à mulher, o mesmo conceito é comunicado como **caminho** ou **forma de começar**, nunca como "profundidade" ou "nível".

---

# 7. Estrutura Narrativa do Primeiro Encontro

## Capítulo 1 — Por que a Divícia existe?

Há momentos em que nossos pensamentos, emoções e atitudes parecem seguir caminhos diferentes.

Nem sempre compreendemos o que sentimos, por que reagimos como reagimos ou o que realmente está nos movendo.

Quando essas partes deixam de conversar entre si, também nos afastamos de nós mesmas.

O autoconhecimento não elimina os desafios da vida. Mas amplia nossa capacidade de atravessá-los com mais clareza, presença e consciência.

A Divícia nasceu para acompanhar cada mulher nesse reencontro consigo mesma, oferecendo experiências que ampliam sua capacidade de reconhecer aquilo que talvez ainda não estivesse visível.

Esse reconhecimento pertence sempre à própria mulher. A Divícia apenas preserva o espaço onde ele pode acontecer, em coerência com sua Constituição.

---

## Capítulo 2 — Como acreditamos que esse caminho acontece?

Acreditamos que o autoconhecimento não acontece de uma única vez.

Ele acontece em movimentos.

Alguns nos aproximam de nós mesmas. Outros nos desafiam. Outros nos convidam a transformar.

Nenhum deles é definitivo. Todos fazem parte do caminho.

Foi dessa compreensão que nasceu a Trilha Divícia — construída sobre cinco movimentos: Presença, Conexão, Aprendizado, Ressignificação, Transformação.

Não como etapas obrigatórias, mas como diferentes formas de caminhar em direção a si mesma.

*(Nota: os nomes técnicos Despertar/Descoberta/Integração não aparecem neste capítulo — ver Princípio Narrativo, Seção 5.)*

---

## Capítulo 3 — Como isso ganha vida?

A Trilha pode ser vivida de diferentes maneiras. Cada experiência revela uma nova forma de percorrê-la.

**🌿 Um caminho mais leve**
Conhecer as Vozes. Iniciar a Travessia. Refletir sobre cada encontro. Sempre disponível.

**🌸 Um caminho de maior presença**
Percorrer Rituais. Explorar novos olhares. Ampliar significados. Conversar com a Lumi.

**✨ Um caminho de construção contínua**
Registrar o próprio caminho. Construir memória. Perceber continuidades. Fortalecer o processo de autoconhecimento ao longo do tempo.

*(Nota: esta é a primeira menção às três formas de vivência — ainda sem nomeá-las tecnicamente, conforme Princípio Narrativo.)*

---

## Capítulo 4 — O que a Divícia precisa conhecer?

Somente após compreender a natureza da Divícia inicia-se a **Pesquisa de Chegada**.

Ela não procura responder:

> Quem é esta mulher?

Ela procura compreender:

> Como ela chega para viver sua primeira experiência?

A pesquisa investiga apenas informações necessárias para orientar seus primeiros passos, preservando sempre seu protagonismo. As categorias de informação, ciclo de vida e política de atualização serão detalhadas na DIV-MA-010 — Mesa de Arquitetura da Pesquisa de Chegada.

---

## Capítulo 5 — Como iniciar sua jornada?

Nenhum caminho começa quando temos todas as respostas.

Ela começa quando aceitamos dar o primeiro passo.

A partir desse momento, a mulher será convidada a escolher como deseja iniciar sua jornada com a Divícia. Cada caminho oferece uma forma diferente de viver essa experiência.

Essa escolha pertence inteiramente a ela. A Divícia apresenta as possibilidades, nunca as impõe.

---

**Nota Arquitetural** *(linguagem arquitetural — não integra o texto exibido à mulher)*

A Trilha escolhida representa a **profundidade de experiência** que a mulher deseja viver — nunca uma segmentação comercial definida pela plataforma.

Por envolverem recursos que ampliam a continuidade e o aprofundamento da experiência (Diário dos Saberes, Memória Experiencial, Interpretação Integrada da Lumi), as trilhas Descoberta e Integração possuem custo associado. A mulher escolhe livremente o quanto deseja se aprofundar desde o início; o valor atribuído é consequência dessa escolha, nunca sua motivação.

**Nota complementar — 19 Jul 2026:** "Diário dos Saberes" constitui exceção confirmada ao Princípio da Dupla Camada de Linguagem (Seção 6) — não é vocabulário arquitetural interno, é nome de marca com identidade visual própria (capa, tagline "Registre. Integre. Transforme."), e já é exibido diretamente à mulher na interface (DIV-MA-010, Etapa 5 — Escolha da Jornada). Essa exceção não enfraquece o princípio geral: nomes de marca com identidade visual própria são, por natureza, vocabulário experiencial desde a origem — diferente de termos como "profundidade", que nasceram como conceito arquitetural e precisam de tradução deliberada para a interface.

> **Princípio Arquitetural — Trilha e Acesso são conceitos independentes**
>
> A Trilha representa uma escolha de experiência. O Acesso representa a forma de disponibilização dessa experiência. Embora se encontrem na materialização do produto, permanecem conceitos arquiteturalmente distintos (ADR-005).

> **A arquitetura não estabelece pré-requisitos entre as trilhas. Cada mulher é livre para iniciar sua jornada pela experiência que fizer mais sentido para ela** — inclusive iniciando diretamente em Integração, sem qualquer vivência prévia em Despertar ou Descoberta.

---

**Texto de interface (linguagem experiencial):**

**🌿 Quero conhecer a Divícia no meu ritmo.**
Conhecer as Vozes. Iniciar minha primeira Travessia. Descobrir esse universo aos poucos.

**🌸 Quero aprofundar meu caminho desde o início.**
Viver Rituais. Explorar novas experiências. Conversar com a Lumi. Ampliar meus olhares.

**✨ Quero construir um caminho contínuo.**
Registrar minha caminhada. Construir memória. Acompanhar minha evolução ao longo do tempo.

Somente após a escolha, discretamente, o nome técnico é revelado:

> *"Você iniciará pela Trilha Despertar."* (ou Descoberta, ou Integração, conforme a escolha)

---

## Capítulo 6 — Nosso compromisso

Na Divícia acreditamos que cada mulher é a maior especialista sobre sua própria vida.

Por isso assumimos alguns compromissos.

Nunca diremos quem você é. Nunca interpretaremos sua história por você. Nunca ofereceremos respostas prontas para perguntas que pertencem apenas à sua experiência.

Respeitaremos o seu tempo, o seu silêncio e a sua liberdade para escolher como deseja caminhar.

Estaremos ao seu lado oferecendo experiências, perguntas, reflexões e caminhos. Mas o significado de cada passo será sempre construído por você.

Porque acreditamos que o reconhecimento pertence sempre à própria mulher. E é apenas esse espaço que a Divícia deseja preservar.

---

# 8. Resultado Arquitetural

Como resultado desta Mesa, fica estabelecido que o Primeiro Encontro culmina na Pesquisa de Chegada, responsável por permitir que a Divícia compreenda o momento vivido pela mulher antes da primeira experiência.

A arquitetura da Pesquisa de Chegada, incluindo suas perguntas, opções de resposta, regras de utilização e fluxo do MVP, será definida na DIV-MA-010 — Mesa de Arquitetura da Pesquisa de Chegada.

---

# 9. Hipótese Arquitetural Identificada (registrada, não investigada nesta Mesa)

Durante a discussão desta Mesa, surgiu a pergunta: **Despertar, Descoberta e Integração são de fato Trilhas independentes, ou são modalidades de percurso de uma única Trilha Divícia?**

Esta é uma pergunta de conhecimento transversal (afeta o ADR-005, a Arquitetura do Produto Camada 4, a Taxonomia da Biblioteca e a nomenclatura oficial já congelada), e não deve ser respondida dentro desta Mesa, conforme o critério de suspensão de decisões transversais (PEND-021).

**Avaliação registrada:** há ceticismo quanto ao mérito prático desta reformulação — o vocabulário atual ("Trilha" = Despertar/Descoberta/Integração) já está consolidado em múltiplos documentos e usado de forma estável há tempo; reformulá-lo exigiria revisão terminológica ampla sem garantia de ganho real. Recomenda-se que esta hipótese amadureça por observação, sem investimento imediato de investigação formal.

Deve ser registrada no Registro de Pendências como **HIP-ARQ-00X** (próximo número disponível da família), não como hipótese local desta Mesa.

---

# 10. Storyboard do Primeiro Encontro

```
Tela 1 → Por que a Divícia existe? (Capítulo 1)
↓
Tela 2 → Como acreditamos que acontece o autoconhecimento? (Capítulo 2)
↓
Tela 3 → Como isso ganha vida? (Capítulo 3 — três caminhos, sem nomes técnicos)
↓
Tela 4 → Nosso compromisso (Capítulo 6 — pode ser intercalado antes da Tela 5)
↓
Tela 5 → Como você gostaria de começar? (Capítulo 5 — escolha + revelação
          discreta do nome técnico da Trilha)
↓
Tela 6 → Pesquisa de Chegada
↓
Tela 7 → Encerramento (privacidade, ausência de julgamento — já existente)
↓
Tela 8 → Primeira Voz / Primeira Home (entrada na Trilha escolhida)
```

**Nota de atualização arquitetural — 13 Jul 2026**

A sequência apresentada originalmente neste Storyboard foi posteriormente refinada pela DIV-MA-010 — Mesa da Pesquisa de Chegada.

Para o Fluxo de Onboarding vigente, prevalece a ordem:

Pesquisa de Chegada → Voz Movimento → Escolha da Trilha.

O conteúdo original permanece preservado como registro da evolução arquitetural.

---

# 11. Critérios de Conclusão

Esta Mesa é considerada concluída com a definição de:

- [x] o significado arquitetural do Primeiro Encontro;
- [x] a narrativa institucional de abertura (Capítulos 1–3, 6);
- [x] o Princípio Narrativo (ordem de revelação: filosofia → arquitetura → organização);
- [x] o Princípio da Dupla Camada de Linguagem;
- [x] a distinção Trilha vs. Acesso, aplicada à tela de escolha;
- [x] a ausência de pré-requisitos entre trilhas;
- [x] o Storyboard completo até a entrada na Home.

---

# 12. Pendências para Documentos Futuros

1. Documento Fundador do Primeiro Encontro (submeter ao Teste da Verdade Permanente antes de congelar — separar, no processo de redação, o que é Nota Arquitetural do que é texto de interface, conforme Seção 6).
2. Especificação de Materialização do Storyboard (Seção 10) para o protótipo/MVP.
3. Abertura da DIV-MA-010 — Mesa de Arquitetura da Pesquisa de Chegada.
4. Registro formal de HIP-ARQ-00X (Seção 9) no Registro de Pendências, com numeração correta.
5. Fechamento formal da PEND-012 no Registro de Pendências, referenciando esta Mesa como resolução.
6. Mesa própria para arquitetura da Home (já planejada pela fundadora como próxima Mesa).
7. Mesa própria (futura, não urgente) para especificação completa de apresentação de cada experiência autoral, caso se prove necessária além do que o Capítulo 3 já cobre em nível de princípio.

---

# 13. Implicações Técnicas

*(Template v1.1 — Congelado)*

**1. Eventos Gerados**
- `primeiro_encontro_iniciado` / `primeiro_encontro_concluido` (a confirmar necessidade em MA-003).
- `trilha_inicial_escolhida` (com identificação da Trilha selecionada no Capítulo 5).
- `pesquisa_chegada_respondida` (por resposta ou por conjunto completo — a definir em especificação futura).

**2. Campos Obrigatórios**
- Respostas da Pesquisa de Chegada (estrutura a ser definida na DIV-MA-010), associadas ao perfil da mulher.
- Trilha inicial escolhida (Despertar/Descoberta/Integração).

**3. Estados Relevantes**
- Primeiro Encontro: não iniciado / em andamento / concluído.

**4. Regras Críticas de Negócio**
- Pesquisa de Chegada ocorre uma única vez, independente da Trilha.
- Nenhum pré-requisito de progressão entre Trilhas.
- Calibração de linguagem da Lumi (via "momento da história") nunca restringe experiências.

**5. O que Nunca Deve Acontecer**
- Exibir nomes técnicos de Trilha antes da escolha da mulher (Capítulo 5).
- Qualquer forma de teste com nota/score diagnóstico (rejeitado nesta Mesa, com base em benchmark).
- Narrativa de personagem com storytelling manipulador vinculado a paywall (rejeitado nesta Mesa).
- Tratar a Pesquisa de Chegada como avaliação ou classificação da mulher.

**6. Dependências**
- ADR-005 (Trilha vs. Modelo de Negócio).
- Arquitetura do Produto e Taxonomia da Biblioteca v1.1 (Camada 4 — Trilhas).
- DIV-CON-001 (Arquitetura da Continuidade) — relação da Pesquisa de Chegada com a Continuidade.
- Mesa futura da Home (Seção 12, item 6).

**7. Impacta**
- REGISTRO-DE-PENDENCIAS.md (fechamento de PEND-012; registro de HIP-ARQ-00X).
- Futuro Documento Fundador do Primeiro Encontro.
- Onboarding do MVP (Storyboard, Seção 10).

---

*Divícia — DIV-MA-009 — Mesa de Arquitetura do Primeiro Encontro — Versão 1.0 — Concluída — Jul 2026*
*Coautoria: Fundadora × Claude × ChatGPT — processo colegiado de revisão.*
