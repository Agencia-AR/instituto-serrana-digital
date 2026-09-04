---
adr: "0004"
title: Abstração multiprovedor de WhatsApp, Meta como baseline
status: aceita
date: 2026-09-04
deciders: [Agência AR]
supersedes: null
superseded_by: null
---

# ADR-0004 — Abstração multiprovedor de WhatsApp, Meta como baseline

## Contexto

O atendimento por WhatsApp é requisito. Há três caminhos possíveis (Meta Cloud
API oficial, Evolution API, megaAPI) com perfis de risco diferentes — Evolution e
megaAPI podem operar em modo não oficial (Baileys/WhatsApp Web), sujeito a
bloqueio.

## Decisão

Todo o domínio fala com uma interface `MessagingProvider`. Implementações:
`MetaWhatsAppProvider` (baseline de produção), `EvolutionWhatsAppProvider`,
`MegaApiWhatsAppProvider`. Cada instância registra explicitamente seu
`connection_type`; modo Baileys é classificado como alternativo/não oficial com
aceite de risco formal.

## Opções consideradas

| Opção | Prós | Contras |
|---|---|---|
| Port + adapters, Meta baseline (escolhida) | troca de provedor sem tocar domínio; risco isolado | mais código de normalização de webhook |
| Só Meta Cloud API | oficial, estável | custo por conversa; onboarding Meta Business mais lento |
| Só Evolution/self-host | barato, flexível | risco de bloqueio como dependência crítica única |

## Consequências

- Positivas: nenhuma regra de produto depende do payload bruto de um provedor.
- Custos: manter normalização de webhook por provedor.
- Pendências: Meta Business, WABA, número, templates e opt-in do Instituto.

## Referências

- `docs/architecture/01-architecture.md` §8.1
- `docs/architecture/03-integrations.md` §3–§7
- `docs/discovery/02-decisions-assumptions.md` §1
