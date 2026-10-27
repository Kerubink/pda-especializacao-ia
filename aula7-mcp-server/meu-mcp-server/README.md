# meu-mcp-server (esqueleto)

Esqueleto de MCP server em TypeScript, transporte stdio, usando o SDK oficial
`@modelcontextprotocol/server`.

## Antes de tocar em `src/index.ts`

Preencha `../decisao-escopo-template.md` (copie pra raiz do seu projeto como
`DECISAO-ESCOPO.md`) — ver `GUIA-DO-ALUNO.md`, Lab 1, passo 1.

## Uso

```bash
npm install
npm run build
claude mcp add --transport stdio meu-server -- node build/index.js
```

Dentro do Claude Code: `/mcp` deve mostrar `meu-server` conectado.

## O que já vem pronto

- `src/index.ts` — server com uma tool de exemplo (`ping`) funcionando de ponta a ponta, e
  comentários `// TODO` marcando onde entra a sua tool real.

## O que você preenche

Os `// TODO` de `src/index.ts`: nome, descrição e schema de input da sua tool, e a lógica
que ela executa — sempre respeitando o que `DECISAO-ESCOPO.md` diz que ela NÃO pode fazer.
