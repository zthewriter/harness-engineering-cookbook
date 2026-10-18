# Publish only the steps you followed

The guardrail on an advocacy harness is that you ran the steps. The agent can draft. You publish after the citation matches what you did.

## You will have

A sample whose commands match the page the server cites today.

## Steps

1. Connect the server from [the first recipe](01-quickstart-on-a-server.md) in your own editor.
2. Ask for the sample through the tool from [the second recipe](02-tool-for-the-sample.md). Follow those steps yourself. When a step fails, fix the page, refresh the source, and follow it again.
3. Only then let the agent draft the surrounding post. The guide says it may not invent a command and it may not publish.
4. Before you publish, ask the server the same question a reader will ask. If the citation is an old page, you are about to ship a tutorial that disagrees with the server you told them to trust. Fix the source first.
5. Hand the endpoint to developers with the [developer recipes](../developers/README.md). Your job was the pipeline. Their job is to call it while they build.

## How you know it worked

You can run the sample from the cited page, on the day the post goes out, without changing a command.

## The tool

A context server is RAG exported as an MCP server. The check is the RAG result: the passages it retrieved for the question you asked, served from the MCP server you told readers to connect. If those passages and your post disagree, the post is the one that changes.

## Also read

- [Context for AI](https://github.com/zthewriter/context-for-ai): the writing practices behind a page an agent can follow.
- [Ship with AI](https://github.com/zthewriter/ship-with-ai): shipping the app the sample is about.
- [Awesome Context Observability](https://github.com/zthewriter/awesome-context-observability): confirming readers' agents cited you.
