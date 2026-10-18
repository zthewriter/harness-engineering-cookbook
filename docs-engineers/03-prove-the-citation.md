# Prove the new page is the one cited

A publish is finished when the harness cites the new page. A green build of the docs site does not tell you that.

## You will have

One question per important page, asked against the server after the refresh, with the citation checked by you.

## Steps

1. Refresh the source on your context server after the page ships.
2. Ask the question that page exists to answer. Use the words a developer uses, not the heading you preferred.
3. Read the citation. It should be the page you just published, not an older duplicate and not a blog post that happens to share the title.
4. If it is the wrong page, look at the opening paragraph. Retrieval is working from the words on the page. Ask the writer to put the question's words in the first paragraph, refresh, and ask again.
5. If the server says the answer is not in the sources, believe it. The page is missing the fact, or the source did not refresh. Do not point the harness at a web search to paper over it.
6. Record the question next to the page, so the next publish runs the same check. [Awesome Context Observability](https://github.com/zthewriter/awesome-context-observability) is the wider set of tools for seeing which passages answers used.

## How you know it worked

The citation URL is the page you shipped, on the day you shipped it.

## The tool

A context server is RAG exported as an MCP server. This check is you looking at the RAG result through that MCP server. If your server keeps a retrieval log, it shows how often the server is asked and which passage was behind a specific answer.

<details>
<summary>Doing this in MCP Studio</summary>

MCP Studio by Appa Tools is one option. Disclosure: maintained by the author of this repo.

The dashboard shows how often the server is asked. The passage behind a specific answer is on the Action analytics tier, described in the [analytics guide](https://docs.appatools.com/mcp-studio/guides/action-predictive-analytics).

</details>

## Also read

- [Context for AI](https://github.com/zthewriter/context-for-ai): connecting a page to the answer that used it.
- [Awesome Context Observability](https://github.com/zthewriter/awesome-context-observability): the tools for that visibility.
- [Ship with AI](https://github.com/zthewriter/ship-with-ai): what the developer does with a citation.
