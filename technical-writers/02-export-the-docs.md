# Export the docs as an MCP server

The context pipeline is the docs, retrieved on demand, exported as an MCP server a harness can call.

## You will have

A server that cites your page, including for a question that never says the name of the style guide.

## Steps

1. On your context server, add the docs site as a source. Add the style guide if it lives somewhere else, and the repo if examples live there. [Choose a context server](../recipes/choose-a-context-server.md) lists what the server needs.
2. If your server supports source rules, add one on the style guide: "When the task is a public page, a release note, or a sample, use this source and follow its voice and terminology." If it shows which words fire the rule, the words you care about have to be in that list. A rule must not change what the page says or tell the agent to hide doubt.
3. Add a custom tool if the team keeps asking one question the built-in search does not match, and your server supports one. Describe it in a sentence: "Find the procedure for this task and the page it came from."
4. Deploy, and connect the endpoint in an MCP client. The [connect an MCP server skill](https://github.com/zthewriter/ship-with-ai/blob/v1.0.0/skills/connect-mcp-server/SKILL.md) lists where common clients keep the config. Ask a question you know the answer to. The citation should be your page.
5. Check what the rule promises. If it says a passage from the style guide is always included, ask a question that should follow the style guide and does not contain the words "style guide." That passage should be in the answer. A rule that only prefers a source raises its rank. It does not guarantee the passage.
6. When a page changes, refresh that source. The next request sees the new page.

## How you know it worked

Both questions cite your material. A wrong citation means the opening of the page does not share words with the question, or the rule is missing those words. Fix that, refresh, and ask again.

## The tool

A context server is RAG exported as an MCP server. RAG is the retrieval of passages from the sources you added. The export is the MCP endpoint. Sources, source rules, and custom tools are how you shape what that endpoint returns. The harness does not contain a copy of the docs. It calls this server.

<details>
<summary>Doing this in MCP Studio</summary>

MCP Studio by Appa Tools is one option. Disclosure: maintained by the author of this repo.

1. In [MCP Studio](https://appatools.com/mcp-studio/studio), add the sources. The [source guide](https://docs.appatools.com/mcp-studio/guides/adding-sources) covers each type.
2. A source rule is called a retrieval rule. Its preview lists the words that fire it and says whether a passage is always included. A rule that tells the agent to hide doubt is refused. See the [retrieval rules guide](https://docs.appatools.com/mcp-studio/guides/retrieval-rules).
3. See [custom tools](https://docs.appatools.com/mcp-studio/guides/custom-tools).

</details>

## Also read

- [Context for AI](https://github.com/zthewriter/context-for-ai): writing the page so the passage is usable.
- [Awesome Context Observability](https://github.com/zthewriter/awesome-context-observability): passage analytics tools, hosted and open source.
- [Ship with AI](https://github.com/zthewriter/ship-with-ai): the RAG explanation a non-writer can follow.
