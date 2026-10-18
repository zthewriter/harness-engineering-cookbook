# Keep delivered context current

This recipe keeps every channel that delivers your docs, whether files, an MCP
server, or an API, in step with what you publish, and catches the change that made
answers worse.

## Who

Docs engineers and context engineers. Technical writers own the question set.

## You will have

A refresh that runs when you publish, a context changelog, and a fixed question set
that runs after each change.

## 1. Refresh on publish

Trigger a refresh of every delivery channel from the same step that publishes the
docs, for example the last job in your docs build. A schedule alone leaves a window
in which agents read the old page.

## 2. Keep a context changelog

Record each change to sources, retrieval rules, tool descriptions, or server
instructions, with its date and its measured effect. Use the
[context changelog template](https://github.com/zthewriter/context-for-ai/blob/v1.0.0/templates/harness/context-changelog.md).
When answers change, this page is how someone finds out why.

## 3. Write a regression question set

Write questions whose correct page you know, including at least two your docs do not
answer. Record, for each one, the page a correct answer cites. Use the
[evaluation template](https://github.com/zthewriter/context-for-ai/blob/v1.0.0/templates/mcp-server/11-evaluation.md)
for an MCP server, or the
[evaluation spec](https://github.com/zthewriter/context-for-ai/blob/v1.0.0/ai-engineers/templates/eval-spec.md)
for any agent.

## 4. Run the set after every context change

Run the questions after each changelog entry and record the result in the entry. A
drop is a reason to revert, not a reason to adjust the questions.

## How you know it worked

Use the following checks:

- Edit a page, publish, and ask about the edit. The answer reflects it within the time
  your plan allows.
- Every context change in the last month has a changelog entry with a result.

## Also read

- [Prove the citation](11-prove-the-citation.md)
- [Context engineers: keep one endpoint current](../context-engineers/03-keep-the-endpoint-current.md)
