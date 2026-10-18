# Contributing

Thank you for helping. This cookbook is better with more people following its
recipes and saying where a step did not work.

## How contributions work

The following rules apply to every change:

1. **Every change is a pull request.** Nobody pushes to `main` directly, including
   collaborators. `main` is protected.
2. **Every pull request is reviewed and approved by the maintainer,
   [@zthewriter](https://github.com/zthewriter), before it is merged.** The
   [CODEOWNERS](.github/CODEOWNERS) file makes that review required.
3. **The maintainer merges.** Contributors do not merge their own pull requests.
4. **Automated checks must pass** (links, Markdown style, diagrams, and a secrets
   scan) before a pull request can be merged.

You get a first response on every pull request within two business days. Not every
pull request is accepted; when one is not, you get a reason.

## What we accept

The following table shows where each kind of contribution goes:

| You want to | Put it in | Notes |
|---|---|---|
| Fix a step that did not work | The recipe | Say what you ran and what happened |
| Explain a part of a harness | `recipes/` | Guides, context engineering, tool orchestration, or guardrails |
| Add a recipe for a persona | The persona folder, such as `technical-writers/` | Open an issue first, so the scope is agreed |
| Add a delivery recipe | `recipes/` | One delivery channel per recipe |
| Add or change a template | [Context for AI](https://github.com/zthewriter/context-for-ai) | Templates live there only. A recipe links to a template and never copies it. |

## Recipe anatomy

Every recipe has the following sections, in this order:

1. An H1 title that names the outcome.
2. One paragraph on why the reader would do this.
3. `## You will have`: what exists when the recipe is done.
4. `## Steps`: a numbered list. Each step describes a capability, so it works with
   any tool that has it.
5. `## How you know it worked`: a check the reader can see, such as a cited page.
6. Optional: a collapsible section titled "Doing this in [product]" with one
   product's click path.

## Vendor neutrality

A recipe never requires a commercial product. Write the step as a capability, such
as "add the docs site as a source in your context server," and link to
[Choose a context server](recipes/choose-a-context-server.md) when a tool is
needed. A product may appear as an example only with at least one alternative
beside it, preferably open source. If you work for, own, or are paid by a product
you mention, say so in the pull request and in the text.

## Writing style

Follow the writing rules in
[Writing style for these templates](https://github.com/zthewriter/context-for-ai/blob/main/templates/style.md):
American English, sentence-case headings, second person, present tense, a lead-in
sentence before every list and table, and descriptive link text. Every Mermaid
diagram has an `accTitle` and an `accDescr`. Examples use the fictional company
Kestrel and fake values only.

## Licenses

By contributing, you agree that your contribution is licensed under
[CC BY 4.0](LICENSE-CONTENT) for recipes, writing, and diagrams, and under the
[MIT License](LICENSE) for code, scripts, workflows, and skills.

Everyone taking part follows the [Code of Conduct](CODE_OF_CONDUCT.md). To report a
leaked secret or an unsafe instruction, see [SECURITY.md](SECURITY.md).
