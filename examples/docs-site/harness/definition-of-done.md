# Definition of done

A change to the docs is done when every check below passes. An agent runs them
before it says the work is finished.

## Checks

The following table lists each check:

| Check | Command or evidence | Required for |
|---|---|---|
| The site builds | `[npm run build]` exits with 0 | Every change |
| Links resolve | `[npm run links]` exits with 0 | Every change |
| Prose lint passes | `[npm run lint:prose]` exits with 0 | Every change to a page |
| The answer cites the page | A question the page answers returns that page from the context server | New pages and renamed headings |
| Rules still fire | Each test question in `harness/retrieval-rules.md` passes | Changes to rules, the style guide, or the API reference |

## When a check fails

Fix the cause and run the check again. Do not skip a check or mark it as passing.
If a check cannot run, say which one and why in the pull request.
