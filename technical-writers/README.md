# Technical writers

You write the pages a harness is allowed to cite, and you publish those pages as a context pipeline. The people who run the harness, developers and the agents in their editors, call that pipeline instead of guessing.

You are doing context engineering when you decide which page answers which question and put that page on an MCP server.

A context server is RAG exported as an MCP server. RAG retrieves the passage. The MCP server is the export a harness connects to. [Choose a context server](../recipes/choose-a-context-server.md) lists options.

How to write the page so a passage can stand alone is [Context for AI](https://github.com/zthewriter/context-for-ai).

| Recipe | You will have |
| --- | --- |
| [Write pages a harness can cite](01-write-pages-a-harness-can-cite.md) | One question per page, terms that match the question |
| [Export the docs as an MCP server](02-export-the-docs.md) | A server, a source rule, and a citation you checked |
| [Hand the server to the developer](03-hand-off-the-server.md) | An endpoint, a token if it is private, and a question that proves it |

## Delivery recipes

The following shared recipes deliver your docs to agents through the channels this
role works with:

- [Publish Markdown and llms.txt](../recipes/06-publish-markdown-and-llms-txt.md)
- [Serve docs from an MCP server](../recipes/07-serve-docs-from-an-mcp-server.md)
- [Prove the citation](../recipes/11-prove-the-citation.md)
- [Observe delivered context](../recipes/12-observe-delivered-context.md)

## Also read

- [Ship with AI](https://github.com/zthewriter/ship-with-ai)
- [Context for AI](https://github.com/zthewriter/context-for-ai)
- [Awesome Context Observability](https://github.com/zthewriter/awesome-context-observability)
