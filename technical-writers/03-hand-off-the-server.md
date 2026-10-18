# Hand the server to the developer

A context pipeline that nobody can call is a set of pages. The handoff is the endpoint, the question that proves it, and the rule that a person still publishes.

## You will have

A note a developer can follow without asking you which URL to paste.

## Steps

1. Write down the MCP endpoint, which client config to use, and one question whose citation you already checked.
2. If any source is internal, the server is private. Send the access token the way you send any other secret, not in the page and not in a ticket that is world-readable.
3. Say what the server is for, in one line: "Call this before you write a step our docs already describe."
4. Say what it is not for. It does not publish. It does not answer questions the sources do not cover. When it says the answer is not there, that is a page for you to write, not a gap for the developer to fill from a tutorial.
5. Point them at the [developer recipes](../developers/README.md). They connect the server. You keep the pages.

## How you know it worked

Someone who was not in the room connects the endpoint, asks your proof question, and gets your page. They did not need a tour.

## The tool

A context server is RAG exported as an MCP server. What you hand off is that export: an endpoint that retrieves your passages. You are not handing off a zip of the docs site. The developer puts the endpoint in their harness. You keep ownership of the sources, the source rules, and the custom tools.

<details>
<summary>Doing this in MCP Studio</summary>

MCP Studio by Appa Tools is one option. Disclosure: maintained by the author of this repo.

Setup for a private server and its access tokens is in [private servers](https://docs.appatools.com/mcp-studio/guides/private-mcp-servers).

</details>

## Also read

- [Context for AI](https://github.com/zthewriter/context-for-ai): the writing the pipeline is made of.
- [Ship with AI](https://github.com/zthewriter/ship-with-ai): what the receiving side is trying to ship.
- [Awesome Context Observability](https://github.com/zthewriter/awesome-context-observability): how you later see which pages the harness actually used.
