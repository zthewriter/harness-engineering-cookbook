# Split memory from retrieval

A harness has two places context can live. One is loaded at the start of every session. The other is retrieved when the task needs it. Putting the docs in the first place crowds out the task. Putting the rules in the second place means the agent forgets them.

## You will have

A guide short enough to load every time, and an MCP server for everything that is only needed for the current question.

## Steps

1. Put only standing rules in `AGENTS.md`: voice, the terms, which server to call for which question, and what the agent must not do. If it is longer than a page, it is hiding a document that belongs on the server.
2. Put pages, repos, and files on the server. The agent asks. It receives the passages for that question. It does not receive the corpus.
3. A fact that must survive into the next session, and that is about the task rather than the docs, goes in the handoff note the guide already requires. It does not go into the server, and it does not stay only in the chat.
4. Give each audience its own server. A public quickstart and an internal runbook do not share an endpoint.
5. Write the developer's instructions as "call this endpoint," not "here is a folder." The [developer recipes](../developers/README.md) are the receiving side.

## How you know it worked

You can delete the docs from the editor's context window and the agent still answers from the server. You can start a fresh session and the voice rules are still in force, because they were in the guide.

## The tool

A context server is RAG exported as an MCP server. This recipe is the decision to use one for the retrieval half. RAG selects the passages for the question. The MCP server is how every harness in the company calls that selection, with the same sources and the same rules, instead of each person pasting a different excerpt.

## Also read

- [Context for AI](https://github.com/zthewriter/context-for-ai): how content becomes passages and passages become answers.
- [Awesome Context Observability](https://github.com/zthewriter/awesome-context-observability): seeing what was retrieved.
- [Ship with AI](https://github.com/zthewriter/ship-with-ai): the same split, explained for someone shipping an app.
