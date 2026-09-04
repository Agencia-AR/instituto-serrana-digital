---
adr: "0007"
title: Modelo de contato unificado (entidade canônica)
status: aceita
date: 2026-09-04
deciders: [Agência AR]
supersedes: null
superseded_by: null
---

# ADR-0007 — Modelo de contato unificado (entidade canônica)

## Contexto

A mesma pessoa ou organização aparece em vários papéis — comprador,
participante, doador, patrocinador, parceiro, voluntário, prestador, equipe,
artista. Duplicar cadastro por módulo gera divergência e impede a visão 360º.

## Decisão

Uma entidade canônica `contacts` (pessoa | organização) com `contact_roles`
acumuláveis. Todos os módulos (CRM, financeiro, RH, eventos, projetos) referenciam
`contacts` — nunca replicam o cadastro básico.

## Opções consideradas

| Opção | Prós | Contras |
|---|---|---|
| Contato canônico + papéis (escolhida) | visão 360º; sem duplicação | joins mais largos; regras de merge/dedupe necessárias |
| Cadastro por módulo | simples por módulo | mesma pessoa repetida; relatórios inconsistentes |

## Consequências

- Positivas: histórico único por pessoa/organização; base para CRM real.
- Custos: precisa de política de deduplicação e de merge de contatos.
- Pendências: definir chave natural (e-mail? telefone? documento?) e RLS por papel.

## Referências

- `docs/architecture/02-data-model.md` §1, §4, §12
- `docs/product/01-prd.md` §12.5 (CRM-002)
