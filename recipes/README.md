# recipes/

This folder is the shared map of a harness. It is not a persona, and it is not where the steps for your job live.

A harness is the environment around a model: what it reads first, what it is allowed to see, which tools it may call, and where a person still approves the result. These four files explain those parts once. The persona folders use them.

| File | Part | What it explains |
| --- | --- | --- |
| [01-guides.md](01-guides.md) | Guides | The short file the agent reads before it acts. Voice, terms, and one task at a time. Not the docs. |
| [02-context-engineering.md](02-context-engineering.md) | Context | Retrieval, memory, MCP, and which source a task may use. This is the part a context server is for: RAG exported as an MCP server. |
| [03-tool-orchestration.md](03-tool-orchestration.md) | Tools and sensors | The actions the agent may take, and the check that has to pass before the work counts as done. |
| [04-guardrails.md](04-guardrails.md) | Guardrails | Who may call the server, how far the agent may go, and what a person still approves. |
| [05-walk-the-pipeline.md](05-walk-the-pipeline.md) | Pointer | Not a fifth part. It sends you to the persona folder for your job. |
| [choose-a-context-server.md](choose-a-context-server.md) | Selection | The capabilities the recipes need, how to check them, and options. |

## Delivery recipes

The parts above describe the harness. The following recipes deliver your
documentation into it, one channel each. Each recipe links to the matching template
in [Context for AI](https://github.com/zthewriter/context-for-ai).

| File | Delivers docs through |
| --- | --- |
| [06-publish-markdown-and-llms-txt.md](06-publish-markdown-and-llms-txt.md) | Static Markdown files and an `llms.txt` file agents can fetch |
| [07-serve-docs-from-an-mcp-server.md](07-serve-docs-from-an-mcp-server.md) | An MCP endpoint |
| [08-expose-docs-search-through-an-api.md](08-expose-docs-search-through-an-api.md) | A search endpoint other systems call |
| [09-ship-context-in-the-repo.md](09-ship-context-in-the-repo.md) | `AGENTS.md`, rules files, and skills next to the code |
| [10-keep-delivered-context-current.md](10-keep-delivered-context-current.md) | Refresh on publish, a context changelog, and a regression question set |
| [11-prove-the-citation.md](11-prove-the-citation.md) | Known questions, checked against the page each answer cites |
| [12-observe-delivered-context.md](12-observe-delivered-context.md) | The signals that show how delivered docs are used |

Start in the folder for your job. The list is on the [repository README](../README.md#start-in-your-folder).
