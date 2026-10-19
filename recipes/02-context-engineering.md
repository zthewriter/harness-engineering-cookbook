# Context engineering

Context engineering is the curation of what the model sees: the passages retrieved for this question, the memory that should survive the session, and the constraint that says which source this task may use.

The agent asks for that context over MCP, from a context server: retrieval over the sources you trust, exported as an MCP endpoint. [Choose a context server](choose-a-context-server.md) lists the capabilities these recipes need. You add sources. A source rule tells the server when a source matters. A custom tool is one question your team asks over and over.

Guides stay short. This recipe is where the pages go.

## Who

Context engineers first. Docs engineers, technical writers, developer advocates, and vibe coders all have a path below. The short path is [at the end](#vibe-coder-paste-the-url).

## You will have

One MCP server whose answers cite your pages. A source rule for the source the question will not name. A custom tool for one recurring docs question.

## 1. Put the sources on a server

A source is the material you already trust.

| Source | Use it for |
| --- | --- |
| Documentation site | The published guide and the reference |
| GitHub repository | The implementation and the working examples |
| A website on one hostname | A changelog or a set of posts |
| An uploaded file | A spec, a deck, a spreadsheet, or a PDF |
| Another MCP server | A docs set that already answers over MCP |

On your context server, add the source, choose the tools, and deploy. A private repository belongs on a server that can restrict access, as [Guardrails](04-guardrails.md) explains.

If you would rather not write code for this, consider a no-code tool such as MCP Studio by Appa Tools, where you add the sources, describe a custom tool in a sentence, and write each source rule in plain language. Disclosure: maintained by the author of this repo. Its steps are under **Doing this in MCP Studio** at the end of this recipe, and other options are in [Choose a context server](choose-a-context-server.md).

Group sources that answer the same kind of question. A useful split for a docs org is Product, Decisions, and Examples. A developer advocate often wants the current quickstart and the sample repo on the Examples server, and the style guide on Product.

An MCP server you add as a source is read from. It does not become a set of buttons that change the other product.

## 2. Decide what is memory and what is retrieved

| Belongs in the guide from [recipe 01](01-guides.md) | Belongs on the server |
| --- | --- |
| Voice, terms, and "one page per task" | The pages those rules apply to |
| The URL of this server | The passages inside it |
| What done means | The example that shows done |

The guide is loaded because it is short. The server is asked because the docs are not. Pasting the docs into the guide makes every later task carry pages it does not need.

When a page changes, refresh that source. The next request sees the new page in every client pointed at the server.

## 3. Add a source rule

Search returns passages that resemble the question. That fails when the right source shares no words with the question. A style guide does not contain the words "release note," and a release note still has to follow it. A source rule tells the server to prefer or include a source for a kind of request. If your server has no such rule, give that source its own server and name the server in the guide.

Write the rule as one or two sentences, the way you would say it to a colleague. Name the kind of request, and say what to do with the source.

```text
This is our style guide. When the task is a public page, a release note,
or a sample, use this source and follow its voice and terminology.
```

If your server shows which words fire the rule, read that list. If a kind of request you care about is missing, write the rule again with those words in the sentence.

A rule should change only which passages come back. It must not change what the page says, answer a question the sources do not cover, change who is allowed to call the server, or tell the agent to hide doubt.

## 4. Add a custom tool for one recurring question

Your server's built-in tools search and answer. A custom tool is for the question those do not quite match, described in your own words. If your server supports custom tools, describe the question and what should come back.

```text
Find the shortest example in our docs that shows this task, and include
the page it came from.
```

```text
List what changed between two versions and the steps a reader has to take
because of it.
```

Be specific about the subject. You do not have to describe how the search works.

A developer advocate's version of this tool is "return the current quickstart for this feature, and the sample repo path that matches it." A docs engineer's version is "given an error string, return the troubleshooting page that mentions it."

## 5. Check the citation

Ask a question you already know the answer to. The reply should name your page. Ask a second question that should hit the source rule, one that does not contain the source's name. The style guide, or whichever source you named, should be in the answer.

If the citation is a different page, the source is the wrong one for that question, or the rule is missing the words you actually ask with. Fix the rule or the page, refresh the source, and ask again.

## Vibe coder: paste the URL

1. Pick a context server. For a public framework, a hosted server for public docs may already cover it. See [Choose a context server](choose-a-context-server.md).
2. Add the docs URL, or the repo, that the project is supposed to follow.
3. Deploy, and connect the endpoint in the editor.
4. Add one line to the editor rules: ask this server before inventing a step.
5. Ask a question you can check by eye. The citation should be that docs site.

You can add the style guide as a second source and a source rule later. The first win is that the editor stops guessing from a tutorial that is not your product.

## What this recipe does not do

The server returns what you placed on it. A decision that was only said in a meeting is invisible until someone writes it down. Questions with no good match in your server's retrieval log are pages you have not written, or pages written so the question cannot find them. [Awesome Context Observability](https://github.com/zthewriter/awesome-context-observability) lists tools that show which passage was behind an answer.

## Personas

The steps for your job are in a folder: [vibe coders](../vibe-coders/README.md), [technical writers](../technical-writers/README.md), [docs engineers](../docs-engineers/README.md), [context engineers](../context-engineers/README.md), [developer advocates](../developer-advocates/README.md), [developers](../developers/README.md).

A context server is RAG exported as an MCP server: retrieval picks the passages from the sources you add, and the MCP endpoint is what a harness calls. Any server with the capabilities in [Choose a context server](choose-a-context-server.md) works for these recipes.

<details>
<summary>Doing this in MCP Studio</summary>

MCP Studio by Appa Tools is one option. Disclosure: maintained by the author of this repo.

1. In [MCP Studio](https://appatools.com/mcp-studio/studio), add the source, choose the tools, and deploy. The [source guide](https://docs.appatools.com/mcp-studio/guides/adding-sources) covers each type, including a private repository.
2. A source rule is called a retrieval rule. In the wizard, each source has **Add a retrieval rule**. On a server that already exists, open it, find **Retrieval rules**, and select **Add a rule**. The preview lists the words that fire the rule. To change a rule, delete it and write it again.
3. A rule can prefer a source, require that one of its passages come back, and pass a short instruction. A rule that tells the agent to hide doubt is refused. See the [retrieval rules guide](https://docs.appatools.com/mcp-studio/guides/retrieval-rules).
4. For a custom tool, choose **Build my own tool** in the wizard's **Tools** step. The tool is saved to your account and selected on the server you deploy. See the [custom tools guide](https://docs.appatools.com/mcp-studio/guides/custom-tools).
5. The [analytics guide](https://docs.appatools.com/mcp-studio/guides/action-predictive-analytics) shows how often a server is asked. The passage behind each answer is on the Action analytics tier.

</details>

## Also read

- [Ship with AI](https://github.com/zthewriter/ship-with-ai)
- [Context for AI](https://github.com/zthewriter/context-for-ai)
- [Awesome Context Observability](https://github.com/zthewriter/awesome-context-observability)
