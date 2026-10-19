# Guardrails and approvals

This page defines what an agent may do alone, what needs a person, and who that
person is.

## Permission levels

The following table lists each level:

| Level | Examples | Approval | Approver |
|---|---|---|---|
| Read | Search the docs, get a page, build and preview | None | None |
| Write | Edit pages on a branch, open a pull request | Review before merge | A docs reviewer |
| Publish | Merge to the default branch, which deploys the site | Branch protection and passing checks | A docs maintainer |
| External | Change the context server's sources, rules, or access | Before each change | [Context server owner] |

## While waiting for approval

The agent leaves the pull request open with the checks it ran and their results,
and does not merge, force-push, or start a second change on the same pages.
