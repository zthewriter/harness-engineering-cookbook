# Rules and custom tools

Two controls shape a RAG server after the sources are in. A source rule fires on the words of the task. A custom tool is a question you got tired of rephrasing.

## You will have

One rule that pulls in a source the question will not name, and one custom tool for a question the team asks every week.

## Steps

1. Write the rule as the sentence a teammate would say. "When the task mentions a public page or a sample, use the style guide." Put it on the style guide source.
2. If your server shows which words fire the rule, read that list. If "release note" matters and it is not in the list, rewrite the rule so it names those words.
3. Do not write a rule that tells the server to stop reporting a weak match. A rule also must not change what a page says, answer a question the sources do not cover, or change who can call the server.
4. For the weekly question, add a custom tool, if your server supports one, and describe the outcome, not the search strategy. "Return the breaking changes between these two versions, each with its page." Check whether a tool can be added to a server that already exists, or only when you deploy it.
5. Ask the weekly question through the new tool and through ordinary search. Keep the tool only if the citation is the page you wanted and ordinary search was not.

## How you know it worked

A task that never says "style guide" still receives it. The weekly question returns the page you named, through the tool you named.

## The tool

A context server is RAG exported as an MCP server. Source rules and custom tools are controls on that RAG system. They do not replace the sources, and they do not change the sentences on the page. The MCP export means a developer turns the tool on in the client and calls it by name.

<details>
<summary>Doing this in MCP Studio</summary>

MCP Studio by Appa Tools is one option. Disclosure: maintained by the author of this repo.

1. A source rule is called a retrieval rule. Its preview lists the words that fire it and is generated from the rule the server applies. There is no edit in place: delete the rule and write a new one.
2. A rule that tells the server to stop reporting a weak match is refused. The [retrieval rules guide](https://docs.appatools.com/mcp-studio/guides/retrieval-rules) states the limit.
3. On the **Tools** step, choose **Build my own tool**, and select it before you deploy. A custom tool belongs to your account and only searches the sources on the server. The dashboard has no tools panel, so a server that already exists keeps the tools it was deployed with unless you change them through the API. The [custom tools guide](https://docs.appatools.com/mcp-studio/guides/custom-tools) is the setup.

</details>

## Also read

- [Context for AI](https://github.com/zthewriter/context-for-ai): what the passages need to contain for either control to have something to return.
- [Awesome Context Observability](https://github.com/zthewriter/awesome-context-observability): checking that the rule fired on real questions.
- [Ship with AI](https://github.com/zthewriter/ship-with-ai): the builder-facing version of "give the assistant your content."
