# GPT-6.2 Sol vs. the rivals: what was measured, what creators reported

English · [简体中文](zh-CN/model-comparison.md) · [← Back to the collection](../README.md)

Two kinds of evidence, kept apart:

1. **What we measured.** The Lab [Evals boards][evals] show Artificial Analysis data, and the Lab [Pelican Test][pelican] runs the same fixed prompt on every model and scores the result.
2. **What creators reported.** Same-prompt posts on X, with their own prompts and settings. Useful context, not verified by us.

GPT-6.2 Sol was announced on November 8, 2026. The measured data below is older than that, so **neither board has a GPT-6.2 Sol result yet**. The absence says nothing about the model's score. The rival rows are the closest measured reference points that exist.

## What we measured: Lab Evals boards

There is no GPT-6.2 Sol row on the Evals boards. The rows below are the Artificial Analysis snapshot of 2026-10-19, which predates the model. Re-read the [boards][evals] before quoting any of them.

| Model (row on the board) | [Intelligence Index][b-intel] | [Output speed][b-speed] | [Cost per task][b-cost] |
|---|---|---|---|
| **GPT-6.2 Sol** | **not on the board yet** | — | — |
| Claude Opus 5.5 (Max) | 57.6 (#1) | 98 tok/s (#187) | $5.98 (#188) |
| Gemini 4 Argon (High) | 52.6 (#9) | not on the board | $1.99 (#158) |
| GPT-6.1 Sol (Max) | 51.8 (#13) | 60 tok/s (#281) | $0.724 (#112) |
| DeepSeek V4.1 Flash 1017 (Max) | 45.1 (#36) | 230 tok/s (#33) | $0.262 (#74) |

What this says, and what it doesn't:

- **Nothing about GPT-6.2 Sol's score.** The previous generation, GPT-6.1 Sol, sits below Gemini 4 Argon (52.6) and Opus 5.5 (57.6) on the Intelligence Index. That is a measurement of the older model, not of the new one.

## What we measured: Lab Pelican Test

The [Pelican Test][pelican] asks each model for an SVG of a pelican riding a bicycle, once static and once animated (CSS/SMIL only). The page is rendered to PNG and scored 0 to 5 by an LLM judge. Cost is the real billed amount on SandBase.

Leaderboard rows from the [live leaderboard][pelican], read 2026-10-20. GPT-6.2 Sol has no row:

| Rank | Model | Results | Score | Avg cost |
|---|---|---|---|---|
| 1 | openai/gpt-6.1-sol | 6 | 3.79 | $0.026 |
| 2 | google/gemini-4-argon | 4 | 3.75 | $0.150 |
| 4 | anthropic/claude-opus-5.5 | 6 | 3.46 | $0.223 |
| 5 | deepseek/deepseek-v4.1-flash | 6 | 3.44 | $0.017 |

Until a GPT-6.2 Sol drawing is scored, the Pelican Test cannot place the model. Run it yourself with the [Pelican Test][pelican-run].

## What creators reported

Same-prompt posts on X. Numbers are as the creator stated them. Click through to see both results. None of the three posts gives a cost, so none is repeated here.

| Creator | Task | GPT-6.2 Sol | Rival | Creator's verdict |
|---|---|---|---|---|
| [@Khazix0918][khazix] | "The End of Time", a 3D interactive page in Three.js, one long prompt | Strong aesthetic; defensive-issue handling improved | — | "强到爆炸" (overwhelmingly strong aesthetic) |
| [@Cayden970207][cayden] | A realistic interactive tornado in a Three.js scene, one short prompt | One shot at the MAX setting, 22 minutes | — | Impressed; "THE KING IS BACK" |
| [@Stargridcompass][stargrid] | Screenshot-worthy single-file web page, same prompt | Front-end aesthetic gain "非常明显" (very clear) | Claude Opus 5.5 | Asks readers which of the two is better |

Solo runs and quality notes:

- [@Khazix0918][khazix] rates the aesthetic of the Three.js page very highly and reports a clear improvement on defensive issues.
- [@Cayden970207][cayden] reports the tornado was a single prompt with no revisions, at the MAX setting.

## How to read this

Creator posts are single runs, often on launch day, with different settings and tools. Of the three posts above, only the front-end test names a rival. Treat each claim as a lead, and rerun the same prompt in the [Lab text arena][arena] before you rely on it.

---

Lab data: [Evals boards][evals] (Artificial Analysis, snapshot 2026-10-19) and [Pelican Test][pelican] (read 2026-10-20). Creator data: their posts, linked; not independently verified.

[evals]: https://www.sandbase.ai/leaderboards?utm_source=github&utm_medium=docs&utm_campaign=awesome-gpt-6-2-sol
[b-intel]: https://www.sandbase.ai/leaderboards?utm_source=github&utm_medium=docs&utm_campaign=awesome-gpt-6-2-sol&utm_content=intelligence
[b-speed]: https://www.sandbase.ai/leaderboards?utm_source=github&utm_medium=docs&utm_campaign=awesome-gpt-6-2-sol&utm_content=speed
[b-cost]: https://www.sandbase.ai/leaderboards?utm_source=github&utm_medium=docs&utm_campaign=awesome-gpt-6-2-sol&utm_content=cost
[pelican]: https://www.sandbase.ai/arena/pelican-test?utm_source=github&utm_medium=docs&utm_campaign=awesome-gpt-6-2-sol
[pelican-run]: https://www.sandbase.ai/arena/pelican-test?utm_source=github&utm_medium=docs&utm_campaign=awesome-gpt-6-2-sol&utm_content=run
[arena]: https://www.sandbase.ai/arena/text?models=openai%2Fgpt-6.2-sol&utm_source=github&utm_medium=docs&utm_campaign=awesome-gpt-6-2-sol
[khazix]: https://x.com/Khazix0918/status/2119507514459144677
[cayden]: https://x.com/Cayden970207/status/2119464819229344113
[stargrid]: https://x.com/Stargridcompass/status/2119743048364277820
