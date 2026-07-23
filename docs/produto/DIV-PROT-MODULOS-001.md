# DIV-PROT-MODULOS-001 — Estado de Módulos do MVP

**Natureza:** Especificação de estado — sucedível (mesma natureza de EM-002 sucedendo EM-001)
**Status:** Vigente para a fase atual do produto (Trilha Despertar)
**Versão:** 1.0
**Data:** 18 de julho de 2026
**Vigente a partir de:** 18 de julho de 2026
**Blueprint de referência:** DIV-PROT-001
**Fase:** Trilha Despertar
**Local recomendado:** `03-produto/juridico/`

---

## Objetivo

Este documento registra, sem explicar juridicamente nada, quais módulos descritos em
**DIV-PROT-JURIDICO-001** estão ativos ou inativos na versão atual do produto.

Ele não decide, não interpreta, não justifica. Apenas liga e desliga módulos.

**Regra de uso:** este documento é a fonte única de verdade sobre módulos ativos nesta
fase. Toda documentação operacional, arquitetural ou técnica — incluindo
DIV-PROT-CONFORMIDADE-JURIDICA-001 e DIV-PROT-001 (Blueprint), mas não se limitando a eles — deverá
apenas referenciar este documento, nunca restatar o estado aqui registrado.

Este documento não cria funcionalidades nem altera direitos ou obrigações jurídicas.
Sua única função é declarar quais capacidades da Plataforma estão autorizadas para
materialização na fase vigente.

Este documento passa no Teste da Verdade Permanente de forma diferente dos Documentos
Fundadores: ele não precisa ser verdade permanente, porque registra explicitamente o
estado de uma fase, não uma decisão consolidada. Quando o estado mudar, nasce uma nova
versão — DIV-PROT-MODULOS-001 v2 — nunca uma edição silenciosa desta.

---

## Estado atual — MVP Trilha Despertar

### Ativos

- ✓ Cadastro (identificação, aceite de Termos e Política)
- ✓ Onboarding (Apresentação da Divícia, Boas-vindas, Pesquisa de Chegada)
- ✓ Trilha Despertar
- ✓ Vozes (Patrimônio das 40 Vozes)
- ✓ Travessias (Travessia da Voz)
- ✓ Reflexões Guiadas
- ✓ Sopro do Dia
- ✓ Home

### Não ativos nesta fase

- ✗ Lumi (materialização) — o conceito arquitetural de Lumi já possui decisões
  publicadas (ex.: D-014, MA-001); o que não está ativo nesta fase é sua materialização
  técnica, pendente de fechamento de MA-005.
- ✗ Inteligência Artificial (qualquer forma)
- ✗ Diário
- ✗ Memória (persistência longitudinal / Instância além do registro de sessão)
- ✗ Pagamentos
- ✗ Assinaturas
- ✗ Books
- ✗ Ritual da Consciência (fora do escopo desta fase do Blueprint — ver DIV-PROT-001)
- ✗ Explorações (fora do escopo desta fase do Blueprint — ver DIV-PROT-001)

---

## Critério de Ativação

Um módulo somente poderá ser marcado como Ativo quando, cumulativamente:

- fizer parte do Blueprint vigente (DIV-PROT-001 ou sucessor);
- possuir arquitetura publicada em Documento Fundador ou Mesa fechada;
- possuir implementação prevista para a fase corrente;
- possuir cobertura jurídica correspondente em DIV-PROT-JURIDICO-001;
- estiver autorizado para materialização por decisão explícita registrada neste
  documento.

A ausência de qualquer um desses critérios mantém o módulo como "não ativo nesta fase",
independentemente do estágio de maturidade conceitual que já possua.

---

## Consequência direta para materialização

Enquanto um módulo constar como **não ativo nesta fase** acima:

- Nenhuma tela, componente, aviso de consentimento específico, tabela de dados ou lógica
  de negócio referente a ele deve ser gerada por qualquer ferramenta de materialização
  (Google Stitch, Claude, Lovable ou outra).
- Nenhuma documentação funcional, especificação técnica, fluxo de navegação ou material
  institucional poderá assumir a existência desse módulo como algo já disponível na
  fase corrente.
- Textos jurídicos de DIV-PROT-JURIDICO-001 relativos a esse módulo (ex.: item 2.7 e 3.6 —
  Lumi/IA; item 2.10 — pagamentos) permanecem como referência para fases futuras, mas não
  devem ser traduzidos em interface nem em lógica nesta fase.

Quando um módulo mudar de "não ativo" para ativo, este documento deve ser sucedido por
nova versão antes de qualquer trabalho de materialização relativo a esse módulo começar,
verificando previamente o cumprimento do Critério de Ativação acima.

---

*Divícia — DIV-PROT-MODULOS-001 — Configuração Jurídica do MVP — v1.0 — Jul 2026.*
