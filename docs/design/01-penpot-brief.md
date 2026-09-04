---
project: Instituto Serrana Digital
document: Penpot Design Brief
version: "1.0"
date: 2026-09-04
---

# Design — Penpot

# 1. Ferramenta oficial

Penpot é a fonte de verdade visual.

Fluxo:

```text
PRD
→ Foundations
→ Tokens
→ Components
→ Screens
→ Prototype
→ MCP inspection
→ Code
→ Visual validation
```

---

# 2. Estrutura Penpot

```text
00 — Foundations & Reference
01 — Design System
02 — Portal Público
03 — Bolerata
04 — Plataforma Administrativa
05 — Mobile
06 — Prototypes & Flows
```

---

# 3. Benchmark

## Heritage / narrativa

- CyArk;
- Google Arts & Culture.

## Institucional

- National Trust.

## Eventos

- Fever;
- DICE.

## Mesas / planta

- Seats.io;
- Cvent Event Diagramming.

## Operação

- Eventbrite Organizer.

## CRM

- Attio.

## ONG

- Neon One.

## Financeiro

- Stripe Dashboard.

Referências servem para padrões de UX, não para copiar identidade.

---

# 4. Identidade institucional

Paleta inicial:

| Token | Cor |
|---|---|
| ivory | `#F5F0E7` |
| colonial-blue | `#315B70` |
| terracotta | `#A35D42` |
| garden-green | `#486A4A` |
| graphite | `#202321` |
| antique-gold | `#A47D38` |

---

# 5. Bolerata

| Token | Cor |
|---|---|
| black | `#080808` |
| graphite | `#171717` |
| gold | `#A37C35` |
| light-gold | `#C6A35A` |
| ivory | `#F4F0E7` |

---

# 6. Tipografia

Proposta:

- títulos culturais: Cormorant Garamond ou Marcellus;
- interface: Inter ou Manrope.

A escolha final deve ser validada no Penpot e no navegador.

---

# 7. Design Tokens

```text
primitive.*
semantic.*
component.*
motion.*
breakpoint.*
```

Exemplos:

```text
semantic.bg.page
semantic.bg.surface
semantic.text.primary
semantic.text.secondary
semantic.action.primary
semantic.status.success
semantic.status.warning
semantic.status.danger
```

---

# 8. Componentes prioritários

## Foundation

- Button;
- Input;
- Select;
- Checkbox;
- Switch;
- Badge;
- Tooltip;
- Avatar;
- Spinner.

## Navigation

- Public Header;
- Admin Sidebar;
- Breadcrumb;
- Tabs;
- Mobile Navigation.

## Data

- Metric Card;
- Table;
- Filters;
- Empty State;
- Error State;
- Loading State.

## CRM

- Pipeline Column;
- Pipeline Card;
- Contact Drawer;
- Timeline;
- AI Summary;
- Task Item.

## Event

- Event Card;
- Edition Card;
- Schedule;
- Participant Row.

## Map

- Table Object;
- Seat Object;
- Stage;
- Venue Canvas;
- Map Legend;
- Toolbar;
- Detail Drawer.

## Finance

- Financial Metric;
- Transaction Row;
- Cost Center;
- Attachment;
- Reconciliation Item.

---

# 9. Storyboard Santa Rita

## Estado 0

Base da escadaria.

Texto:

```text
INSTITUTO SERRANA
Cultura, memória e desenvolvimento no coração do Serro.
```

## Estado 1

Entrada.

```text
Cada degrau guarda uma história.
```

## Estado 2

Subida.

```text
Memória • Cultura • Patrimônio • Comunidade
```

## Estado 3

Meio.

Apresentação institucional.

## Estado 4

Últimos degraus.

```text
Preservar o passado.
Mobilizar o presente.
Construir novos caminhos.
```

## Estado 5

Chegada frontal.

Identidade + CTAs.

---

# 10. Regras do hero

- começar embaixo;
- nunca iniciar diante da igreja;
- manter igreja como ponto focal;
- evitar texto sobre fachada;
- não tornar experiência longa;
- reduzir movimento no final;
- desktop e mobile separados;
- reduced-motion obrigatório.

---

# 11. Mapa Bolerata

## Conceito A

Mapa ilustrado, cultural e contextual.

## Conceito B

Mapa técnico e operacional.

O Design System deve compartilhar estados, mas permitir linguagem visual diferente.

---

# 12. Dashboard

Primeira dobra:

- próxima edição;
- ocupação;
- receita;
- pendências;
- atendimento;
- falhas;
- atividade.

Evitar “dashboard de template” com gráficos sem ação.

---

# 13. CRM

- Kanban;
- tabela;
- busca;
- filtros;
- Contact Drawer;
- resumo IA;
- histórico.

Referência funcional: Attio.

---

# 14. Responsividade

## Público mobile

- narrativa Santa Rita simplificada;
- Bolerata;
- eventos;
- CTA.

## Admin mobile

Priorizar:

- dashboard;
- CRM;
- atendimento;
- mapa;
- check-in;
- tarefas.

---

# 15. Acessibilidade

- contraste AA;
- foco;
- teclado;
- labels;
- reduced motion;
- estados não dependem apenas de cor;
- área de toque adequada.

---

# 16. Protótipo da reunião

Telas mínimas:

1. Home;
2. Instituto;
3. projetos;
4. Bolerata;
5. edição;
6. mapa A;
7. mapa B;
8. login;
9. dashboard;
10. CRM;
11. financeiro;
12. mobile.

---

# 17. Handoff

Cada componente relevante deve documentar:

- finalidade;
- props;
- estados;
- responsividade;
- acessibilidade;
- componente de código esperado;
- tokens;
- exceções.

---

# 18. Uso do MCP

Primeira execução sempre:

1. ler;
2. listar;
3. auditar;
4. propor;
5. só depois editar.

Mudanças em lotes pequenos.
