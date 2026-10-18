# A tool that returns the current sample

Readers ask for "the sample" in a dozen wordings. A custom tool is that question, described once, attached to the server.

## You will have

A tool whose result is the current sample and the page it came from.

## Steps

1. Add a custom tool on your context server and describe the outcome in a sentence: "Return the current sample for this task, the commands it runs, and the page they came from."
2. Attach it to the server that has the samples repo and the quickstart. Check whether your server lets you add a tool after deploy. If it does not, add the tool before you deploy.
3. Call the tool with the task name you use in the tutorial. The citation should be the sample you maintain.
4. Call it again with the phrasing a reader actually uses. If that misses, the sample's README does not contain those words. Add them to the README, refresh the source, and call again.
5. In the tutorial, use the tool name your server shows in the client's tool list, which may differ from the name you had in mind.

## How you know it worked

Two phrasings return the same page. A command in an old blog post is not what the tool returns, unless that post is still the source.

## The tool

A context server is RAG exported as an MCP server. The custom tool is a named question on top of that RAG system. The MCP export is why the tutorial can say "call this tool" and have it mean the same thing in every editor that speaks MCP.

<details>
<summary>Doing this in MCP Studio</summary>

MCP Studio by Appa Tools is one option. Disclosure: maintained by the author of this repo.

1. On the **Tools** step, choose **Build my own tool**, leave it selected, and deploy. A custom tool belongs to your account and only searches that server's sources. The dashboard has no tools panel, so add the tool before deploy.
2. MCP Studio names the tool from your description. You do not choose the name. The [custom tools guide](https://docs.appatools.com/mcp-studio/guides/custom-tools) is the setup.

</details>

## Also read

- [Context for AI](https://github.com/zthewriter/context-for-ai): making the sample page match the words readers use.
- [Ship with AI](https://github.com/zthewriter/ship-with-ai): prompts that name a stack, which is the same discipline as naming this tool.
- [Awesome Context Observability](https://github.com/zthewriter/awesome-context-observability): whether the tool is what agents called.
