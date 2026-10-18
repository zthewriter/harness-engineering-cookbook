# Developers

You use the harness to build. The context is not something you recreate. Technical writers, docs engineers, context engineers, and developer advocates already published it as MCP servers. You connect those servers, and you write code against what they cite.

When they have not covered a repo you own, you can put that repo on a server of your own. That is the exception, not the default.

A context server is RAG exported as an MCP server. [Choose a context server](../recipes/choose-a-context-server.md) lists options. The servers you connect are that export: retrieval over their sources, spoken as MCP.

| Recipe | You will have |
| --- | --- |
| [Call the servers they already shipped](01-call-the-servers.md) | Their endpoint in your editor, checked with their proof question |
| [Put the endpoint in the harness](02-endpoint-in-the-harness.md) | A guide that names which server answers which question |
| [When you need a server they have not built](03-a-server-of-your-own.md) | One server for your repo, private if the repo is |

## Delivery recipes

The following shared recipes deliver your docs to agents through the channels this
role works with:

- [Serve docs from an MCP server](../recipes/07-serve-docs-from-an-mcp-server.md)
- [Expose docs search through an API](../recipes/08-expose-docs-search-through-an-api.md)
- [Ship context in the repo](../recipes/09-ship-context-in-the-repo.md)

## Also read

- [Ship with AI](https://github.com/zthewriter/ship-with-ai)
- [Context for AI](https://github.com/zthewriter/context-for-ai)
- [Awesome Context Observability](https://github.com/zthewriter/awesome-context-observability)
