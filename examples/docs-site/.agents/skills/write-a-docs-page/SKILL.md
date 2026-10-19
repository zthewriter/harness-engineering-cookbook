---
name: write-a-docs-page
description: Write or revise one task page in the docs repository so readers and the context server can use it. Use when asked to document a task, a feature, or an error.
---

# Write a docs page

## Steps

1. Search the docs through the context server first. If a page already covers the
   task, revise that page instead of writing a second one.
2. Read `[style guide path]`, and copy the structure of one existing task page.
3. Write one task per page. Name each second-level heading for what is under it.
4. Run every check in `harness/definition-of-done.md`.
5. Open a pull request that names the question the page answers.

## Report format

The pull request description states the question the page answers, the checks run
and their results, and any check that could not run.

## Never

- Never invent a command, a flag, or a value. If the sources do not say, ask.
- Never delete or rename a page without approval.
