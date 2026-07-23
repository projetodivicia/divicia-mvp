# Origem dos Ativos de Identidade Visual

## Fonte oficial

Repositório:
projetodivicia/divicia-biblioteca-arquitetural

Pasta:
07-identidade-visual/

Commit:
e7c93c8 (merge de chore/corrigir-fundo-de-vozes — corrige nomenclatura dos fundos das Vozes)

## Finalidade

Esta pasta contém uma cópia operacional de documentos e ativos utilizados na materialização tecnológica do MVP da Divícia.

## Regra de soberania

A Biblioteca Arquitetural permanece como fonte oficial.

Em caso de divergência entre esta cópia e a Biblioteca, prevalece a Biblioteca.

Mudanças oficiais não devem nascer nesta pasta.

## Escopo copiado

| Origem (Biblioteca) | Destino (divicia-mvp) |
|---|---|
| `07-identidade-visual/DIV-IDENTIDADE-VISUAL-v1.0.md` | `design/identidade-visual/documentos-orientadores/DIV-IDENTIDADE-VISUAL-v1.0.md` |
| `07-identidade-visual/DIV-GUIA-CONCEITUAL-v1.0.md` | `design/identidade-visual/documentos-orientadores/DIV-GUIA-CONCEITUAL-v1.0.md` |
| `07-identidade-visual/DIV-MANUAL-CROMATICO-v1.0.md` | `design/identidade-visual/documentos-orientadores/DIV-MANUAL-CROMATICO-v1.0.md` |
| `07-identidade-visual/DIV-GLOSSARIO-TOM-DE-VOZ-v1.0.md` | `design/identidade-visual/linguagem/DIV-GLOSSARIO-TOM-DE-VOZ-v1.0.md` |
| `07-identidade-visual/simbolos-pilares/com-fundo/simbolo_presenca_sol_oficial.png` | `design/identidade-visual/simbolos-pilares/com-fundo/simbolo_presenca_sol_oficial.png` |
| `07-identidade-visual/simbolos-pilares/com-fundo/simbolo_conexao_elo_oficial.png` | `design/identidade-visual/simbolos-pilares/com-fundo/simbolo_conexao_elo_oficial.png` |
| `07-identidade-visual/simbolos-pilares/com-fundo/simbolo_aprendizado_terracota_dourado.png` | `design/identidade-visual/simbolos-pilares/com-fundo/simbolo_aprendizado_terracota_dourado.png` |
| `07-identidade-visual/simbolos-pilares/com-fundo/simbolo_ressignificado_meialua_oficial.png` | `design/identidade-visual/simbolos-pilares/com-fundo/simbolo_ressignificado_meialua_oficial.png` |
| `07-identidade-visual/simbolos-pilares/com-fundo/simbolo_transformacao_roxo_dourado.png` | `design/identidade-visual/simbolos-pilares/com-fundo/simbolo_transformacao_roxo_dourado.png` |
| `07-identidade-visual/fundo-de-vozes/voz-presenca.png` | `design/identidade-visual/ativos-produtos/fundo-de-vozes/voz-presenca.png` |
| `07-identidade-visual/fundo-de-vozes/voz-conexao.png` | `design/identidade-visual/ativos-produtos/fundo-de-vozes/voz-conexao.png` |
| `07-identidade-visual/fundo-de-vozes/voz-aprendizado.png` | `design/identidade-visual/ativos-produtos/fundo-de-vozes/voz-aprendizado.png` |
| `07-identidade-visual/fundo-de-vozes/voz-ressignificado.png` | `design/identidade-visual/ativos-produtos/fundo-de-vozes/voz-ressignificado.png` |
| `07-identidade-visual/fundo-de-vozes/voz-transformacao.png` | `design/identidade-visual/ativos-produtos/fundo-de-vozes/voz-transformacao.png` |
| `07-identidade-visual/colecao-vozes-do-silencio/capa-vozes-do-silencio.png` | `design/identidade-visual/ativos-produtos/vozes-do-silencio/capa-vozes-do-silencio.png` |
| `07-identidade-visual/diario-dos-saberes/capa-diario-dos-saberes.png` | `design/identidade-visual/ativos-produtos/diario-dos-saberes/capa-diario-dos-saberes.png` |
| `07-identidade-visual/ritual-da-consciencia/logo-ritual-da-consciencia.png` | `design/identidade-visual/ativos-produtos/ritual-da-consciencia/logo-ritual-da-consciencia.png` |
| `07-identidade-visual/ritual-da-consciencia/mapa-escolha-vozes-por-posicao.png` | `design/identidade-visual/referencias-funcionais/ritual-da-consciencia/mapa-escolha-vozes-por-posicao.png` |

Os quatro ativos listados na seção "Ativos de produtos e experiências" (fundos das Vozes por Pilar, capa da Coleção Vozes do Silêncio, capa do Diário dos Saberes, logo do Ritual da Consciência) são ativos de produtos ou experiências específicas — não devem ser classificados como ativos institucionais universais da Divícia.

O mapa de escolha de Vozes por posição é referência funcional do Ritual da Consciência, e não referência estética global.

## Itens deliberadamente não copiados

- `fontes-originais/BrandBook-Apresentacao.pdf`
- `assets/`
- `simbolos-pilares/transparente/`

Motivos:

- o BrandBook em PDF possui 51 MB e permanece preservado na Biblioteca como fonte primária;
- as outras duas pastas estão vazias e não são rastreadas pelo Git.

## Lacunas identificadas

- ausência de logotipo institucional master da Divícia;
- ausência de arquivos binários das fontes;
- ausência de texturas;
- ausência dos símbolos dos Pilares com fundo transparente.

## Inconsistências encontradas na origem

Registradas sem correção — pertencem à Biblioteca, não ao repositório de materialização:

1. `DIV-MANUAL-CROMATICO-v1.0.md` cita `fontes-originais/Divicia_Manual_Cromatico_FINAL.docx`, mas o arquivo não existe na pasta.
2. `DIV-GUIA-CONCEITUAL-v1.0.md` e `DIV-GLOSSARIO-TOM-DE-VOZ-v1.0.md` citam `BrandBook_-_Apresentação.pdf`, enquanto o arquivo físico existente se chama `BrandBook-Apresentacao.pdf`.

## Atualização

Esta pasta não deve ser alterada como fonte de verdade.

Mudanças oficiais devem nascer ou ser aprovadas na Biblioteca e depois ser novamente propagadas para o repositório de materialização.

## Histórico de sincronizações

### 2026-07-23 — Correção de nomenclatura dos Fundos das Vozes

- Origem: `07-identidade-visual/cards-completos/` → `07-identidade-visual/fundo-de-vozes/` (commit `e7c93c8` da Biblioteca, merge de `chore/corrigir-fundo-de-vozes`).
- Destino: `design/identidade-visual/ativos-produtos/pilares/` → `design/identidade-visual/ativos-produtos/fundo-de-vozes/`.
- Arquivos renomeados: `card-presenca.png` → `voz-presenca.png`, `card-conexao.png` → `voz-conexao.png`, `card-aprendizado.png` → `voz-aprendizado.png`, `card-ressignificado.png` → `voz-ressignificado.png`, `card-transformacao.png` → `voz-transformacao.png`.
- `DIV-IDENTIDADE-VISUAL-v1.0.md` ressincronizado com a versão atual da Biblioteca.
- Verificação: as 5 imagens renomeadas foram conferidas bit a bit (`git hash-object`) contra os arquivos correspondentes da Biblioteca — 5/5 idênticos, nenhuma alteração de conteúdo binário.
