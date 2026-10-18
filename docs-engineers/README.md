# Docs engineers

You build the context pipeline the harness calls. The writer owns the sentence. You own which source answers which question, whether the server is current, and whether the citation is the page you just shipped.

That is context engineering: the retrieval, the export, and the check.

A context server is RAG exported as an MCP server. RAG is the retrieval. The MCP server is the thing the harness connects to. [Choose a context server](../recipes/choose-a-context-server.md) lists options.

| Recipe | You will have |
| --- | --- |
| [Map questions to sources](01-map-questions-to-sources.md) | One source per kind of question |
| [Build the pipeline](02-build-the-pipeline.md) | A server, rules, and a tool for the question the search misses |
| [Prove the new page is the one cited](03-prove-the-citation.md) | A check you run after every publish |

## Delivery recipes

The following shared recipes deliver your docs to agents through the channels this
role works with:

- [Publish Markdown and llms.txt](../recipes/06-publish-markdown-and-llms-txt.md)
- [Serve docs from an MCP server](../recipes/07-serve-docs-from-an-mcp-server.md)
- [Expose docs search through an API](../recipes/08-expose-docs-search-through-an-api.md)
- [Keep delivered context current](../recipes/10-keep-delivered-context-current.md)
- [Prove the citation](../recipes/11-prove-the-citation.md)
- [Observe delivered context](../recipes/12-observe-delivered-context.md)

## Also read

- [Ship with AI](https://github.com/zthewriter/ship-with-ai)
- [Context for AI](https://github.com/zthewriter/context-for-ai)
- [Awesome Context Observability](https://github.com/zthewriter/awesome-context-observability)
