# CLAUDE.md — Instituto Serrana Digital

## Fonte principal

Leia `docs/product/01-prd.md` antes de qualquer tarefa relevante.

## Fontes da verdade

- Produto: `docs/product/01-prd.md`
- Arquitetura: `docs/architecture/01-architecture.md`
- Modelo de dados: `docs/architecture/02-data-model.md`
- Integrações: `docs/architecture/03-integrations.md`
- Decisões: `docs/discovery/02-decisions-assumptions.md` + `docs/architecture/decisions/`
- Visual: Penpot
- Tokens: `packages/design-tokens`
- Implementação: Git

## Estados de informação

Use: **CONFIRMADO**, **PROPOSTA**, **PENDENTE**, **DECISÃO**.

Nunca converta hipótese em fato silenciosamente.

## Regras de produto

- Penpot substitui Figma.
- Home pública começa na base da escadaria e sobe até a Igreja de Santa Rita.
- Existem Portal Público e Plataforma Administrativa.
- Sympla é a fonte oficial da venda na primeira etapa.
- Não presumir API pública de criação de pedido/hold.
- WhatsApp deve usar adapter multiprovedor.
- Meta Cloud API é baseline oficial.
- Evolution pode usar Cloud API ou Baileys; identificar o modo.
- megaAPI deve ser tratada como gateway de terceiros e ter mecanismo validado.
- Priorizar MVP.
- Discovery e protótipo avançam em paralelo.

## Regras de trabalho

- Não expor segredos; nunca versionar tokens, chaves, `.env` ou URLs MCP com segredo.
- Não alterar dados críticos sem confirmação.
- Não fazer mudanças arquiteturais sem ADR (`docs/architecture/decisions/`).
- Não instalar dependência sem necessidade.
- Não modificar Penpot antes de uma leitura/auditoria inicial (ver `docs/design/01-penpot-brief.md` §18).
- Trabalhar em lotes pequenos; registrar decisões.
- Git: um objetivo por commit; sem `reset --hard`; sem `force push`; `git status`
  antes e depois; sem ação destrutiva sem solicitação explícita.
- Detalhamento do fluxo: `docs/workflow/01-claude-code-workflow.md`.

## Ferramental de agentes de IA

Este repositório tem AIOS Core instalado (`.aiox-core/`, orquestrado por
`@aiox-master`) e regras espelhadas em `AGENTS.md` e `.cursor/rules/` para
outros clientes (Cursor, Codex, Gemini). As seções `AIOX-MANAGED` de
`AGENTS.md` são geridas pelo AIOS — não editar manualmente.

## Primeira tarefa ao carregar este projeto

Não altere arquivos.

Leia, nesta ordem:

1. `docs/product/01-prd.md`
2. `docs/architecture/01-architecture.md`
3. `docs/discovery/01-meeting-plan.md`
4. `docs/discovery/02-decisions-assumptions.md`

Produza uma auditoria de consistência e um plano do próximo lote.
