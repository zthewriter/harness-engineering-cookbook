# When you need a server they have not built

Some repos are yours. The docs pipeline does not cover them, and it should not have to. You put that repo on a server, connect it the same way, and you do not recreate their docs server beside it.

## You will have

One MCP server for your repository, public or private to match the repo, connected next to the servers you already use.

## Steps

1. Confirm the writers and the context engineer do not already have a server for this. Two servers on the same docs will disagree.
2. On a context server, add your repository as a source. Add the design note or the spec if it is a file rather than a page. [Choose a context server](../recipes/choose-a-context-server.md) lists options, including ones you run yourself.
3. If the repository is private, the server must be private. Connect it with an access token, and never put a private source on a public server.
4. Add a source rule only if one document must show up when the question will not name it, and your server supports one: "When the task touches the public API of this repo, use the design note." Check which words fire it.
5. Add a custom tool, if your server supports one, only for a question you ask every time you open the repo, described in a sentence.
6. Put one line in the guide: "This repo's own code and design note: call my server. Company procedures: call theirs."
7. Ask a question you can answer by opening a file. The citation should be that file.

## How you know it worked

A question about your repo cites your server. A question about the product docs still cites their server. The two did not collapse into one search.

## The tool

A context server is RAG exported as an MCP server. Here you are the one exporting: RAG over your repository, served as an MCP endpoint your harness calls. It can be the same kind of server the writers used for the docs, or a different one. Yours is scoped to the repo they do not own. Theirs stays the source for everything they published.

<details>
<summary>Doing this in MCP Studio</summary>

MCP Studio by Appa Tools is one option. Disclosure: maintained by the author of this repo.

1. Add the repository in [MCP Studio](https://appatools.com/mcp-studio/studio). The [source guide](https://docs.appatools.com/mcp-studio/guides/adding-sources) covers a repo and an upload.
2. A private GitHub source locks the server private. See [private servers](https://docs.appatools.com/mcp-studio/guides/private-mcp-servers).
3. A source rule is called a retrieval rule. See the [retrieval rules guide](https://docs.appatools.com/mcp-studio/guides/retrieval-rules) and [custom tools](https://docs.appatools.com/mcp-studio/guides/custom-tools).

</details>

## Also read

- [Ship with AI](https://github.com/zthewriter/ship-with-ai): shipping the app this repo is part of.
- [Context for AI](https://github.com/zthewriter/context-for-ai): how to write the design note so retrieval can use it.
- [Awesome Context Observability](https://github.com/zthewriter/awesome-context-observability): seeing what your own server returned.
