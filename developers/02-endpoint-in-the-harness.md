# Put the endpoint in the harness

A server you connected once and then forgot is not part of the harness. The guide has to name it, or the next session will invent a procedure from the model instead of calling it.

## You will have

A few lines in the editor rules that say which MCP server answers which kind of question, and a check before you merge.

## Steps

1. Add lines like these to the project guide:

   ```text
   Procedures: call the docs MCP server. Do not invent a command it did not cite.
   Samples: call the sample tool they named.
   What changed: call the docs server and ask for the changelog.
   Internal runbooks: the private server only. Never paste its answers into a public issue.
   ```

2. Keep those lines short. The pages stay on their server. [Context engineers](../context-engineers/01-split-memory-from-retrieval.md) made that split on purpose.
3. Scope the task to one change. The agent may edit the files in this task. It may not publish, open a PR, or install a package the cited page did not name.
4. Before you merge, read the citation on any code that came from the docs. The line in the diff should match the page. If the page is wrong, send it back to the writer. If the code is wrong, change the code.
5. When their server says the answer is not in the sources, stop. That is a missing page, not permission to guess.

## How you know it worked

A fresh session, given only the guide, calls their server for a procedure and refuses to invent the command when the server has nothing.

## The tool

A context server is RAG exported as an MCP server. The endpoint in your guide is that export. Every call retrieves passages from their sources and returns them over MCP, which is why the same server works in the editor, the terminal client, and the agent that opens the PR. You hold the guide. They hold the RAG index.

## Also read

- [Ship with AI](https://github.com/zthewriter/ship-with-ai): the stack choice and the prompts, beside this harness.
- [Context for AI](https://github.com/zthewriter/context-for-ai): how their pages were written to be retrieved.
- [Awesome Context Observability](https://github.com/zthewriter/awesome-context-observability): the view from their side of the questions you asked.
