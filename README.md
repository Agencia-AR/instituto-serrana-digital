---
project: Instituto Serrana Digital
document: Índice do repositório
version: "1.0"
date: 2026-09-04
status: Pré-descoberta / pronto para prototipação
---

# Instituto Serrana Digital

Repositório de produto, arquitetura, design e desenvolvimento da plataforma web
**pública e administrativa** do Instituto Serrana, tendo a **Bolerata** como
primeiro grande caso de uso de eventos, relacionamento, reservas e inteligência
operacional.

> Fase atual: pré-descoberta + design conceitual em paralelo. Ainda não há código
> de aplicação — o próximo entregável é o protótipo navegável no Penpot para a
> reunião de descoberta (Gate D1).

## Comece por

Primeira vez no repositório? Leia [`START-HERE.md`](START-HERE.md) para
preparar o ambiente (Git, Penpot MCP). Depois siga a ordem de leitura abaixo.

## Ordem de leitura

Para qualquer tarefa relevante, ler nesta ordem:

1. [`CLAUDE.md`](CLAUDE.md) — regras operacionais e de governança
2. [`docs/product/01-prd.md`](docs/product/01-prd.md) — requisitos de produto
3. [`docs/architecture/01-architecture.md`](docs/architecture/01-architecture.md) — arquitetura de software
4. [`docs/discovery/02-decisions-assumptions.md`](docs/discovery/02-decisions-assumptions.md) — decisões, propostas e pendências
5. O documento específico da tarefa atual (ver mapa abaixo)

Esta é a **única** ordem de leitura canônica. Qualquer outro documento que liste
uma sequência de leitura deve apontar para cá.

## Mapa de documentos

| Caminho | Finalidade | Natureza |
|---|---|---|
| `docs/product/01-prd.md` | Fonte principal de requisitos de produto | Normativo |
| `docs/product/02-roadmap-mvp.md` | Fases, MVP (MoSCoW), DoR/DoD, riscos | Normativo |
| `docs/architecture/01-architecture.md` | Arquitetura de software, infraestrutura e repositório | Normativo |
| `docs/architecture/02-data-model.md` | Modelo conceitual de dados | Normativo |
| `docs/architecture/03-integrations.md` | Sympla, WhatsApp, Instagram, e-mail, n8n | Normativo |
| `docs/architecture/decisions/` | Architectural Decision Records (ADRs) | Normativo |
| `docs/design/01-penpot-brief.md` | Design System, tokens, storyboard, handoff | Normativo |
| `docs/security/01-security-lgpd.md` | Segurança, privacidade e governança de acesso | Normativo |
| `docs/discovery/01-meeting-plan.md` | Plano e estrutura da reunião de descoberta | Vivo |
| `docs/discovery/02-decisions-assumptions.md` | Decisões, propostas, hipóteses e pendências | Vivo |
| `docs/discovery/03-roteiro-reuniao-descoberta.md` | Roteiro minuto a minuto + matriz + P0/P1/P2 do protótipo | Vivo |
| `docs/apresentacao-descoberta.html` | Material navegável de apoio à reunião (design system + telas-conceito) | Vivo |
| `docs/workflow/01-claude-code-workflow.md` | Detalhamento do fluxo de trabalho com IA | Vivo |
| `prompts/discovery-presentation.md` | Prompt para gerar o roteiro da apresentação | Ferramenta |

## Estrutura do repositório

```text
apps/            public-web (portal) + admin-web (plataforma) — scaffold, sem código ainda
packages/        ui, design-tokens — scaffold, sem código ainda
services/        integrations — scaffold, sem código ainda
docs/            documentação normativa e viva (ver mapa acima)
prompts/         prompts operacionais prontos para copiar no Claude Code
assets/          referências visuais (Santa Rita, local da Bolerata)
scripts/         automações do repositório
```

Ferramental de agentes de IA instalado neste repositório: **AIOS Core**
(`.aiox-core/`, orquestrado por `@aiox-master`) e regras espelhadas para
Claude Code, Cursor, Codex, Gemini e outros clientes — ver `AGENTS.md` e
`.cursor/rules/`.

## Fontes da verdade

| Dimensão | Fonte |
|---|---|
| Produto e regra de negócio | `docs/product/01-prd.md` |
| Arquitetura | `docs/architecture/01-architecture.md` |
| Decisões e incertezas | `docs/discovery/02-decisions-assumptions.md` + `docs/architecture/decisions/` |
| Visual | Penpot |
| Tokens | `packages/design-tokens` (vazio, aguardando os P0/P1 do plano Penpot) |
| Implementação | Este repositório Git |

Não há documento consolidado ("mestre"): os arquivos individuais **são** a
fonte. Se um consolidado for necessário para leitura offline, ele deve ser
gerado e tratado como artefato descartável (`docs/_generated/`, fora do
versionamento).

## Regra de governança

Toda informação ainda não formalmente validada deve ser classificada como:

- **CONFIRMADO** — sustentado por documento, fonte oficial ou decisão registrada;
- **PROPOSTA** — direção escolhida para protótipo ou discussão;
- **PENDENTE** — depende de informação do Instituto;
- **DECISÃO** — escolha formal já adotada no projeto.

O protótipo pode avançar com itens `PROPOSTA`, desde que não sejam apresentados
ao Instituto como fatos confirmados.
