# GPT-6.2 Sol 对比其他模型：实测了什么，创作者报告了什么

[English](../model-comparison.md) · 简体中文 · [← 返回合集](../../README.zh-CN.md)

两类证据，分开呈现：

1. **我们测到的。** Lab [Evals 榜单][evals] 展示 Artificial Analysis 的数据；Lab [Pelican Test][pelican] 用同一份固定提示词跑每个模型并给结果打分。
2. **创作者报告的。** 发在 X 上的同提示词对比，附他们自己的提示词和设置。有参考价值，但我们没有验证。

GPT-6.2 Sol 于 2026 年 11 月 8 日宣布。下面的实测数据早于这个日期，所以**两个榜单目前都没有 GPT-6.2 Sol 的结果**。缺席本身不代表模型的分数。下面的对手行是现有最接近的实测参照。

## 我们测到的：Lab Evals 榜单

Evals 榜单上没有 GPT-6.2 Sol 这一行。下表是 2026-10-19 的 Artificial Analysis 快照，早于该模型的宣布。引用任何数字前，请重新查看[榜单][evals]。

| 模型（榜单上的行） | [智能指数][b-intel] | [输出速度][b-speed] | [单任务成本][b-cost] |
|---|---|---|---|
| **GPT-6.2 Sol** | **尚未进入榜单** | — | — |
| Claude Opus 5.5 (Max) | 57.6（第 1） | 98 tok/s（第 187） | $5.98（第 188） |
| Gemini 4 Argon (High) | 52.6（第 9） | 不在榜上 | $1.99（第 158） |
| GPT-6.1 Sol (Max) | 51.8（第 13） | 60 tok/s（第 281） | $0.724（第 112） |
| DeepSeek V4.1 Flash 1017 (Max) | 45.1（第 36） | 230 tok/s（第 33） | $0.262（第 74） |

这说明什么、不说明什么：

- **不能说明 GPT-6.2 Sol 的分数。** 上一代 GPT-6.1 Sol 在智能指数上低于 Gemini 4 Argon（52.6）和 Opus 5.5（57.6）。这是上一代模型的测量，不是新模型的。

## 我们测到的：Lab Pelican Test

[Pelican Test][pelican] 让每个模型画一只骑自行车的鹈鹕，一次静态、一次动画（只用 CSS/SMIL）。页面渲染成 PNG，由 LLM 裁判打 0–5 分。成本是 SandBase 上的实际计费金额。

2026-10-20 读取的[实时榜单][pelican]（GPT-6.2 Sol 尚无结果）：

| 排名 | 模型 | 结果数 | 得分 | 平均成本 |
|---|---|---|---|---|
| 1 | openai/gpt-6.1-sol | 6 | 3.79 | $0.026 |
| 2 | google/gemini-4-argon | 4 | 3.75 | $0.150 |
| 4 | anthropic/claude-opus-5.5 | 6 | 3.46 | $0.223 |
| 5 | deepseek/deepseek-v4.1-flash | 6 | 3.44 | $0.017 |

在 GPT-6.2 Sol 的鹈鹕图被打分之前，Pelican Test 无法给它定位。可以自己[跑一次][pelican-run]。

## 创作者报告的

X 上的同提示词对比。数字按创作者自述。点进链接可以两边一起看。三条帖子都没有给出花费，所以这里也不重复成本。

| 创作者 | 任务 | GPT-6.2 Sol | 对手 | 创作者结论 |
|---|---|---|---|---|
| [@Khazix0918][khazix] | 《时间的尽头》，Three.js 3D 交互页面，长提示词 | 审美很强；防御性问题有改善 | — | "强到爆炸" |
| [@Cayden970207][cayden] | Three.js 场景中可互动的逼真龙卷风，短提示词 | MAX 设置下一次生成，22 分钟 | — | "THE KING IS BACK" |
| [@Stargridcompass][stargrid] | 值得截图分享的单文件网页，同一提示词 | 前端审美提升"非常明显" | Claude Opus 5.5 | 请读者判断哪一个更好 |

单项运行与质量评价：

- [@Khazix0918][khazix] 对这个 Three.js 页面的审美评价很高，并称防御性问题有明显改善。
- [@Cayden970207][cayden] 报告龙卷风是一条提示词一次生成、没有修改，使用 MAX 设置。

## 怎么读这些数据

创作者的帖子大多是发布当天的单次运行，设置和工具各不相同。以上三条帖子中，只有前端对比点名了对手。把每条说法当作线索，在依赖它之前，请到[Lab 文本竞技场][arena]用同一提示词重跑一次。

---

Lab 数据：[Evals 榜单][evals]（Artificial Analysis，2026-10-19 快照）与 [Pelican Test][pelican]（2026-10-20 读取）。创作者数据：他们本人的帖子，已附链接，未经我们独立验证。

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
