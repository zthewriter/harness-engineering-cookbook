# Keep one endpoint current

A context pipeline rots when the page changes and the server does not, or when people ask questions the sources cannot answer and nobody writes the page.

## You will have

A refresh after each docs publish, and a weekly look at questions the server could not answer.

## Steps

1. Tie refresh to the docs release, not to a calendar guess, for example as the last job in the docs build. [Refresh on publish](../recipes/10-keep-delivered-context-current.md#1-refresh-on-publish) shows how. The source updates, then you ask yesterday's proof question, the question whose citation you already checked, and confirm the citation is the new page.
2. Read the questions that came back empty or off the sources. Each one is either a missing page, a page that does not use the reader's words, or a question this server should not answer. Write that down. Hand the first two to the writer. Refuse the third in the guide, so the agent stops trying.
3. Use the retrieval log you have. Know which numbers your server shows, which need a paid tier, and which you would have to log yourself. If your server logs nothing, [observe delivered context](../recipes/12-observe-delivered-context.md) shows what to record. A wider map of this kind of tooling is [Awesome Context Observability](https://github.com/zthewriter/awesome-context-observability).
4. When you retire a source, disconnect it. The server should stop being able to cite it. Confirm with the proof question.
5. Tell the developers when the endpoint stays the same and the sources changed. They should not need a new config. They should know the citations moved.

## How you know it worked

The proof question cites this week's page. The empty-question list got shorter because a page was written, not because someone told the agent to stop mentioning gaps.

## The tool

A context server is RAG exported as an MCP server. Keeping it current is keeping the RAG index on the pages you mean, and keeping the MCP endpoint stable so every harness that calls it stays pointed at the same place. You change sources, rules, and tools. You do not ask each developer to re-paste the docs.

<details>
<summary>Doing this in MCP Studio</summary>

MCP Studio by Appa Tools is one option. Disclosure: maintained by the author of this repo.

How often the server is asked is on the free dashboard. The passage behind an answer is a paid analytics tier. The [analytics guide](https://docs.appatools.com/mcp-studio/guides/action-predictive-analytics) says which is which.

</details>

## Also read

- [Context for AI](https://github.com/zthewriter/context-for-ai): tracing an answer back to a passage.
- [Awesome Context Observability](https://github.com/zthewriter/awesome-context-observability): the category of tools that show that trace.
- [Ship with AI](https://github.com/zthewriter/ship-with-ai): what a stale answer costs the person building the app.
