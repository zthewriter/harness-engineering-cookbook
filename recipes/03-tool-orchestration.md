# Tool orchestration and sensors

Tools are the actions the agent may take. Sensors are the checks that come back, so "done" is a result you can look at rather than a sentence the agent typed.

For docs work the actions are small. Search the sources. Ask a question. Fetch the page. Run the style check. Report the link. The context those tools read is the server from [context engineering](02-context-engineering.md).

## Who

Docs engineers and developer advocates. Technical writers use the sensor. Vibe coders use the last section.

## You will have

A server that exposes a few tools on purpose, a custom tool for the question your readers actually ask, and one check you run before you accept the edit.

## Choose the tools

A server needs a search and a way to ask. Add a custom tool only for a question the built-ins keep missing, and only if your server supports one. Your server's documentation says what each built-in tool is for.

| Tool | Docs job |
| --- | --- |
| Search | Find the page that might answer |
| Ask | Answer from those pages, with a citation |
| Examples | Pull a snippet that already exists |
| Your custom tool | The question your team keeps rephrasing |

Leave off tools the task does not need. An agent that can call ten tools will call one you did not mean, and the citation gets harder to read.

Connect the endpoint where the work happens: the editor, Claude, or the workflow tool your advocates already use. Your server's documentation has the client config for each one.

## Add a sensor

Pick one check that matches the role.

**Docs engineer.** After the agent edits a page, ask the server the question that page is supposed to answer. The citation should be the page you just edited. If it cites an older page, the new one is not the passage the question finds. Change the heading or the first paragraph so the question and the page share words, refresh the source, and ask again.

**Developer advocate.** Ask for the quickstart with the custom tool from the context recipe. Open the page it names and follow the steps yourself. The sample should match the page. A sample that drifted is a source to refresh, or a page to update, before the agent writes another one.

**Technical writer.** Run the style check you already trust, then read the note the [guide](01-guides.md) told the agent to leave. The note should name the page and the question. A note that names three pages means the scope rule was ignored. Send it back to one page.

## Vibe coder

Connect the server. Ask one question you know the answer to before you ask it to build. If the citation is your docs, continue. If the citation is a general tutorial, stop and check that the editor is actually calling your server. Building on a wrong citation is how a project grows a feature your product does not have.

## How you know it worked

The same question, asked twice with the source unchanged, cites the same page. The check fails in a way you can see: wrong page, broken link, or a style error with a line. A check that always passes is not a sensor.

## Personas

The steps for your job are in a folder: [vibe coders](../vibe-coders/README.md), [technical writers](../technical-writers/README.md), [docs engineers](../docs-engineers/README.md), [context engineers](../context-engineers/README.md), [developer advocates](../developer-advocates/README.md), [developers](../developers/README.md).

A context server is RAG exported as an MCP server: retrieval picks the passages from the sources you add, and the MCP endpoint is what a harness calls. Any server with the capabilities in [Choose a context server](choose-a-context-server.md) works for these recipes.

<details>
<summary>Doing this in MCP Studio</summary>

MCP Studio by Appa Tools is one option. Disclosure: maintained by the author of this repo.

- The [tool guide](https://docs.appatools.com/mcp-studio/guides/choosing-tools) says what each built-in tool is for.
- [Connecting a client](https://docs.appatools.com/mcp-studio/reference/connecting-clients) has the config for each client.

</details>

## Also read

- [Ship with AI](https://github.com/zthewriter/ship-with-ai)
- [Context for AI](https://github.com/zthewriter/context-for-ai)
- [Awesome Context Observability](https://github.com/zthewriter/awesome-context-observability)
