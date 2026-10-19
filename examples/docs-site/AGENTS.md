# [Product] docs

The source for the [Product] documentation site at [docs URL]. Pages are Markdown in
`docs/`, built into the site by [site generator].

## Commands

- Install: `[npm ci]`
- Preview the site: `[npm start]`
- Build the site: `[npm run build]`
- Check links: `[npm run links]`
- Lint prose: `[npm run lint:prose]`

## Conventions

- One task per page. The page title names the task, such as "Rotate an API key".
- Every second-level heading names what is under it, because the context server
  splits pages at those headings and a reader's agent sees the heading alone.
- Follow `[style guide path]` for voice and terms.

## Boundaries

- Never edit generated files, such as `[api reference path]`, because the next
  build overwrites them.
- Ask before deleting or renaming a page, because published links and agents'
  saved citations point to it. A moved page leaves a redirect.
- Never put a secret, a customer name, or real account data in a page or example.

## Where to find more

- Definition of done: `harness/definition-of-done.md`
- Which source answers which question: `harness/context-source-map.md`
- Tools an agent may call: `harness/tool-catalog.md`
- What needs approval: `harness/guardrails.md`
