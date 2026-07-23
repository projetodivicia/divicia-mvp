# Nota Arquitetural — Registro de Entrada

**Status:** Publicada — validada pela Fundadora nesta revisão
(equivalente a aprovação de Mesa)
**Domínio:** 03 · Produto — Primeiro Encontro
**Origem:** Discussão de arquitetura, jul/2026 (Fundadora + Mesa Arquitetural),
com contribuição de revisão colegiada (chat)
**Relaciona-se com:** DIV-MA-009 (Primeiro Encontro), DIV-MA-010 (Pesquisa de
Chegada), DIV-MA-002 (Instância de Experiência), DIV-PROT-001 (Blueprint),
DIV-PROT-CONFORMIDADE-JURIDICA-001, DIV-PROT-JURIDICO-001, DIV-PROT-MODULOS-001

---

## Por que este conceito existe

A chegada da mulher à Divícia — identificação, respostas da Pesquisa de
Chegada, Voz Movimento, escolha da Trilha — precisa ser registrada desde
o primeiro instante, antes de existir qualquer confirmação de que ela é
titular do e-mail informado.

Esse registro não é uma Instância de Experiência (DIV-MA-002): não há
Voz revelada, não há Território, não há Pilar ou Movimento envolvidos —
é identificação e trânsito, não encontro com o Patrimônio. Tratar esse
momento como Instância forçaria exceções num conceito já publicado e
poluiria a leitura longitudinal (Janela de Observação, Arco de
Experiência) com dados de natureza diferente.

Também não é, ainda, uma Conta — chamar de "Conta" algo que pode nunca
vir a se confirmar seria impreciso.

## Princípio

O **Registro de Entrada** é a estrutura que existe entre o momento em
que a mulher informa seus dados (Etapa 02, Identificação) e o momento em
que sua titularidade sobre o e-mail é confirmada.

Ele nasce na submissão da Etapa 02 e armazena, desde então: identificador
interno único; nome de tratamento; pronome (quando informado); e-mail
informado (editável); respostas da Pesquisa de Chegada; Trilha
escolhida; aceite jurídico associado; e metadados de criação.

O Registro de Entrada não é uma experiência, não é Memória Experiencial,
não é Instância de Experiência, e não é, ainda, uma Conta.

## Promoção a Conta

Quando a titularidade do e-mail é confirmada — na Etapa 06.5
(Confirmação de Titularidade), que ocorre logo após a Escolha da
Trilha — o Registro de Entrada é **promovido** a Conta.

Não há migração de dados: é o mesmo identificador interno, a mesma
linha, que passa a ser institucionalmente reconhecida como Conta a
partir desse momento. Tudo que já pertencia ao Registro de Entrada
(respostas, Trilha escolhida, aceite jurídico) passa a pertencer à
Conta automaticamente, por continuidade do mesmo identificador — não
por associação posterior.

A partir da promoção, aplica-se o Princípio da Conta da Mulher já
registrado no Blueprint: a Conta é a identidade persistente da mulher;
toda Instância de Experiência futura pertence a essa Conta.

**O Registro de Entrada não depende do dispositivo.** A pergunta
arquitetural correta não é "como recuperar em outro aparelho" — é
"como confirmar que quem voltou é realmente a titular daquele
Registro". O Registro não está associado ao navegador ou dispositivo;
está associado à identidade que será confirmada no momento da
promoção, ou antes dela, pelo fluxo de retorno ("Já tenho uma conta",
ver Blueprint, Etapa 01).

**A plataforma nunca informa se existe ou não uma Conta ou Registro de
Entrada apenas com base no e-mail informado.** Quando houver
necessidade de recuperação de acesso ou continuidade, a confirmação da
titularidade deve ocorrer antes da revelação de qualquer informação
relacionada à existência daquele Registro ou Conta — evita que o
e-mail sozinho vire vetor de descoberta sobre quem já usa a
plataforma.

## O que isso torna possível

- **Correção de e-mail sem perda de dado.** Se o e-mail informado na
  Etapa 02 estiver incorreto, a correção no checkpoint atualiza o mesmo
  Registro de Entrada — nenhuma resposta é perdida, porque nunca esteve
  amarrada ao texto do e-mail, apenas ao identificador interno.
- **Relatório de abandono com e-mail disponível.** É possível identificar
  Registros de Entrada nunca promovidos a Conta, com o e-mail informado
  e o ponto exato em que a mulher parou (quantas perguntas da Pesquisa
  de Chegada respondeu, se chegou a escolher Trilha) — permitindo
  comunicação de continuidade. **Nota de precisão (corrigida):** esta
  finalidade ainda não consta em DIV-PROT-JURIDICO-001 §3.5 — é proposta
  nova, distinta de marketing, pendente de inclusão formal como décima
  segunda entrada na tabela de finalidades (ex.: "Recuperação de
  cadastro incompleto"). Não citar §3.5 como fonte já existente até essa
  inclusão ser feita.
- **A primeira experiência da mulher existe independentemente da
  Conta.** Ela vive a chegada antes de decidir formalizar sua relação
  com a plataforma — a Conta não cria essa experiência, apenas lhe dá
  continuidade a partir da promoção.

## O que isso não muda

- O e-mail nunca é usado como chave de associação entre Registro de
  Entrada/Conta e as respostas — a associação é sempre por identificador
  interno (reforça DIV-PROT-CONFORMIDADE-JURIDICA-001 §5).
- O mecanismo técnico de confirmação de titularidade (e-mail, login
  social, ou outro) permanece decisão de Engenharia, não afetada por
  esta Nota.
- Pagamento não promove a Conta. Escolha de Trilha não promove a Conta.
  Somente a confirmação de titularidade promove.

## Abrangência desta Nota

Esta Nota Arquitetural formaliza exclusivamente o conceito de Registro
de Entrada e sua promoção a Conta. Ela não define mecanismos de
autenticação, política de retenção, regras de segurança, política de
sessões ou decisões de Engenharia — essas permanecem em especificação
técnica própria (ver Blueprint, Pendência Técnica), sem afetar os
princípios registrados aqui.

## Pendências

- Regra de retenção/expiração de Registros de Entrada nunca promovidos —
  pendência de Engenharia, mesma natureza da já registrada no Blueprint
  para o mecanismo de confirmação de titularidade.
- Nome "Registro de Entrada" pode evoluir; esta Nota registra o
  conceito, não o rótulo definitivo.

---

*Divícia — Nota Arquitetural — Registro de Entrada — Jul 2026.*
