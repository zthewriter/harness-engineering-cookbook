# Write pages a harness can cite

A harness retrieves passages. A page that answers one question, in the words a developer will type, is a page the retrieval can return. A page that answers four questions in an introduction is a page it will miss.

## You will have

A style guide and a set of pages that each open on the question they answer.

## Steps

1. List the questions implementations keep missing. Sort them into what you promise, why it is this way, how it is done here, and what just changed.
2. Give each question one page. The title is the question, or the task. The first paragraph answers it. Steps are an ordered list. A version claim names the version.
3. Use the term the developer will type. If they say "login" and the page only says "authentication," retrieval has nothing to match. Put the word they use in the title or the first paragraph. [Context for AI](https://github.com/zthewriter/context-for-ai) is the longer version of this, including how a page becomes passages.
4. Keep the always-loaded guide short. Voice, the terms, and "one page per task" go in `AGENTS.md`. The pages themselves do not. Point `AGENTS.md` at the docs URL.
5. Do not invent a command to fill a gap. A missing step is a page to write, not a sentence for the agent to guess.

## How you know it worked

Read a page out of context, as if it were the only paragraph an agent received. It still answers its question. It does not depend on the previous heading.

## The tool

The pages are the sources. A context server is RAG exported as an MCP server: it retrieves passages from these pages and serves that retrieval at an MCP endpoint. Writing the page is what makes the retrieval possible. The next recipe is the export.

## Also read

- [Context for AI](https://github.com/zthewriter/context-for-ai): templates and the ten practices for pages an agent can use.
- [Ship with AI](https://github.com/zthewriter/ship-with-ai): what the developer on the other end is building.
- [Awesome Context Observability](https://github.com/zthewriter/awesome-context-observability): how to see which of your passages an answer used.
