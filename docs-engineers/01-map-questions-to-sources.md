# Map questions to sources

A harness that searches "all the docs" returns the first page that shares words with the question. Your job is to decide, ahead of time, which source is allowed to answer which kind of question.

## You will have

A short map. The developer can read it. The server is built from it.

## Steps

1. List the questions the team actually asks. Group them: install, a specific task, an API shape, what changed, an example.
2. Assign one source to each group. The docs site for tasks. The repo for examples. The changelog for what changed. Do not assign two sources to the same question unless you can say which one wins.
3. Write the map where the harness can see it, as a few lines in `AGENTS.md`: "For a procedure, call the docs server. For a sample, call the examples server."
4. Mark anything that must not be public. Those sources go on a private server, not on the one customers can call.
5. If a question has no source, it is a page to commission from the writer. It is not a source to invent.

## How you know it worked

You can point at one URL for "how do I reset a token" and a different URL for "what changed in the last release." Nobody has to search the site to find out which.

## The tool

A context server is RAG exported as an MCP server. Each row of the map becomes a source on that server, or its own server when the audiences differ. RAG retrieves from those sources. The MCP endpoint is the export the developer connects. The next recipe builds it.

## Also read

- [Context for AI](https://github.com/zthewriter/context-for-ai): how a page is split into the passages retrieval returns.
- [Awesome Context Observability](https://github.com/zthewriter/awesome-context-observability): how you see whether the map matches what agents actually asked.
- [Ship with AI](https://github.com/zthewriter/ship-with-ai): the plain-language account of RAG, if you are explaining the map to someone who does not run the pipeline.
