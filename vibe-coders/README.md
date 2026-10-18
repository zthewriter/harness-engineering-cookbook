# Vibe coders

Use a harness while you build. The editor writes the app. The harness is the three lines it reads first, and the MCP server it asks before it invents a step.

A context server is RAG exported as an MCP server. RAG means it retrieves the passages that answer a question from the sources you give it, such as the docs for the stack you chose. The export is the endpoint you connect in the editor. [Choose a context server](../recipes/choose-a-context-server.md) lists options.

The build guides live in [Ship with AI](https://github.com/zthewriter/ship-with-ai). These recipes are the harness around that build.

| Recipe | You will have |
| --- | --- |
| [Set the guide before you build](01-set-the-guide.md) | Three lines the editor reads on every task |
| [Connect the docs as an MCP server](02-connect-the-docs.md) | The stack's docs, retrieved and callable |
| [Check the citation, then build](03-check-then-build.md) | A rule that you do not continue on the wrong page |

## Delivery recipes

The following shared recipes deliver your docs to agents through the channels this
role works with:

- [Ship context in the repo](../recipes/09-ship-context-in-the-repo.md)
- [Serve docs from an MCP server](../recipes/07-serve-docs-from-an-mcp-server.md)

## Also read

- [Ship with AI](https://github.com/zthewriter/ship-with-ai)
- [Context for AI](https://github.com/zthewriter/context-for-ai)
- [Awesome Context Observability](https://github.com/zthewriter/awesome-context-observability)
