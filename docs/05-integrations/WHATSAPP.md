# Estratégia WhatsApp

## Provedores

### Meta WhatsApp Cloud API
Status: baseline de produção.

### Evolution API
Pode atuar:
- com Cloud API oficial;
- com WhatsApp Web/Baileys (não oficial).

### MegaAPI
Gateway não oficial para avaliar como alternativa/contingência.

## Arquitetura

`CRM → MessagingProvider → provider adapter`

Adapters:
- `MetaWhatsAppProvider`
- `EvolutionWhatsAppProvider`
- `MegaApiWhatsAppProvider`

## Regra

Nunca acoplar lógica de CRM diretamente ao payload de um provedor.

## Risco

Modos não oficiais dependem de tecnologia não homologada e podem sofrer bloqueio/interrupção. Devem ter aceite de risco e possibilidade de troca rápida.

## Fontes
- Meta: https://developers.facebook.com/documentation/business-messaging/whatsapp/about-the-platform
- WhatsApp Terms: https://www.whatsapp.com/legal/terms-of-service
- Evolution: https://github.com/evolution-foundation/evolution-api
- MegaAPI: https://www.megaapi.com.br/
