---
adr: "0005"
title: Penpot como fonte de verdade visual
status: aceita
date: 2026-09-04
deciders: [Agência AR]
supersedes: null
superseded_by: null
---

# ADR-0005 — Penpot como fonte de verdade visual

## Contexto

O projeto precisa de Design System, tokens e handoff design→código com um
pipeline que funcione com Claude Code / Cursor via MCP.

## Decisão

Penpot é a ferramenta oficial de design. O fluxo é
PRD → Foundations → Tokens → Components → Screens → Prototype → inspeção via
Penpot MCP → código → validação visual. Nenhuma edição ampla no Penpot sem
leitura prévia e plano aprovado em lotes pequenos.

## Opções consideradas

| Opção | Prós | Contras |
|---|---|---|
| Penpot + MCP (escolhida) | open-source; MCP; tokens versionáveis | ecossistema menor que o do Figma |
| Figma | mercado maduro | custo; preferência já registrada contra |

## Consequências

- Positivas: tokens versionados no repo como ponte design↔código.
- Custos: disciplina de sincronização Penpot ↔ `packages/design-tokens`.
- Pendências: definir Remote MCP vs. local; auditar arquivo Penpot atual.

## Referências

- `docs/design/01-penpot-brief.md`
- `docs/discovery/02-decisions-assumptions.md` §1
