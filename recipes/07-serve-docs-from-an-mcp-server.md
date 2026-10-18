# Serve docs from an MCP server

This recipe delivers your documentation through a Model Context Protocol (MCP)
server, so an agent searches your pages and gets passages with links, instead of
fetching whole pages or guessing.

## Who

Context engineers and docs engineers. Technical writers own the pages the server
reads and the descriptions of its tools.

## You will have

One MCP endpoint that answers questions from your documentation with a link to the
page behind each passage, and a documentation set for the server itself.

## 1. Choose a context server

Pick a server against the capabilities in
[Choose a context server](choose-a-context-server.md). The first five are the
minimum: ingest your sources, keep headings with passages, retrieve by words and by
meaning, cite the page, and expose an MCP endpoint.

## 2. Add your sources and deploy

Add the documentation site first, then the repository that holds working examples.
Deploy, and note the endpoint URL.

## 3. Write the tool descriptions and server instructions

Agents choose tools by reading their names and descriptions, so write them as
carefully as a page title. If the server sends instructions to clients, publish them
and version them like code. Use the
[tools reference](https://github.com/zthewriter/context-for-ai/blob/v1.0.0/templates/mcp-server/04-tools-reference.md)
and
[server instructions](https://github.com/zthewriter/context-for-ai/blob/v1.0.0/templates/mcp-server/07-server-instructions.md)
templates.

## 4. Document the server

Write at least the required pages of the
[MCP server template set](https://github.com/zthewriter/context-for-ai/blob/v1.0.0/templates/mcp-server/README.md):
the overview, connecting a client, authentication and permissions, security and
data, limitations, troubleshooting, and change history.

## How you know it worked

Use the following checks:

- Your MCP client lists the server's tools.
- A question answered on one page returns a passage from that page, with its URL.
- A question your docs do not cover gets "not found", not a guess.

## Also read

- [Context engineering](02-context-engineering.md)
- [Prove the citation](11-prove-the-citation.md)
