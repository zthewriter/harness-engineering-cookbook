# Context engineers

You own the split between what the harness loads every time and what it retrieves when asked. Writers supply the pages. Docs engineers run the publish check. You decide the pipeline: memory, retrieval, the MCP export, and what the developer is handed.

A context server is RAG exported as an MCP server. It is the retrieval half. [Choose a context server](../recipes/choose-a-context-server.md) lists options. `AGENTS.md` is the memory half. They are not substitutes.

| Recipe | You will have |
| --- | --- |
| [Split memory from retrieval](01-split-memory-from-retrieval.md) | A short guide, and everything else on a server |
| [Rules and custom tools](02-rules-and-custom-tools.md) | The two controls on what the server returns |
| [Keep one endpoint current](03-keep-the-endpoint-current.md) | A refresh habit and a reading of what came back empty |

## Delivery recipes

The following shared recipes deliver your docs to agents through the channels this
role works with:

- [Serve docs from an MCP server](../recipes/07-serve-docs-from-an-mcp-server.md)
- [Ship context in the repo](../recipes/09-ship-context-in-the-repo.md)
- [Keep delivered context current](../recipes/10-keep-delivered-context-current.md)
- [Observe delivered context](../recipes/12-observe-delivered-context.md)

## Also read

- [Ship with AI](https://github.com/zthewriter/ship-with-ai)
- [Context for AI](https://github.com/zthewriter/context-for-ai)
- [Awesome Context Observability](https://github.com/zthewriter/awesome-context-observability)
