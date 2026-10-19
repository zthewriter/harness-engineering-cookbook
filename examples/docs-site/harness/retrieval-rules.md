# Retrieval rules

This page records each rule that changes which passages come back, and the question
that proves it works. A rule changes ranking only. It never changes what a page
says, and it never tells an agent to hide doubt.

## Rules at a glance

The following table lists every rule:

| Rule | Trigger | Effect | Test question |
|---|---|---|---|
| Errors prefer the API reference | An error code, such as `[E1042]` | Prefer the API reference | "What does [E1042] mean?" |
| Writing tasks include the style guide | A request to write or edit a page | Always include one style guide passage | "Write a page about [task]" |

## Errors prefer the API reference

- **Trigger:** a question containing an error code.
- **Effect:** prefer passages from the API reference.
- **Reason:** blog posts and forum answers quoting the code rank above the page
  that defines it.
- **Test question:** "What does [E1042] mean?" Passes when the API reference errors
  page is cited.

## Writing tasks include the style guide

- **Trigger:** a request to write, edit, or review a page.
- **Effect:** always include one passage from `[style guide path]`.
- **Reason:** the style guide shares no words with the request, so search alone
  never returns it.
- **Test question:** "Write a page about [task]." Passes when a style guide passage
  is among the results.
