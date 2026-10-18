# Set the guide before you build

The guide is the part of the harness the editor reads before it writes. For a vibe-coded app it is three lines, not a style manual.

## You will have

An editor rule that names the product, the docs that are allowed, and the order of work: ask the server, then write.

## Steps

1. Pick the stack in [Ship with AI](https://github.com/zthewriter/ship-with-ai) and copy the prompt that names the framework and why. One stack per app. A later chat does not get to switch it.
2. Add three lines to the editor rules:

   ```text
   Stack: the one named in the prompt. Do not swap frameworks.
   Docs: ask the MCP server before you invent a step, a package, or an endpoint.
   Done: the feature works in the browser, and the citation for any API call is a page on that server.
   ```

3. Scope is one feature. "Add login" is a task. "Also redesign the nav and add billing" is three tasks. Finish one, then start the next.

## How you know it worked

Start a fresh chat and ask what stack the app uses. The answer should be the one you named, with no alternative offered "in case you want React instead."

## The tool

A context server is RAG exported as an MCP server. The next recipe puts the docs on one. RAG retrieves the passages for the question you asked. The MCP server is what the editor calls. You do not paste the docs into the chat.

## Also read

- [Ship with AI](https://github.com/zthewriter/ship-with-ai): choose the stack and ship the app.
- [Context for AI](https://github.com/zthewriter/context-for-ai): how a page becomes the passage an agent can use.
- [Awesome Context Observability](https://github.com/zthewriter/awesome-context-observability): tools that show which passage an answer used.
