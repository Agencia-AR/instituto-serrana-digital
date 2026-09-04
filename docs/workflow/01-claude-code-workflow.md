---
project: Instituto Serrana Digital
document: Claude Code Workflow
version: "1.0"
date: 2026-09-04
---

# Fluxo Claude Code

Este documento detalha o fluxo de trabalho. As regras curtas e a ordem de leitura
canônica vivem em `CLAUDE.md` e no `README.md` — não repita listas de leitura
aqui.

# 1. Antes de trabalhar

Siga a ordem de leitura do `README.md` e abra o documento específico da tarefa.

# 2. Primeiro ciclo (somente leitura)

```text
Leia os documentos.
Não altere nada.

Entregue:
1. resumo do produto;
2. decisões;
3. propostas;
4. pendências;
5. riscos;
6. inconsistências;
7. próximo lote recomendado.
```

# 3. Antes de escrever no Penpot

```text
1. confirmar arquivo;
2. confirmar página;
3. listar componentes;
4. listar tokens;
5. detectar duplicações;
6. propor plano;
7. aguardar aprovação.
```

# 4. Antes de implementar código

```text
1. mapear requisito;
2. mapear design;
3. mapear componente existente;
4. propor arquivos;
5. listar migrations;
6. listar testes;
7. listar riscos.
```

# 5. ADR

Quando houver mudança arquitetural relevante, criar um registro em
`docs/architecture/decisions/` a partir de `ADR-0000-template.md`. Ver o índice
em `docs/architecture/decisions/README.md`.

# 6. Git

- um objetivo por commit;
- sem secrets;
- sem `reset --hard`;
- sem `force push`;
- `git status` antes e depois.

# 7. Tarefa imediata recomendada

1. gerar roteiro da reunião usando `prompts/discovery-presentation.md`;
2. preparar estrutura Penpot;
3. criar protótipo;
4. validar em reunião;
5. atualizar `docs/product/01-prd.md` e `docs/discovery/02-decisions-assumptions.md`.
