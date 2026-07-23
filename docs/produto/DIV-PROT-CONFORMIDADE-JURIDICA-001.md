# DIV-PROT-CONFORMIDADE-JURIDICA-001 — Especificação Técnica de Conformidade Jurídica

**Natureza:** Especificação técnica de materialização (não é documento jurídico; traduz
DIV-PROT-JURIDICO-001 e DIV-PROT-MODULOS-001 em requisitos de sistema)
**Status:** Em construção — v1.1 cobre o escopo do MVP Trilha Despertar
**Versão:** 1.1
**Data:** 18 de julho de 2026
**Local recomendado:** `03-produto/juridico/`
**Consome:** DIV-PROT-JURIDICO-001, DIV-PROT-MODULOS-001
**Dialoga diretamente com:** DIV-PROT-001 (Blueprint de Materialização do MVP)

---

## Objetivo

Este documento declara os requisitos mínimos de sistema necessários para que a
implementação permaneça aderente às decisões jurídicas vigentes (DIV-PROT-JURIDICO-001 e
DIV-PROT-MODULOS-001).

Ele não redige texto jurídico. Ele não decide o que está ativo ou inativo — isso
pertence exclusivamente a **DIV-PROT-MODULOS-001**. Ele não substitui especificações de
Engenharia nem decisões de Arquitetura de UX — a forma de materialização da interface
pertence ao Blueprint do Produto e às especificações próprias dessas camadas. Este
documento define apenas requisitos de conformidade; não prescreve componente visual,
padrão de navegação ou solução técnica específica além do estritamente necessário para
garantir o cumprimento jurídico.

---

## 1. Módulos

O estado de ativação de cada módulo (Lumi, Diário, Memória, IA, Pagamentos, Assinaturas,
Books, Ritual, Explorações) é definido exclusivamente em **DIV-PROT-MODULOS-001**. Este
documento nunca restabelece essa lista.

Regra de implementação: antes de gerar qualquer tela, componente ou lógica, verificar se
o módulo correspondente consta como ativo em DIV-PROT-MODULOS-001. Se não ativo, não
implementar — nem como placeholder visível, nem como código comentado que sugira
funcionalidade futura na interface. Esta regra vale para qualquer ferramenta de
materialização (ex.: Google Stitch, Claude, Lovable), sem se limitar a nenhuma delas em
particular.

---

## 2. Tela de aviso de privacidade (pré-coleta de dado)

Posição no fluxo: entre a Etapa 01 (Apresentação da Divícia) e a Etapa 02
(Identificação) do Blueprint DIV-PROT-001 — Etapa 01.5, pendente de registro formal via
decisão pontual antes desta versão ser considerada fechada.

Conteúdo mínimo: aviso curto de privacidade com link para a Política de Privacidade
vigente (texto completo em DIV-PROT-JURIDICO-001 §3), mais o checkbox de aceite obrigatório
descrito no bloco 3 abaixo.

Este aviso não substitui os Termos e Política completos (DIV-PROT-JURIDICO-001 §2 e §3) — é o
mínimo necessário para dar base legal à coleta que já ocorre nas Etapas 02 e 04
(Identificação e Pesquisa de Chegada), enquanto a arquitetura de Cadastro técnico
completo (autenticação, conta persistente) permanece pendência aberta no Blueprint.

---

## 3. Registro de aceite

O sistema deverá registrar, no momento do aceite:

- versão do documento aceito (Termos e Política, cada um com sua própria versão);
- idioma do documento aceito;
- timestamp exato (data e hora);
- identificador da usuária ou da sessão;
- identificador da sessão, quando a conta ainda não existir;
- IP, quando disponível.

O aceite de Termos e Política é um checkbox único e obrigatório. O aceite de marketing é
um checkbox separado, opcional, nunca pré-marcado, e nunca condiciona o prosseguimento do
onboarding.

---

## 4. Exibição de documentos legais

Os documentos legais (Termos de Uso e Política de Privacidade) devem permanecer
acessíveis a qualquer momento, sem interromper ou invalidar o fluxo de onboarding em
andamento. Ao retornar do documento legal, a usuária deve poder continuar exatamente no
ponto onde estava.

A solução de interface (modal, aba sobreposta ou outra) pertence à camada de UX e não é
prescrita por este documento.

---

## 5. Segregação de dados

A arquitetura deverá manter separação lógica entre a identidade da usuária
(Identificação: nome, pronome) e o conteúdo das experiências (Instâncias), utilizando
identificadores internos, controles de acesso e mecanismos de pseudonimização sempre que
possível. Isso não impede o sistema de relacionar conta e experiências quando
necessário para a operação do produto — o requisito é de separação lógica e
controle de acesso, não de impossibilidade de associação.

Camadas devem permanecer conceitualmente separadas:

```
Conta / Identificação
      ↓
Experiências (Instâncias)
      ↓
Diário (não ativo nesta fase)
      ↓
IA / Lumi (não ativo nesta fase)
```

Esta separação decorre diretamente do princípio já publicado de que o sistema persiste a
Instância de Experiência, não a identidade da mulher (D-001, MA-001). Não é uma decisão
jurídica nova — é a aplicação técnica de uma decisão arquitetural já existente, motivada
adicionalmente por proteção de dados (privacy by design).

Este princípio deve ser levado ao documento técnico de Engenharia correspondente, para
não permanecer apenas registrado aqui.

---

## 6. Exclusão de conta

Deve existir opção acessível à usuária para excluir sua conta e apagar seu histórico.

Antes da exclusão definitiva, o sistema deverá solicitar confirmação explícita da
usuária, informando que a operação é irreversível, ressalvadas as hipóteses legais de
retenção.

Ao ser confirmada, a exclusão deve:

- excluir dados de autenticação/identificação;
- excluir registros de experiências vinculados à conta;
- excluir histórico associado;
- preservar apenas dados cuja retenção seja legalmente obrigatória (ver DIV-PROT-JURIDICO-001
  §3.9, Tabela de Retenção, quando definida).

No MVP, essa ação pode ser implementada de forma simples (remoção da linha/registro
correspondente), desde que preserve o comportamento acima.

---

## 7. Inteligência artificial

Não implementar nesta versão. Ver módulo "Lumi" e "Inteligência Artificial" em
DIV-PROT-MODULOS-001 — ambos não ativos nesta fase. Nenhuma tela de chat, aviso pré-IA ou
lógica de processamento de linguagem deve ser gerada nesta fase.

---

## 8. Pagamentos e assinaturas

Não implementar nesta versão. Ver módulos "Pagamentos" e "Assinaturas" em
DIV-PROT-MODULOS-001 — ambos não ativos nesta fase. Nenhuma lógica de checkout, plano ou
cobrança deve ser gerada nesta fase.

---

## 9. Idade mínima

Checkbox de declaração de maioridade (18 anos ou mais) obrigatório no mesmo momento do
aceite de Termos e Política. Ver texto literal em DIV-PROT-JURIDICO-001 §4.4.

---

## 10. Validação de Conformidade

Nenhuma implementação poderá ser considerada concluída sem verificar:

- ✓ Fluxo de aceite
- ✓ Registro de consentimento
- ✓ Links jurídicos acessíveis sem interromper o fluxo
- ✓ Exclusão de conta com confirmação explícita
- ✓ Declaração de maioridade
- ✓ Separação lógica dos dados
- ✓ Estado dos módulos conforme DIV-PROT-MODULOS-001

---

## Pendências registradas (não resolvidas por este documento)

- Posição definitiva da Etapa 01.5 no Blueprint — depende de decisão pontual formal
  (ver nota no bloco 2).
- Arquitetura de Cadastro técnico completo (autenticação, conta persistente) — pendência
  já registrada em DIV-PROT-001, possível conflito com EM-002.
- Tabela de Retenção detalhada — depende de DIV-PROT-JURIDICO-001 §3.9.
- Fornecedores de banco de dados e autenticação ainda não nomeados.

---

*Divícia — DIV-PROT-CONFORMIDADE-JURIDICA-001 — Especificação Técnica de Conformidade Jurídica — v1.1 — Jul 2026.*
