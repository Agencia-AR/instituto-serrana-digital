---
adr: "0008"
title: Política de IA (human-in-the-loop)
status: aceita
date: 2026-09-04
deciders: [Instituto Serrana, Agência AR]
supersedes: null
superseded_by: null
---

# ADR-0008 — Política de IA (human-in-the-loop)

## Contexto

A plataforma usa IA para FAQ, resumo de conversas, classificação, sugestão de
resposta, pós-venda e relatórios. É preciso delimitar o que a IA **não** pode
fazer sozinha, especialmente em dinheiro, preço e dados pessoais.

## Decisão

IA sempre com supervisão humana para decisões críticas. É proibido à IA, de forma
autônoma: conceder desconto, alterar preço, aprovar reembolso, movimentar
recursos, emitir nota fiscal, assumir decisão jurídica, expor dados entre
usuários ou executar mudança crítica sem autorização. Minimizar dados enviados
ao provedor de IA; nunca enviar segredos; registrar automações relevantes.

## Opções consideradas

| Opção | Prós | Contras |
|---|---|---|
| IA assistiva, human-in-the-loop (escolhida) | ganho de produtividade sem risco financeiro/jurídico | humano continua no caminho crítico |
| IA autônoma em pós-venda/atendimento | escala | risco de erro irreversível e de exposição de dados |

## Consequências

- Positivas: conformidade com a LGPD e com o apetite de risco do Instituto.
- Custos: fluxos de aprovação para ações sensíveis sugeridas por IA.
- Pendências: definir provedor de IA e contrato de tratamento de dados.

## Referências

- `docs/product/01-prd.md` §12.7 (AI-001, AI-002)
- `docs/security/01-security-lgpd.md` §14
