# Changelog

All notable changes to Harness Engineering Cookbook are recorded in this file. The format follows
[Keep a Changelog](https://keepachangelog.com/en/1.1.0/), and versions follow
[VERSIONING.md](VERSIONING.md).

## [Unreleased]

### Added

- `examples/docs-site/`: the whole harness for a documentation site as one
  architecture diagram, with starter files to clone: `AGENTS.md`, a context source
  map, retrieval rules, a tool catalog, a definition of done, guardrails, and a
  skill for writing a page.

## [1.0.0] - 2026-10-18

The first tagged release.

### Added

- The four parts of a harness, explained once in `recipes/`: guides, context
  engineering, tool orchestration, and guardrails.
- Persona folders with three recipes each, for vibe coders, technical writers,
  docs engineers, context engineers, developer advocates, and developers.
- Seven delivery recipes, one per channel: Markdown and `llms.txt`, an MCP server,
  a search API, files in the repository, keeping context current, proving the
  citation, and observing delivered context. Each links to its template in Context
  for AI, and each persona folder lists the ones it needs. See
  [recipes](recipes/README.md#delivery-recipes).
- A "Link to a stable version" section in the README and a headings rule in
  `VERSIONING.md`, so links to a page or a heading keep working.
- A content license, CC BY 4.0, for recipes, writing, and diagrams.
- `CONTRIBUTING.md`, `CODE_OF_CONDUCT.md`, `SECURITY.md`, `CITATION.cff`,
  `VERSIONING.md`, issue and pull request forms, and CI for links, diagrams,
  markdownlint, and secrets.
- Vendor-neutral and verified-figures items in the pull request checklist.

### Changed

- Recipes are tool-neutral. Each step names a capability, and any context server
  that has it works. One product's click path sits in a collapsible "Doing this in
  MCP Studio" block, with a disclosure. `recipes/choose-a-context-server.md` lists
  the capabilities, how to check them, and open source and hosted options.
- The MIT license names Zair Rogelio as the copyright holder, matching the related
  repositories.
- The export, keep-current, and connect recipes link to the pages that answer
  their open questions: where a client keeps its config, how to refresh on
  publish, and what to log.

[Unreleased]: https://github.com/zthewriter/harness-engineering-cookbook/compare/v1.0.0...HEAD
[1.0.0]: https://github.com/zthewriter/harness-engineering-cookbook/releases/tag/v1.0.0
