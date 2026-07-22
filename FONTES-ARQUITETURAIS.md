# Fontes Arquiteturais

Este documento é um índice de navegação. Não substitui a leitura dos
documentos oficiais da Biblioteca nem constitui fonte de decisões
arquiteturais.

Este documento mapeia cada tema da aplicação ao seu documento oficial
na Biblioteca Arquitetural. Em caso de dúvida sobre uma regra, um
texto ou uma decisão de produto, a resposta está sempre num desses
documentos — nunca neste repositório.

A Biblioteca Arquitetural é a única fonte oficial de especificações:
https://github.com/projetodivicia/divicia-biblioteca-arquitetural

**Como localizar o arquivo:** utilize o identificador institucional
(ex.: `DIV-CON-001`) para localizar o documento na Biblioteca —
pesquise pelo identificador no repositório. Alguns documentos podem
aparecer abaixo apenas com seu identificador quando sua localização
física ainda não tiver sido consolidada; isso não é lacuna a ignorar,
é convenção permanente deste índice — caminhos de pasta mudam com o
tempo, o identificador não.

| Tema | Documento Oficial |
|---|---|
| Blueprint do MVP | DIV-PROT-001 |
| Pacote jurídico (Termos, Privacidade) | DIV-PROT-JURIDICO-001 |
| Estado de módulos ativos/inativos | DIV-PROT-MODULOS-001 |
| Conformidade técnica/jurídica | DIV-PROT-CONFORMIDADE-JURIDICA-001 |
| Registro de Entrada → Conta | Nota Arquitetural — Registro de Entrada |
| Fluxo de Onboarding | EM-003 |
| Reflexões Guiadas — conteúdo (15 Reflexões + Matriz Voz×Reflexão) | Patrimônio de Reflexões Guiadas v1.0 |
| Reflexões Guiadas — estrutura da experiência | DIV-MA-012 *(Mesa em andamento — Blocos D/E pendentes, ainda não é Documento Fundador)* |
| Sopro do Dia — banco de frases | `sopros-do-dia.json` |
| Navegação das Experiências | DIV-EXP-001 |
| Continuidade | DIV-CON-001 |
| Home | DIV-MA-013 |
| Primeiro Encontro | DIV-MA-009 |
| Pesquisa de Chegada | DIV-MA-010 |
| Instância de Experiência | DIV-MA-002 |
| Coleção Vozes do Silêncio (40 Vozes) | DIV-40VOZES-Conteudo-Autoral-Completo-v1.0 |
| Identidade visual — Manual Cromático | DIV-MANUAL-CROMATICO-v1.0 |
| Identidade visual — Guia Conceitual | DIV-GUIA-CONCEITUAL-v1.0 |
| Identidade visual — Glossário e Tom de Voz | DIV-GLOSSARIO-TOM-DE-VOZ-v1.0 |
| Identidade visual — índice consolidado | DIV-IDENTIDADE-VISUAL-v1.0 |

---

## Ordem de autoridade

Quando houver divergência entre fontes, utilize sempre a seguinte
prioridade:

1. Documento Fundador
2. Especificação
3. Blueprint
4. Mesa de Arquitetura (quando ainda não houver publicação)
5. Código existente

---

## Antes de implementar

Verifique:

- [ ] Existe Documento Fundador?
- [ ] Existe Especificação?
- [ ] Existe Blueprint?
- [ ] Existe Artefato Derivado oficial?

Se não existir nenhum dos quatro, **interrompa a implementação**. Não
crie arquitetura neste repositório — volte para a Biblioteca.

---

## Regra de manutenção

Sempre que um novo documento oficial for publicado na Biblioteca e
afetar a implementação, adicione uma linha nova aqui. Este arquivo
não substitui a Biblioteca — é só um índice de navegação.
