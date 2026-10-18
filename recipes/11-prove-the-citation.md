# Prove the citation

This recipe checks that delivered context is the context an agent actually used:
you ask questions whose answer you know, confirm the page each answer cites, and
record the result.

## Who

Technical writers and docs engineers. It needs no access beyond an agent connected
to your docs.

## You will have

A short record of known questions, the page each answer cited, and whether that was
the right page.

## 1. Pick ten known questions

Choose questions you can answer yourself, each answered on exactly one page. Include
two that your docs do not answer.

## 2. Ask each question in a clean session

Ask in a new session, so earlier answers do not leak into the next one. Use the
channel your readers use: the MCP server, the API, or an agent given your
`llms.txt`.

## 3. Open every cited page

Open each cited URL and confirm the passage is on that page and supports the answer.
A citation that points at the right site but the wrong page is a failure.

## 4. Record the result

Record each question in a table like the following one:

| Question | Expected page | Cited page | Right page | Date |
|---|---|---|---|---|
| How do I roll back a deploy? | /guides/rollback | /guides/rollback | Yes | 2026-10-01 |
| What does Kestrel charge for GPUs? | None | /pricing | No: should say not found | 2026-10-01 |

For an ongoing record across many questions, use the
[content usage log](https://github.com/zthewriter/context-for-ai/blob/v1.0.0/templates/content-usage-log.csv).

## How you know it worked

You have a dated record for every question. Each failure names the page that should
have been cited, or says the answer should have been "not found".

## Also read

- [Keep delivered context current](10-keep-delivered-context-current.md)
- [Observe delivered context](12-observe-delivered-context.md)
