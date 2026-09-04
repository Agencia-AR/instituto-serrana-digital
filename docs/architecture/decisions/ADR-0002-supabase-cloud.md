---
adr: "0002"
title: Supabase Cloud como backend
status: proposta
date: 2026-09-04
deciders: [Agência AR]
supersedes: null
superseded_by: null
---

# ADR-0002 — Supabase Cloud como backend

## Contexto

O produto precisa de Postgres, autenticação, storage, RLS e Edge Functions com
baixo esforço operacional numa fase inicial sem equipe de infraestrutura
dedicada. O destino de deploy final ainda não está confirmado (ver ADR-0006).

## Decisão

Adotar Supabase Cloud como plataforma de backend (Postgres + Auth + Storage +
RLS + Edge Functions), com n8n para orquestrações não críticas.

## Opções consideradas

| Opção | Prós | Contras |
|---|---|---|
| Supabase Cloud (escolhida) | tempo de setup mínimo; RLS nativo; auth pronto | lock-in parcial; custo cresce com uso |
| Supabase self-hosted | controle total; custo previsível | exige operação (backup, upgrades, monitoramento) |
| Postgres puro + serviço de auth próprio | flexível | reescreve o que o Supabase já entrega |

## Consequências

- Positivas: MVP mais rápido; segurança por RLS desde o início.
- Custos: dependência de um fornecedor; revisar custo antes da fase de escala.
- Pendências: confirmar região, plano e política de backup; alinhar com ADR-0006.

## Referências

- `docs/architecture/01-architecture.md` §2, §13, §21
- `docs/discovery/02-decisions-assumptions.md` §2
