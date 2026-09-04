---
project: Instituto Serrana Digital
document: Decisions and Assumptions
version: "1.0"
date: 2026-09-04
---

# Decisões, Propostas e Pendências

# 1. Decisões

| Tema | Estado | Decisão |
|---|---|---|
| Produto | DECISÃO | Instituto Serrana Digital |
| Ambientes | DECISÃO | Portal Público + Administrativo |
| Design | DECISÃO | Penpot |
| Design-to-code | DECISÃO | Penpot MCP + Claude Code/Cursor |
| Home | DECISÃO | inicia na base e sobe até Santa Rita |
| Venda inicial | DECISÃO | Sympla permanece fonte oficial |
| WhatsApp | DECISÃO | arquitetura multiprovedor |
| WhatsApp produção | DECISÃO | Meta Cloud API como baseline |
| Discovery | DECISÃO | não bloqueia protótipo |

---

# 2. Propostas

| Tema | Proposta |
|---|---|
| domínio | `www.institutoserrana.org.br` |
| admin | `app.institutoserrana.org.br` |
| mapa A | urbano ilustrado |
| mapa B | operacional |
| stack | Next.js + Supabase + n8n |
| deployment | container-ready; VPS/Coolify ou gerenciado a confirmar |

---

# 3. Confirmado por fonte pública

- Instituto Serrana ONG existe e possui site público;
- site informa criação em 27/09/2001;
- missão/visão/valores estão publicados;
- atuação pública abrange patrimônio, cultura, turismo e desenvolvimento;
- domínio atual observado: `institutoserrana.org`;
- projetos públicos identificados no site atual: Afromineiridades; Eu Amo, Eu
  Preservo; Mapa Cartográfico dos Chafarizes e Fontes Públicas; publicações
  históricas; Carnaval; Festa do Queijo; Seminário Internacional Bateia;
  Festival Sabores do Queijo; e projetos de patrimônio, cultura e inclusão;
- termo de fomento com a Prefeitura do Serro para restauro/preservação de bens
  públicos (fonte: portal oficial do município).

---

# 4. Pendente

- domínio `.org.br`;
- estatuto atual;
- CNPJ/documentos;
- diretoria atualizada;
- acesso ao domínio;
- contrato Sympla;
- token Sympla;
- mapa real/dimensões;
- financeiro;
- NFS-e;
- Meta Business;
- número WhatsApp;
- provedor final;
- usuários;
- política de transparência;
- materiais finais;
- cronograma;
- orçamento.

---

# 5. Regra de alteração

Uma `PROPOSTA` só vira `DECISÃO` depois de:

- validação do responsável;
- registro da data;
- atualização deste arquivo;
- ajuste do PRD, se impactado.

---

# 6. Log

## 2026-09-04

- consolidação do PRD;
- atualização do Sympla para documentação pública v1.6.0 observada;
- manutenção do modelo multiprovedor de WhatsApp;
- preparação do pacote para Claude Code.
