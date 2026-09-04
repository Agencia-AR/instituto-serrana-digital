---
project: Instituto Serrana Digital
document: Índice de ADRs
version: "1.0"
date: 2026-09-04
---

# Architectural Decision Records

Registros de decisões arquiteturais. Um arquivo por decisão, numerado
sequencialmente, criado a partir de [`ADR-0000-template.md`](ADR-0000-template.md).

Regra (ver `CLAUDE.md`): nenhuma mudança arquitetural relevante sem um ADR.
Quando uma decisão substitui outra, marque `status: substituída` e preencha
`superseded_by` na antiga e `supersedes` na nova — nunca apague.

## Índice

| ADR | Título | Status |
|---|---|---|
| [0001](ADR-0001-duas-aplicacoes-vs-uma.md) | Duas aplicações (público + admin) vs. uma | aceita |
| [0002](ADR-0002-supabase-cloud.md) | Supabase Cloud como backend | proposta |
| [0003](ADR-0003-sympla-fonte-de-venda.md) | Sympla como fonte de verdade da venda na 1ª etapa | aceita |
| [0004](ADR-0004-whatsapp-multiprovedor.md) | Abstração multiprovedor de WhatsApp, Meta como baseline | aceita |
| [0005](ADR-0005-penpot-fonte-visual.md) | Penpot como fonte de verdade visual | aceita |
| [0006](ADR-0006-estrategia-de-deploy.md) | Estratégia de deploy (container-ready) | proposta |
| [0007](ADR-0007-modelo-de-contato-unificado.md) | Modelo de contato unificado (entidade canônica) | aceita |
| [0008](ADR-0008-politica-de-ia.md) | Política de IA (human-in-the-loop) | aceita |

> Os ADRs 0001–0008 nascem como **stubs** derivados de
> `docs/architecture/01-architecture.md` §23 e de
> `docs/discovery/02-decisions-assumptions.md`. Precisam ser preenchidos com
> contexto, opções e consequências completas antes de serem tratados como
> registro definitivo.
