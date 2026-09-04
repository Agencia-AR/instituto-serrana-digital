---
project: Instituto Serrana Digital
document: Integrations
version: "1.0"
date: 2026-09-04
---

# Integrações

# 1. Princípio

Toda integração externa deve estar atrás de uma interface interna.

```text
Domain
→ Port
→ Provider Adapter
→ External API
```

Nenhuma regra crítica do produto deve depender diretamente do formato bruto de um fornecedor.

---

# 2. Sympla

## 2.1. Status atual

A documentação pública atual da Sympla, em 2026-09-04, apresenta contrato v1.6.0 para produtores.

Operações documentadas incluem:

- listar eventos;
- buscar evento;
- listar apresentações;
- buscar apresentação;
- listar pedidos;
- buscar pedido;
- listar participantes;
- buscar participante;
- realizar check-in.

A API pública expõe, entre outros, campos úteis como:

- `order_status`;
- `order_total_sale_price`;
- `order_total_net_value`;
- `buyer_email`;
- UTM;
- `sector_name`;
- `marked_place_name`;
- `ticket_status`;
- `ticket_sale_price`;
- `ticket_net_value`;
- check-in.

## 2.2. Limitação arquitetural

No contrato público atual analisado, não deve ser presumida capacidade para:

- criar pedido de venda;
- reservar/segurar assento;
- processar checkout;
- alterar lugar marcado.

Qualquer operação desse tipo dependerá de confirmação oficial/contratual.

## 2.3. Sync

```text
Sympla
→ Sync Worker/n8n
→ Normalizer
→ Upsert local
→ Link CRM
→ Dashboard/Finance
```

## 2.4. Dados locais

- external id;
- event;
- presentation;
- order;
- participant;
- ticket;
- status;
- place;
- values;
- UTM;
- check-in;
- timestamps.

---

# 3. WhatsApp — arquitetura multiprovedor

```text
CRM / Atendimento / IA
          ↓
MessagingProvider
          ↓
 ┌────────┼──────────┐
 ↓        ↓          ↓
Meta   Evolution   megaAPI
```

---

# 4. Meta WhatsApp Cloud API

## Papel

Baseline oficial de produção.

## Uso

- inbound;
- outbound;
- templates;
- status;
- mídia;
- webhooks;
- atendimento;
- automações.

## Dependências

- Meta Business;
- WABA;
- número;
- tokens;
- permissões;
- templates;
- opt-in;
- políticas.

---

# 5. Evolution API

A Evolution API atual suporta:

- WhatsApp Cloud API oficial;
- modo Baileys/WhatsApp Web;
- REST;
- Chatwoot;
- Typebot;
- OpenAI;
- filas/eventos;
- storage;
- webhooks.

## Uso recomendado

Avaliar como camada operacional/self-host.

Registrar explicitamente o `connection_type` usado por instância.

Se `BAILEYS`, classificar como modo alternativo/não oficial e aplicar política de risco.

---

# 6. megaAPI

Tratar como gateway de terceiros.

A oferta atual possui diferentes planos/endpoints e divulga integrações para mensagens/webhooks.

Antes do uso:

- identificar plano;
- identificar mecanismo real de conexão;
- confirmar se é Cloud API oficial ou conector alternativo;
- avaliar SLA;
- segurança;
- retenção;
- contrato;
- risco de bloqueio.

---

# 7. Adapter de mensageria

Modelo:

```ts
type ChannelProvider = "meta" | "evolution" | "megaapi";

interface MessagingProvider {
  sendText(...)
  sendMedia(...)
  sendTemplate(...)
  markAsRead(...)
  healthCheck(...)
  normalizeWebhook(...)
}
```

## Modelo interno normalizado

```text
provider
provider_account_id
external_message_id
conversation_id
contact_id
direction
type
content
delivery_status
sent_at
delivered_at
read_at
failed_at
raw_event_ref
```

---

# 8. Instagram

Integração prevista:

- mensagens;
- webhooks;
- identificação do perfil;
- histórico;
- encaminhamento ao CRM.

Confirmar:

- conta profissional;
- Meta Business;
- permissões;
- política.

---

# 9. E-mail

Usos:

- notificações;
- formulários;
- documentos;
- comunicação transacional.

Provedor a decidir.

---

# 10. n8n

Responsabilidades:

- webhook routing;
- sync;
- scheduled jobs;
- follow-up;
- IA;
- notificações;
- transformações não críticas.

Não usar como único local de regras essenciais.

---

# 11. Financeiro / banco

Fase inicial:

- OFX/CSV;
- importação;
- conciliação assistida.

Integração bancária direta futura dependerá do banco e escopo.

---

# 12. NFS-e

Pendente:

- município;
- provedor;
- credenciais;
- modelo fiscal;
- orientação contábil.

Não automatizar antes da validação.

---

# 13. Segurança de integração

- segredo em vault/env;
- assinatura de webhook quando disponível;
- idempotency key;
- retry com backoff;
- dead-letter/erro;
- logs sem segredo;
- rate limit;
- circuit breaker quando necessário;
- health check.

---

# 14. Fontes oficiais

Verificadas em 2026-09-04:

- Sympla docs: https://developers.sympla.com.br/api-doc/
- Sympla OpenAPI: https://developers.sympla.com.br/api-docs
- Meta: https://developers.facebook.com/documentation/business-messaging/whatsapp/about-the-platform
- Evolution: https://github.com/evolution-foundation/evolution-api
- megaAPI: https://megaapi.io/
