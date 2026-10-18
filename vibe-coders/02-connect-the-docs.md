# Connect the docs as an MCP server

A vibe-coded app goes wrong when the editor follows a tutorial for a different version of the framework. The fix is a server that retrieves your stack's docs and answers over MCP.

## You will have

One MCP endpoint connected in the editor, aimed at the docs for the stack you already chose.

## Steps

1. Copy the docs URL for that stack. One official docs site, not a mix of blog posts.
2. Put the URL on a context server, and connect its endpoint in the editor. For a public framework, a hosted server for public sources may already cover it, such as Context7 for library docs or DeepWiki MCP for public repositories. [Choose a context server](../recipes/choose-a-context-server.md) lists options, including ones you run yourself.
3. If the project also has a README or a spec PDF, add it as a second source on the same server, if your server can ingest it.
4. If your server supports source rules, add one in a sentence: "When I ask how to call this framework, use the docs source, not a general tutorial." If it shows which words fire the rule, check that the words you actually type are there.
5. If the URL is a company site rather than public framework docs, make the server private before you connect it. A private server answers only with an access token. Keep the token out of chats you share. A hosted server for public docs cannot hold a company site, so this case needs a server you control.

## How you know it worked

Ask "how do I read a row from the database in this stack?" The citation should be the docs URL you pasted.

## The tool

A context server is RAG exported as an MCP server. It retrieves passages from the sources you added and serves them at an MCP endpoint. That endpoint is the context piece of the harness. The editor writes the code. The server is what it is allowed to read.

<details>
<summary>Doing this in MCP Studio</summary>

MCP Studio by Appa Tools is one option. Disclosure: maintained by the author of this repo.

1. Open [MCP Studio](https://appatools.com/mcp-studio/studio), paste the URL, and deploy. [Connecting a client](https://docs.appatools.com/mcp-studio/reference/connecting-clients) has the config.
2. The [source guide](https://docs.appatools.com/mcp-studio/guides/adding-sources) covers a URL, a repo, and an upload.
3. A source rule is called a retrieval rule. Read its preview. If the words you type are missing, delete the rule and write them into the sentence. See the [retrieval rules guide](https://docs.appatools.com/mcp-studio/guides/retrieval-rules).
4. See [private servers](https://docs.appatools.com/mcp-studio/guides/private-mcp-servers) to make the server private.

</details>

## Also read

- [Ship with AI](https://github.com/zthewriter/ship-with-ai): what RAG is, in one page, and the starter setup.
- [Context for AI](https://github.com/zthewriter/context-for-ai): how pages become passages.
- [Awesome Context Observability](https://github.com/zthewriter/awesome-context-observability): how to see what an agent retrieved.
