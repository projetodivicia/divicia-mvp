# Divícia — MVP App

Este repositório contém **exclusivamente a materialização tecnológica**
do produto Divícia.

**Não constitui patrimônio intelectual.** Nenhuma decisão de arquitetura,
produto ou conteúdo nasce aqui — este repositório implementa decisões já
tomadas e publicadas na Biblioteca Arquitetural.

---

## Onde está a arquitetura oficial

A especificação completa do MVP está no Blueprint de Materialização:

**[DIV-PROT-001 — Blueprint de Materialização do MVP, Trilha Despertar](https://github.com/projetodivicia/divicia-biblioteca-arquitetural/blob/main/03-produto/prototipo/trilha-do-despertar/DIV-PROT-001-Blueprint-Materializacao-MVP-Trilha-Despertar.md)**

A Biblioteca Arquitetural é a única fonte oficial de especificações.

Para as fontes específicas de cada tema (Home, Continuidade, Navegação,
Identidade Visual, etc.), ver [`FONTES-ARQUITETURAIS.md`](./FONTES-ARQUITETURAIS.md).

---

## Regra permanente deste repositório

- **Código evolui livremente** — commits, branches, merges, sem
  burocracia de aprovação linha a linha.
- **Conhecimento institucional nunca nasce aqui.** Qualquer decisão de
  produto, arquitetura, conteúdo ou regra de negócio pertence à
  Biblioteca Arquitetural — não a este repositório.
- **Artefatos Derivados** (arquivos copiados ou adaptados do patrimônio
  para consumo da aplicação — JSONs de conteúdo, tokens de design,
  assets exportados, etc.) devem declarar sua origem no cabeçalho do
  próprio arquivo. Ver seção abaixo.
- Quando uma sincronização da Biblioteca afeta a implementação (nova
  Voz, nova Reflexão, mudança de regra), a atualização correspondente
  neste repositório passa por revisão antes do merge para a branch
  principal.

---

## Artefatos Derivados — cabeçalho obrigatório

Todo arquivo copiado ou derivado da Biblioteca Arquitetural deve
declarar, no início do próprio arquivo (ou em `meta`, se for JSON):

```
ARTEFATO DERIVADO
Origem: [documento oficial na Biblioteca]
Versão da origem: [versão ou hash do commit de origem]
Tipo: [derivado fiel / operacional / técnico / de execução / temporário]
Finalidade: [uso pretendido neste repositório]
Fonte oficial: Biblioteca Arquitetural da Divícia

Este arquivo é um artefato derivado do patrimônio intelectual da
Divícia. A fonte oficial é exclusivamente o documento publicado na
Biblioteca Arquitetural. Alterações realizadas neste arquivo não
modificam o patrimônio institucional e poderão ser sobrescritas por
futuras sincronizações.
```

---

## Estrutura deste repositório

```
/app            — código do aplicativo, componentes, telas, rotas
/assets         — imagens, ícones de interface, tokens de design
/content        — Artefatos Derivados: conteúdo copiado da Biblioteca
                  para consumo da aplicação
/mocks          — dados simulados
/prototypes     — protótipos exportados do Stitch (ou outra ferramenta)
/tests          — testes
/docs           — documentação técnica do projeto
```

*Estrutura inicial sugerida. Pode evoluir conforme a implementação —
não é arquitetura obrigatória.*

---

## Governança

A governança operacional deste repositório evoluirá conforme o ritmo
real de desenvolvimento. Apenas as regras permanentes acima estão
consolidadas neste documento.
