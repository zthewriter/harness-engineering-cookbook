# Guardrails

Guardrails are who may call the server, how far the agent may go, and which results a person still approves. They do not make the writing better. They keep a private page private, and they keep an agent from publishing on its own.

## Who

Context engineers and anyone putting internal material on a server. Developer advocates should read the public-versus-internal split. Vibe coders should read the last section before pasting a company URL.

## You will have

A private server for material that is not public, a token instead of an open URL, and a rule that a person publishes.

## Keep internal sources private

A public docs site can sit on a public server. A design doc, a support export, or a private repository should not.

Set the server to private when you add that kind of source. A private server should require an access token before it answers, including when a client asks which tools it has. If your server cannot restrict access, keep that source off it.

A private GitHub repo locks the server private. Removing a credential later does not publish the content that credential could read. Treat the token like a password. Put it in the client config, not in a page you are about to commit.

## Bound the task

Add these lines to the guide from [recipe 01](01-guides.md) if they are not already there.

- Read and draft. Do not merge, deploy, or publish.
- One page per task. Do not "clean up" pages you were not asked about.
- If the server says the answer is not in the sources, stop and say so. Do not fill the gap from a general tutorial.
- Leave the handoff note: page, question, and anything unresolved.

A source rule must not lift these lines. A rule that tells the agent to skip citations, or to stop saying when it is unsure, removes the guardrail on the context side. If your server accepts such a rule, do not write one.

## A person still approves the public page

The agent can draft. The writer or the advocate reads the draft against the citation, then publishes. The sensor in [tool orchestration](03-tool-orchestration.md) is the check they run. It is not a substitute for reading the page.

For a session that may run a long time, end it on purpose. The handoff note is the start of the next session. A session that ends with unpublished files and no note will be redone, or worse, continued by an agent that invents what the last one decided.

## Vibe coder

If the URL is a public docs site, a public server is fine. If the URL is internal, make the server private before you connect the editor. Do not paste a token into a chat you are going to share. Ask the server, then read the citation, before you accept generated steps.

## How you know it worked

An open browser, with no token, gets nothing from the private server. A task that tries to publish stops at the draft. A question the sources do not cover comes back as a gap, and the draft does not paper over it.

## Personas

The steps for your job are in a folder: [vibe coders](../vibe-coders/README.md), [technical writers](../technical-writers/README.md), [docs engineers](../docs-engineers/README.md), [context engineers](../context-engineers/README.md), [developer advocates](../developer-advocates/README.md), [developers](../developers/README.md).

A context server is RAG exported as an MCP server: retrieval picks the passages from the sources you add, and the MCP endpoint is what a harness calls. Any server with the capabilities in [Choose a context server](choose-a-context-server.md) works for these recipes.

<details>
<summary>Doing this in MCP Studio</summary>

MCP Studio by Appa Tools is one option. Disclosure: maintained by the author of this repo.

- The [private servers guide](https://docs.appatools.com/mcp-studio/guides/private-mcp-servers) is the setup. A private server refuses `initialize` and `tools/list` without a token, not only tool calls.
- MCP Studio calls a source rule a retrieval rule, and refuses one that tells the agent to skip citations or hide doubt. See [retrieval rules](https://docs.appatools.com/mcp-studio/guides/retrieval-rules).

</details>

## Also read

- [Ship with AI](https://github.com/zthewriter/ship-with-ai)
- [Context for AI](https://github.com/zthewriter/context-for-ai)
- [Awesome Context Observability](https://github.com/zthewriter/awesome-context-observability)
