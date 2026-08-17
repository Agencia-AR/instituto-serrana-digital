# START HERE — preparação no Cursor

## 1. Abrir o projeto

No Cursor, na tela inicial, clique em **Open project** e selecione esta pasta:

`instituto-serrana-digital`

## 2. Inicializar Git

Abra `Terminal → New Terminal` e execute:

```bash
git init
git add .
git commit -m "chore: bootstrap Instituto Serrana Digital workspace"
```

Se o Git ainda não estiver configurado com nome/e-mail, faça isso antes do commit.

## 3. Validar o contexto

No Agent do Cursor ou no Claude Code, use:

```text
Leia CLAUDE.md e docs/00-master/MASTER.md.
Não altere nada.
Resuma as decisões confirmadas, as hipóteses e o próximo lote de trabalho.
```

## 4. Configurar Penpot MCP

Não cole a chave diretamente nos arquivos do repositório.

No Penpot:
1. `Your account → Integrations`;
2. habilite `MCP Server`;
3. gere a MCP key;
4. copie a URL completa fornecida;
5. mantenha a chave fora de prints e commits.

No terminal, para a sessão atual:

```bash
export PENPOT_MCP_URL='COLE_AQUI_A_URL_COMPLETA_FORNECIDA_PELO_PENPOT'
```

Depois reinicie/recarregue as ferramentas MCP do Cursor/Claude Code.

No Penpot, abra o arquivo correto e use:

`File → MCP Server → Connect`

## 5. Primeiro teste MCP

Faça somente leitura:

```text
Use o MCP do Penpot.
Confirme o arquivo e a página atualmente abertos.
Liste páginas, componentes e tokens.
Não modifique nada.
```

## 6. Próximo lote

Construir Foundations e o protótipo para a reunião, conforme:
`docs/02-product/PROTOTYPE-SCOPE.md`.
