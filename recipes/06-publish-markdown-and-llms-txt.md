# Publish Markdown and llms.txt

This recipe delivers your documentation as static files any agent can fetch: a
Markdown version of each page, and an `llms.txt` file at the site root that lists
the pages worth reading. Nothing needs to run on your side once the files are
published.

## Who

Technical writers and docs engineers who own a documentation site.

## You will have

A Markdown version of each page you choose, and an `llms.txt` file that lists those
pages with a note on what each one answers.

## 1. Write the listing policy

Decide which pages the file lists before you write it, or the file grows into a
second sitemap. Write the rule down with the
[llms.txt template](https://github.com/zthewriter/context-for-ai/blob/v1.0.0/templates/harness/llms-txt.md).
Most sites list task and reference pages and leave out marketing and archived pages.

## 2. Publish a Markdown version of each listed page

Serve each listed page as Markdown at a predictable address, for example the page's
URL with `.md` added. Many docs frameworks can do this through a plugin or a build
step. Check your framework's documentation, and confirm the Markdown keeps headings
and code blocks.

## 3. Write llms.txt

Follow the format at [llmstxt.org](https://llmstxt.org): an H1 with the site name, a
blockquote summary, then H2 sections of links with a short note each. Put links an
agent can skip under an H2 named "Optional".

```markdown
# Kestrel docs

> Guides and API reference for deploying apps on Kestrel.

## Guides

- [Deploy an app](https://docs.kestrel.example/guides/deploy.md): First deploy, step by step
```

## 4. Serve it at the site root

Publish the file at `/llms.txt`. Regenerate it in the same build that publishes the
pages, so a removed page leaves the file in the same release.

## How you know it worked

Use the following checks:

- `https://<your site>/llms.txt` returns the file as plain text.
- Every link in the file returns Markdown, not an HTML page or a 404.
- An agent given only the site URL can find and quote a listed page.

## Also read

- [Keep delivered context current](10-keep-delivered-context-current.md)
- [Context delivery plan template](https://github.com/zthewriter/context-for-ai/blob/v1.0.0/templates/harness/context-delivery-plan.md)
