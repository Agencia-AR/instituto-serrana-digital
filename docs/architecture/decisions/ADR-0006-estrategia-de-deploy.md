---
adr: "0006"
title: Estratégia de deploy (container-ready)
status: proposta
date: 2026-09-04
deciders: [Agência AR]
supersedes: null
superseded_by: null
---

# ADR-0006 — Estratégia de deploy (container-ready)

## Contexto

O destino final de hospedagem ainda não está confirmado. É preciso não travar a
decisão agora, mas também não construir de um jeito que só rode num provedor.

## Decisão (proposta)

Construir tudo **container-ready** desde o início (Dockerfile por app, CI/CD no
GitHub, migrations controladas, health checks, rollback). O destino — VPS/Coolify
ou serviço gerenciado (ex.: Vercel para o front, Supabase para o backend) — é
confirmado antes da fase de deploy, sem exigir reescrita.

## Opções consideradas

| Opção | Prós | Contras |
|---|---|---|
| Container-ready, destino adiado (escolhida) | portabilidade; decisão informada depois | um pouco mais de setup inicial |
| Comprometer com Vercel + Supabase agora | DX ótima; zero infra | custo variável; lock-in antes de dados de uso |
| Comprometer com VPS/Coolify agora | custo previsível | exige operação antes de haver produto |

## Consequências

- Positivas: a decisão de hospedagem vira reversível.
- Custos: manter Docker e pipeline genéricos.
- Pendências: confirmar orçamento de infra e responsável por operação.

## Referências

- `docs/architecture/01-architecture.md` §17–§19
- `docs/discovery/02-decisions-assumptions.md` §2
