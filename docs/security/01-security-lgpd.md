---
project: Instituto Serrana Digital
document: Security and LGPD
version: "1.0"
date: 2026-09-04
---

# Segurança, Privacidade e LGPD

# 1. Bases normativas de referência

- Constituição Federal, art. 5º, X — intimidade, vida privada, honra e imagem;
- Constituição Federal, art. 5º, XII — sigilo das comunicações, nos termos constitucionais;
- Lei nº 13.709/2018 — LGPD;
- Marco Civil da Internet — Lei nº 12.965/2014;
- orientações da ANPD aplicáveis.

Este documento é requisito técnico e de governança; validações jurídicas específicas devem ser feitas quando necessário.

---

# 2. Papéis preliminares

## Controlador

Instituto Serrana, para dados tratados conforme suas finalidades institucionais.

## Operador

Agência AR, na medida em que tratar dados por instrução do Instituto.

## Terceiros

- Sympla;
- Meta;
- provedores de WhatsApp;
- e-mail;
- hosting;
- analytics;
- IA.

O papel de cada terceiro deve ser avaliado conforme contrato e finalidade.

---

# 3. Princípios

- finalidade;
- adequação;
- necessidade;
- transparência;
- segurança;
- prevenção;
- responsabilização.

---

# 4. Classificação de dados

## Público

- páginas;
- eventos;
- projetos;
- documentos publicados.

## Interno

- operações;
- fornecedores;
- tarefas;
- indicadores.

## Pessoal

- nome;
- e-mail;
- telefone;
- mensagens;
- pedidos;
- participação.

## Sensível/alto impacto operacional

- documentos;
- dados financeiros;
- credenciais;
- informações de equipe.

---

# 5. Autenticação

- e-mail;
- senha robusta;
- recuperação segura;
- MFA para perfis sensíveis;
- timeout;
- revogação;
- sessão auditável.

---

# 6. Autorização

RBAC + RLS.

Perfis não devem receber dados desnecessários.

Exemplo:

- atendimento não precisa ver todo financeiro;
- check-in não precisa ver documentos;
- comunicação não precisa acessar contratos privados.

---

# 7. Segredos

Nunca versionar:

- tokens;
- API keys;
- service role;
- WABA tokens;
- Sympla token;
- MCP key;
- passwords.

Usar:

- `.env`;
- secret manager;
- variáveis do runtime.

---

# 8. Logs

Logs não devem registrar:

- token;
- senha;
- conteúdo desnecessário;
- documento pessoal integral.

Logs sensíveis devem ter acesso restrito.

---

# 9. Webhooks

- autenticação/assinatura;
- idempotência;
- replay protection quando possível;
- rate limit;
- schema validation;
- auditoria.

---

# 10. Storage

- bucket público apenas quando necessário;
- arquivos privados com signed URLs;
- policies;
- malware/content checks quando aplicável;
- retenção.

---

# 11. Consentimento e preferências

Registrar quando aplicável:

- opt-in de marketing;
- canal;
- data;
- origem;
- revogação.

Mensagens transacionais e marketing devem ser distinguidos.

---

# 12. Direitos do titular

Preparar processo para:

- confirmação;
- acesso;
- correção;
- eliminação/anominização quando aplicável;
- informação de compartilhamento;
- revogação.

---

# 13. Retenção

Definir tabela de retenção após discovery.

Exemplo de categorias:

- CRM;
- pedidos;
- documentos contábeis;
- mensagens;
- logs;
- projetos;
- contratos.

Retenção deve considerar obrigações legais e finalidade.

---

# 14. IA

## Política

- minimizar dados enviados;
- não enviar segredo;
- não usar dados além da finalidade;
- registrar automações relevantes;
- supervisão humana para decisões críticas.

## Proibido

- decisão financeira autônoma;
- autorização de reembolso;
- alteração de preço;
- exposição de dados entre usuários;
- inferências sensíveis desnecessárias.

---

# 15. Backup

- criptografia;
- controle de acesso;
- retenção;
- restauração testada.

---

# 16. Incidentes

Criar procedimento:

```text
detectar
→ conter
→ preservar evidência
→ avaliar impacto
→ corrigir
→ comunicar responsáveis
→ avaliar dever de comunicação
→ registrar lições
```

---

# 17. Checklist de release

- RLS revisada;
- RBAC revisado;
- secrets auditados;
- dependências auditadas;
- logs revisados;
- endpoints protegidos;
- CORS;
- headers;
- rate limit;
- backup;
- restore;
- privacy notice;
- termos.
