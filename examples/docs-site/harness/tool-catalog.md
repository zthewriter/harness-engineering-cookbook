# Tool catalog

This page lists every tool an agent may call while working on the docs or answering
from them, with its permission level. The levels are defined in
[Guardrails and approvals](guardrails.md).

## Tools

The following table lists each tool:

| Tool | Provided by | Used for | Permission level | Owner |
|---|---|---|---|---|
| Search the docs | Context server | Find passages that answer a question | Read | Docs team |
| Get a page | Context server | Return one page by URL | Read | Docs team |
| [Custom tool] | Context server | [The question your team keeps asking] | Read | Docs team |
| Build and preview the site | Docs repository commands | Check a change renders | Read | Docs engineers |
| Open a pull request | Git host | Propose a change | Write | The person who asked |

The public context server exposes read tools only. A tool that changes something,
such as opening a ticket, belongs on a separate server with its own access.
