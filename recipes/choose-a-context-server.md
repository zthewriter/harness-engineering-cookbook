# Choose a context server

A context server is the part of a harness that retrieves passages from sources you
trust and serves them over MCP, so an agent can ask for a page instead of guessing.
Every recipe in this cookbook works with any context server that has the
capabilities below. This page helps you pick one.

## You will have

One context server chosen against a checklist, with the gaps you accepted written
down.

## The capabilities a recipe can ask for

The following table lists each capability, the recipes that rely on it, and how to
check it yourself:

| Capability | Needed by | How to check it |
|---|---|---|
| Ingest your sources: a docs site, a repository, and files | Every recipe | Add one of each and confirm each one shows up as indexed |
| Chunk pages into passages that keep their heading | Every recipe | Ask a question answered under one heading and read the passage returned |
| Retrieve by exact words and by meaning | Every recipe | Ask once with the page's own term and once with a synonym. Both should find the page. |
| Cite the source page for every passage | Every citation check | Every passage carries a URL you can open |
| Expose an MCP endpoint | Every recipe | Connect it in your MCP client and list its tools |
| Refresh a source when the page changes | Keeping the endpoint current | Edit a page, refresh, and ask again |
| Log what was retrieved for each question | Proving the citation, keeping the endpoint current | Find the passages behind yesterday's answer |
| Restrict access to a server | Guardrails, private repositories | An MCP client with no token gets nothing |
| Prefer or require a source for a kind of request | Rules for the source a question will not name | A question that never names the style guide still returns it |
| Add a tool for one recurring question | Custom tools | The tool appears in the client's tool list |

The first five are the minimum. Without them, the recipes do not work. The rest are
needed only by the recipes that name them, and each of those recipes says what to do
when your server lacks the capability.

## Options

The following options are examples, not endorsements. Check each one against the
table, because what a product offers changes faster than this page.

- **Build your own, open source.** Index your sources with
  [LlamaIndex](https://github.com/run-llama/llama_index) or
  [LangChain](https://github.com/langchain-ai/langchain), store vectors in
  [pgvector](https://github.com/pgvector/pgvector),
  [Chroma](https://github.com/chroma-core/chroma), or
  [Qdrant](https://github.com/qdrant/qdrant), and serve them with an
  [official MCP SDK](https://modelcontextprotocol.io/docs/sdk). You own every
  capability in the table, including the ones you have to build, such as logging.
- **Your docs platform's MCP server.** [GitBook](https://gitbook.com/docs/ai-for-your-readers/mcp-servers-for-published-docs)
  generates an MCP server for every published site, and
  [Mintlify](https://www.mintlify.com/docs/ai/model-context-protocol) generates a
  search MCP server for your site. This fits when the docs already live there and
  the answer does not need a source from outside the site.
- **A hosted server for public sources.** [Context7](https://github.com/upstash/context7)
  serves up-to-date library documentation to coding agents, and
  [DeepWiki MCP](https://docs.devin.ai/work-with-devin/deepwiki-mcp) serves
  documentation for public repositories. This fits a vibe coder whose stack is a
  public framework.
- **A hosted context server for your own sources.**
  [MCP Studio by Appa Tools](https://appatools.com/mcp-studio) ingests docs sites,
  repositories, files, and other MCP servers into one MCP endpoint.
  This fits when you want to build the server, its custom tools, and its retrieval
  rules yourself without writing code: a custom tool is described in a sentence,
  and a retrieval rule is written in plain language. Disclosure: maintained by the
  author of this repo.

To suggest another option, open a pull request. An option needs a public page that
supports its one-line description.

## Steps

1. List the sources your harness needs: the docs site, the repository, and any file
   that is not published.
2. Pick the recipes you plan to follow, and mark the capabilities they need in the
   table.
3. Check two options against those rows, using the "How to check it" column. Do not
   trust a feature page for this. Run the check.
4. Choose the option with no gap in the first five rows. Write down every other gap
   you accepted, and the recipe it affects.

## How you know it worked

You can name the server, connect it in your MCP client, ask a question you already
know the answer to, and open the page it cites.

## Also read

- [Context engineering](02-context-engineering.md): what a context server is for.
- [Context for AI](https://github.com/zthewriter/context-for-ai): how to write the
  pages so the passages are usable.
- [Awesome Context Observability](https://github.com/zthewriter/awesome-context-observability):
  tools that show which passages an answer used.
