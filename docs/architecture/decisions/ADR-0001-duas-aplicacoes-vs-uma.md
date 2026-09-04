---
adr: "0001"
title: Duas aplicações (público + admin) vs. uma
status: aceita
date: 2026-09-04
deciders: [Agência AR]
supersedes: null
superseded_by: null
---

# ADR-0001 — Duas aplicações (público + admin) vs. uma

## Contexto

O produto tem dois públicos com necessidades opostas de deploy, autorização,
performance e cadência de evolução: portal público (SEO, tráfego anônimo,
conteúdo) e plataforma administrativa (auth, RBAC/RLS, dados sensíveis).

## Decisão

Duas aplicações separadas — `apps/public-web` e `apps/admin-web` — compartilhando
Design System, tipos e pacotes internos via monorepo.

## Opções consideradas

| Opção | Prós | Contras |
|---|---|---|
| Duas apps no monorepo (escolhida) | isolamento de deploy/segurança; superfície pública mínima | mais configuração inicial |
| App única com rotas protegidas | setup simples | bundle público carrega código admin; deploy acoplado |

## Consequências

- Positivas: superfícies de ataque e de build separadas; evolução independente.
- Custos: pipeline e infra duplicados; disciplina para manter componentes no pacote `ui`.
- Pendências: definir estratégia de sessão/redirect entre domínios.

## Referências

- `docs/architecture/01-architecture.md` §3, §4
- `docs/discovery/02-decisions-assumptions.md` §1
