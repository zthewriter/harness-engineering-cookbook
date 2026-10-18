# Ship context in the repo

This recipe delivers context as files next to the code: an `AGENTS.md`, rules
files, and skills. A coding agent working in the repository reads them without
calling anything.

## Who

Internal engineers, docs engineers, and context engineers who maintain a repository
that coding agents work in.

## You will have

An `AGENTS.md` at the repository root, a definition of done it links to, and one
skill for a procedure your team repeats.

## 1. Write AGENTS.md

List the commands, the conventions review enforces, the boundaries, and where the
longer docs live. Keep it short, because it is read on every task. Use the
[AGENTS.md template](https://github.com/zthewriter/context-for-ai/blob/v1.0.0/templates/harness/agents-md.md).
The format is described at [agents.md](https://agents.md).

## 2. Write the definition of done

List the checks work must pass, each with a command. Link it from `AGENTS.md`. Use
the
[definition of done template](https://github.com/zthewriter/context-for-ai/blob/v1.0.0/templates/harness/definition-of-done.md).

## 3. Add one skill

Pick the procedure your team explains to agents most often and write it as a
`SKILL.md`, following the [Agent Skills specification](https://agentskills.io/specification).
Use the
[agent skill template](https://github.com/zthewriter/context-for-ai/blob/v1.0.0/templates/harness/agent-skill.md).
Where each coding tool looks for skills differs. The
[Ship with AI skills page](https://github.com/zthewriter/ship-with-ai/blob/v1.0.0/skills/README.md)
lists install locations for several tools.

## 4. Add rules files only where your tool needs them

Some coding tools read their own rules files as well as `AGENTS.md`. Keep one source
of truth: put the content in `AGENTS.md`, and make any tool-specific file point to it.

## How you know it worked

Use the following checks:

- Ask a coding agent to run the tests. It uses the command from `AGENTS.md`.
- Ask it to do the procedure in your skill. It follows the skill's steps and reports
  in the skill's format.
- Ask it to do something a boundary forbids. It refuses or asks first.

## Also read

- [Guides](01-guides.md)
- [Guardrails](04-guardrails.md)
