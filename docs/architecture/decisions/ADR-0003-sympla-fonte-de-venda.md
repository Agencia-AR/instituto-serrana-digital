---
adr: "0003"
title: Sympla como fonte de verdade da venda na 1ª etapa
status: aceita
date: 2026-09-04
deciders: [Instituto Serrana, Agência AR]
supersedes: null
superseded_by: null
---

# ADR-0003 — Sympla como fonte de verdade da venda na 1ª etapa

## Contexto

O Instituto já opera venda de ingressos pela Sympla. A documentação pública da
Sympla (contrato v1.6.0, verificada em 2026-09-04) é majoritariamente de leitura:
não há endpoint público confirmado para criar pedido, segurar assento ou
processar checkout white-label.

## Decisão

A Sympla permanece como fonte oficial de venda, pagamento, emissão e check-in
na primeira etapa. A plataforma apenas **importa e normaliza** dados da Sympla
(eventos, pedidos, participantes, valores, UTM, check-in) atrás de um
`TicketingProvider`, e concentra CRM, gestão, consolidação e inteligência.

## Opções consideradas

| Opção | Prós | Contras |
|---|---|---|
| Sympla como fonte, sync read-only (escolhida) | zero risco de regressão comercial; rápido | plataforma não controla o funil de compra |
| Checkout próprio | controle total da jornada | exige gateway, fiscal, antifraude, contrato — fora do MVP |

## Consequências

- Positivas: MVP não depende de capacidade não confirmada da Sympla.
- Custos: estado comercial oficial é sempre da Sympla; mapa de mesas é ilustrativo.
- Pendências: obter por escrito da Sympla o que a API contratada realmente expõe
  (criação de pedido, hold de assento, `marked_place_name`).

## Referências

- `docs/product/01-prd.md` §11 (SYM-001..003)
- `docs/architecture/03-integrations.md` §2
- `docs/architecture/01-architecture.md` §8.2, §9
