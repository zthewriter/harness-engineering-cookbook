# Observe delivered context

This recipe sets up the signals that show how your delivered docs are used: which
passages answered which questions, which agents fetched which pages, and where
answers fell short. The tools for each signal are listed in
[Awesome Context Observability](https://github.com/zthewriter/awesome-context-observability).

## Who

Docs engineers and context engineers, and technical writers who decide what to fix
next.

## You will have

One signal per delivery channel, and a monthly reading of what it showed.

## 1. Pick a signal for each channel

Match each channel in your
[context delivery plan](https://github.com/zthewriter/context-for-ai/blob/v1.0.0/templates/harness/context-delivery-plan.md)
to the category of tool that observes it:

| Channel | What to observe | Category in Awesome Context Observability |
|---|---|---|
| MCP server or API | Which passages answered which questions | [Answer and passage analytics](https://github.com/zthewriter/awesome-context-observability#answer-and-passage-analytics) |
| Your own retrieval pipeline | Each step from question to passages | [Retrieval tracing](https://github.com/zthewriter/awesome-context-observability#retrieval-tracing) |
| Markdown and `llms.txt` | Which agents and crawlers fetched which pages | [AI agent and crawler traffic](https://github.com/zthewriter/awesome-context-observability#ai-agent-and-crawler-traffic) |
| Public docs in AI search | Whether AI search tools cite your pages | [AI search visibility](https://github.com/zthewriter/awesome-context-observability#ai-search-visibility) |
| A hosted docs platform | The AI insights your platform reports | [Docs platforms with AI insights](https://github.com/zthewriter/awesome-context-observability#docs-platforms-with-ai-insights) |

## 2. Keep what you log within your retention policy

Questions can contain personal data. Decide how long you keep question text and
returned passages before you turn logging on, and write it in your security and data
page.

## 3. Read the signal monthly

Each month, list the questions with weak or no answers, and the pages cited most and
least. Each weak question is either a missing page or a page that needs rewriting.

## How you know it worked

You can answer three questions from data, not memory: which page answered the most
questions last month, which question had no good answer, and which channel was used
most.

## Also read

- [Prove the citation](11-prove-the-citation.md)
- [Standards and specs](https://github.com/zthewriter/awesome-context-observability#standards-and-specs)
