# Call the servers they already shipped

The docs you need are already an MCP server, built by the people who own the pages. Connecting it is the whole task. Pasting the docs site into the chat is how the harness gets a second, staler copy.

## You will have

The endpoint in your editor, answering their proof question with their page.

## Steps

1. Take the endpoint, the client config, and the proof question from the writer, the docs engineer, or the advocate. The config pattern is in their server's documentation. If they did not send one, the [connect an MCP server skill](https://github.com/zthewriter/ship-with-ai/blob/v1.0.0/skills/connect-mcp-server/SKILL.md) lists where common clients keep it and how to read a token from an environment variable.
2. If they sent a token, the server is private. Put the token in the place that client expects for a secret. Do not commit it and do not paste it into a shared chat.
3. Ask the proof question before you ask for any code. The citation should be the page they named.
4. If it is not, stop and tell them. Do not point the editor at a web search "just for this one." A wrong citation means you are about to implement the wrong product.
5. Ask for the change you actually want, and tell the editor to call that server before it writes a step the docs already describe.

## How you know it worked

The proof question cites their page. A real task cites the same server, not a blog post from somewhere else.

## The tool

The server you just connected is a context server: RAG exported as an MCP server. RAG means the answer is passages retrieved from the sources they added, which are the docs, the repo, and the files they chose. The export is the MCP endpoint in your config. You are not running a second retrieval stack. You are calling theirs. Source rules and custom tools they attached are already on that endpoint. Use the tool they named when they gave you one.

<details>
<summary>Doing this in MCP Studio</summary>

MCP Studio by Appa Tools is one option. Disclosure: maintained by the author of this repo.

The client config pattern is [connecting a client](https://docs.appatools.com/mcp-studio/reference/connecting-clients).

</details>

## Also read

- [Ship with AI](https://github.com/zthewriter/ship-with-ai): building the app once the docs are in reach.
- [Context for AI](https://github.com/zthewriter/context-for-ai): why the page they cited is shaped the way it is.
- [Awesome Context Observability](https://github.com/zthewriter/awesome-context-observability): what they can see about the questions you ask.
