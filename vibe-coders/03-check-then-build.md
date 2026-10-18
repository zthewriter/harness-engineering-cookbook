# Check the citation, then build

The sensor in a vibe-coding harness is one question you already know the answer to. You ask it before the editor builds the feature.

## You will have

A stop rule. Wrong citation means you fix the connection. You do not "let it try."

## Steps

1. Ask a question you can check by eye, about the stack you chose.
2. If the citation is the docs server from [the previous recipe](02-connect-the-docs.md), build the feature. Follow a prompt from [Ship with AI](https://github.com/zthewriter/ship-with-ai/blob/v1.0.0/prompts/README.md) so the chat keeps the same stack.
3. If the citation is a general tutorial, stop. Confirm the editor is calling your MCP server. Ask again.
4. When the feature is in the browser, ask the server how that framework expects the call to look. Compare the code the editor wrote with the cited page. Change the code to match the page.
5. One feature per chat. The handoff into the next chat is the guide plus the server, not a paste of the last conversation.

## How you know it worked

The API call in the app matches the cited page. A second chat, started fresh, still names the same stack and the same server.

## The tool

A context server is RAG exported as an MCP server. The check above is you looking at what it retrieved. The passages come from your sources. The MCP server is how the editor asks for them. A custom tool is optional here, and only if your server supports one. Add one only when you keep asking the same question, such as "show the current auth snippet and the page it came from."

<details>
<summary>Doing this in MCP Studio</summary>

MCP Studio by Appa Tools is one option. Disclosure: maintained by the author of this repo.

Describe a custom tool in a sentence on the wizard's **Tools** step. See [custom tools](https://docs.appatools.com/mcp-studio/guides/custom-tools).

</details>

## Also read

- [Ship with AI](https://github.com/zthewriter/ship-with-ai): the prompts and the rescue guides.
- [Context for AI](https://github.com/zthewriter/context-for-ai): why a passage has to stand on its own.
- [Awesome Context Observability](https://github.com/zthewriter/awesome-context-observability): seeing which passage reached the answer.
