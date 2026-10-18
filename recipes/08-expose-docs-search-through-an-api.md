# Expose docs search through an API

This recipe delivers your documentation through a search endpoint that other systems
call over HTTP: a support tool, a chatbot, or an agent framework that does not speak
MCP.

## Who

Docs engineers and developers who integrate documentation into other products.

## You will have

One HTTP endpoint that takes a question and returns passages, each with the URL of
the page it came from, plus a reference page for the endpoint.

## 1. Choose where search runs

Use the search API of your context server if it has one. Otherwise, index your pages
in a search engine, for example Meilisearch or Typesense, which are both open source.
Index by heading, so each result is one section, not one whole page.

## 2. Define the response

Return passages, not pages, and give each one the fields a caller needs to cite it:

```json
{
  "results": [
    {
      "text": "To roll back, run kestrel rollback --to <release>.",
      "url": "https://docs.kestrel.example/guides/rollback",
      "heading": "Roll back a deployment"
    }
  ]
}
```

## 3. Protect the endpoint

Require a key for anything that is not public documentation, and rate limit every
caller. Write down which pages the endpoint can return.

## 4. Document the endpoint

Write a reference page with the
[API endpoint reference template](https://github.com/zthewriter/context-for-ai/blob/v1.0.0/templates/classic/api-endpoint-reference.md),
and list every error with the
[API errors template](https://github.com/zthewriter/context-for-ai/blob/v1.0.0/templates/classic/api-errors.md).

## How you know it worked

Use the following checks:

- A request with a question answered on one page returns that page's URL in the
  first results.
- A request without a key, where a key is required, is refused.
- Each error in the reference page is one you can reproduce.

## Also read

- [Serve docs from an MCP server](07-serve-docs-from-an-mcp-server.md)
- [Observe delivered context](12-observe-delivered-context.md)
