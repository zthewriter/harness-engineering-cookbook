# Put the quickstart on a server

A quickstart pasted into a blog post is frozen on the day you wrote it. A quickstart on an MCP server is the page you can still update, retrieved when the reader asks.

## You will have

An endpoint you can put in the tutorial, aimed at the quickstart, the samples repo, and the docs.

## Steps

1. Treat the quickstart as one task. The title is the task. The steps are an ordered list. Each step is something you have done yourself this week.
2. Add that page, the samples repository, and the docs site as sources on your context server.
3. If your server supports source rules, add one: "When the task is getting started or running the sample, use the quickstart source." Check that the words readers type fire it, including "hello world" if that is what they type.
4. Deploy. Ask "how do I get started?" The citation should be your quickstart.
5. In the tutorial, tell the reader to connect the endpoint and ask that question, then follow the cited page. Link your server's client setup page, so you do not maintain a second copy of it.
6. If the sample needs an internal API, that server is private and the tutorial does not include the token. Public samples stay on a public server.

## How you know it worked

A reader who connects the endpoint and asks your question gets your quickstart, not a third-party tutorial that shares the product name.

## The tool

A context server is RAG exported as an MCP server. You are publishing the quickstart twice: once as a page a person reads, and once as retrieval a harness calls. The MCP server is the second copy, and it is the one that stays tied to the page when you edit it.

<details>
<summary>Doing this in MCP Studio</summary>

MCP Studio by Appa Tools is one option. Disclosure: maintained by the author of this repo.

1. Add the sources in [MCP Studio](https://appatools.com/mcp-studio/studio). The [source guide](https://docs.appatools.com/mcp-studio/guides/adding-sources) covers a URL and a repo.
2. A source rule is called a retrieval rule. Its preview lists the words that fire it. See the [retrieval rules guide](https://docs.appatools.com/mcp-studio/guides/retrieval-rules).
3. [Connecting a client](https://docs.appatools.com/mcp-studio/reference/connecting-clients) is the config to link.

</details>

## Also read

- [Context for AI](https://github.com/zthewriter/context-for-ai): writing the quickstart so a passage still makes sense alone.
- [Ship with AI](https://github.com/zthewriter/ship-with-ai): the kind of prompt your reader will paste next to your server.
- [Awesome Context Observability](https://github.com/zthewriter/awesome-context-observability): seeing whether agents used the quickstart or something else.
