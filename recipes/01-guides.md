# Guides

The agent reads a guide before it acts. In a docs repo that guide is short on purpose: voice, the words you use, which page to open first, and the rule that one change touches one page.

This is the feedforward control in the harness. It does not contain your whole documentation set. That set is a source, and it belongs in [context engineering](02-context-engineering.md).

## Who

Technical writers, developer advocates, and anyone about to point an agent at a docs change. Vibe coders can use the short version at the end.

## You will have

A file named `AGENTS.md` at the root of the docs repo. An agent that opens the repo reads it before editing a page.

## Write the guide

1. State the voice in a few lines a person can check. American English if that is your standard. One term for each thing, and the term you do not use.
2. Point at the pages, do not paste them. Name the style guide, the glossary, and the template for a new page as paths or URLs.
3. Say the scope. One page, or one feature, per task. The agent does not rewrite the navigation, the changelog, and the landing page in the same pass.
4. Say what done means. The page answers one question. A procedure has an ordered list. A claim that can go stale names the version it describes.
5. Say what the agent must not do. It does not invent a command. It does not publish. It leaves a note saying which page it changed and which question that page now answers.

```markdown
# Docs agent guide

Voice: American English. Call the product by its full name on first mention.
Terms live in GLOSSARY.md. Do not introduce a synonym.

Before editing, read STYLE.md and the template in templates/concept.md.
Change one page. Do not edit navigation or the changelog in the same task.

Done: the page answers one question, the steps are ordered, and any version
claim names the version. Do not invent commands. Do not publish.

Leave a note: page path, question it answers, anything you were not sure of.
```

## How you know it worked

Open a fresh agent session on the repo. Ask it to add a page for a procedure you already understand. The edit should stay on that page, use the terms in the glossary, and end with the note from step 5.

## Where this sits in the harness

The guide is what the agent sees on every session. It is memory of the rules, not memory of the docs. When the task needs a paragraph from the docs, the agent should ask the server in the next recipe, not reread this file hoping the paragraph was pasted in.

## Vibe coder, shorter

If you do not have a docs repo yet, put three lines in the editor rules: which product name to use, which docs URL is the source of truth, and "ask the MCP server before you invent a step." Then do [the short path](02-context-engineering.md#vibe-coder-paste-the-url).

## Personas

The steps for your job are in a folder: [vibe coders](../vibe-coders/README.md), [technical writers](../technical-writers/README.md), [docs engineers](../docs-engineers/README.md), [context engineers](../context-engineers/README.md), [developer advocates](../developer-advocates/README.md), [developers](../developers/README.md).

A context server is RAG exported as an MCP server: retrieval picks the passages from the sources you add, and the MCP endpoint is what a harness calls. Any server with the capabilities in [Choose a context server](choose-a-context-server.md) works for these recipes.

## Also read

- [Ship with AI](https://github.com/zthewriter/ship-with-ai)
- [Context for AI](https://github.com/zthewriter/context-for-ai)
- [Awesome Context Observability](https://github.com/zthewriter/awesome-context-observability)
