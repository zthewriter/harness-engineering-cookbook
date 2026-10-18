# Build the pipeline

The pipeline is sources in, passages out, served as an MCP server. You build it once. The harness calls it on every task.

## You will have

One endpoint per audience, with a source rule for the source that must ride along, and a custom tool for the question plain search keeps missing.

## Steps

1. On your context server, add the sources from the map: a docs site, a GitHub repo, a website, an uploaded file, or another MCP server, whichever your server can ingest. Treat another MCP server as a source to read from, not as actions to pass through to the harness.
2. Split audiences onto separate servers when one of them is internal. The public server has public sources only.
3. Add a source rule where the map says a source should be present even if the question never names it, if your server supports one. Example: "When the question is what changed, use the changelog." Know which kind of rule you wrote. One that always includes the source returns a passage from it. One that only prefers it raises its rank.
4. Add a custom tool, if your server supports one, for a recurring question the built-in tools phrase differently from your readers. Describe the outcome in a sentence: "Return the install steps for this platform and the page they came from."
5. Deploy. Ask one question from each row of the map. Write down the citation you got.

## How you know it worked

Each row's question cites the source you assigned. A miss means the page and the question do not share words, or the rule omitted the words people type. Fix the page with the writer, or rewrite the rule sentence. Then refresh.

## The tool

A context server is RAG exported as an MCP server. This recipe is that export. RAG retrieves the passages. MCP is the protocol the harness already speaks, so the endpoint drops into Cursor, Claude, or any other client without a second integration. Sources, source rules, and custom tools are the controls on what comes back.

<details>
<summary>Doing this in MCP Studio</summary>

MCP Studio by Appa Tools is one option. Disclosure: maintained by the author of this repo.

1. In [MCP Studio](https://appatools.com/mcp-studio/studio), add the sources. The [source guide](https://docs.appatools.com/mcp-studio/guides/adding-sources) covers each type. Another MCP server added as a source is read from and does not pass its tools through.
2. A source rule is called a retrieval rule. Its preview says "Always include" or "Prefer" and lists the words that fire it. The [retrieval rules guide](https://docs.appatools.com/mcp-studio/guides/retrieval-rules) covers the limits, including the rules that are refused.
3. See [custom tools](https://docs.appatools.com/mcp-studio/guides/custom-tools).

</details>

## Also read

- [Context for AI](https://github.com/zthewriter/context-for-ai): writing and structuring the sources.
- [Awesome Context Observability](https://github.com/zthewriter/awesome-context-observability): tracing what the pipeline returned.
- [Ship with AI](https://github.com/zthewriter/ship-with-ai): how a builder consumes a server like this.
