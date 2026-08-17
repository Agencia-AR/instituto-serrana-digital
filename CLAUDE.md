# CLAUDE.md — Instituto Serrana Digital

## Antes de qualquer trabalho

Leia:
- `docs/00-master/MASTER.md`
- `docs/06-decisions/DECISIONS.md`
- o documento específico da área em que vai atuar.

## Fontes da verdade

- Produto/regras: Documento Mestre.
- Visual: Penpot.
- Tokens: `packages/design-tokens`.
- Código: repositório Git.

## Regras

- Diferencie `CONFIRMADO`, `PROPOSTA` e `PENDENTE`.
- Não invente dados institucionais.
- O design pode avançar com hipóteses marcadas como proposta.
- Não modifique Penpot antes de uma leitura/auditoria inicial.
- Nunca exponha tokens, chaves, `.env` ou URLs MCP com segredo.
- WhatsApp deve usar adapter multprovedor; Meta Cloud API é o baseline de produção.
- Evolution/MegaAPI em modo não oficial exigem avaliação e aceite de risco.
- Sympla é a fonte oficial da venda na primeira etapa.
- Não faça ações Git destrutivas sem solicitação explícita.
- Faça alterações pequenas, verificáveis e reversíveis.
