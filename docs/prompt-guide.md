# GPT-6.2 Sol prompt guide: how to prompt GPT-6.2 Sol for video

English · [简体中文](zh-CN/prompt-guide.md) · [← Back to the collection](../README.md)

GPT-6.2 Sol doesn't output video. It writes code, usually a single HTML page with Three.js, and the creator records that page playing. The patterns below come from the prompts creators shared with their posts on launch days. Each example links to the post it came from. This guide is short because the collection is young; it grows as more creators share prompts.

## 1. Write the full brief: theme, quality bar and deliverable

The most detailed prompt shared so far asks for a 3D interactive page, sets a theme, pushes for the top of the model's range, and says what to deliver. Translated from the Chinese original:

> Create a 3D interactive web page in Three.js on the theme "The End of Time." Use your highest-level aesthetic, art-design and 3D programming ability, and push composition, light, materials, particles, animation and atmosphere to the limit. … Finish development, run and test it directly, and deliver a truly playable work.

([@Khazix0918][khazix], translated) The creator's verdict on the result: the aesthetic is "强到爆炸" (overwhelmingly strong), and defensive-coding issues improved. The prompt names the renderer, the mood and the finish line ("run and test it"), and leaves the design to the model.

## 2. Keep a short brief, but name the renderer and the interaction

A one-line brief can work when it names the renderer and the thing the viewer should be able to do:

> 生成一个画面非常逼真的龙卷风，要在threejs 场景里面可以互动 ("Generate a very realistic tornado, interactive in a Three.js scene")

([@Cayden970207][cayden], translated.) The creator reports it was a one-shot result from GPT-6.2 Sol at its MAX setting, taking 22 minutes, and gave no other specification. The request is short; "Three.js" and "interactive" are what made the output a playable scene.

## 3. Use one prompt for a head-to-head

When you compare models, send the identical prompt to each, and include the constraints that make the output comparable. One creator did this against Claude Opus 5.5 for front-end design:

> 做一个让人看了就想截图分享的网页，主题自定，单文件 HTML，不使用外部图片。 ("Make a web page that people will want to screenshot and share, any theme, single-file HTML, no external images.")

([@Stargridcompass][stargrid], translated.) The single-file and no-external-image rules are what make the two pages comparable. The creator reports a clear front-end aesthetic gain for GPT-6.2 Sol and asks readers which page they prefer; the post gives no score. See the [model comparison](model-comparison.md).

## A prompt to start from

```text
Build [subject] as ONE self-contained HTML file that opens directly from disk.

Look: [style, mood, lighting, palette].
Motion: [what moves and how].
Interaction: [mouse, keyboard or click behaviour].
Rules: [any numbers, limits or constraints the scene must respect].

Technical:
- Renderer: [Three.js as an ES module from a CDN import map, or Canvas / SVG].
- No external images, fonts or audio.
- Before you finish, run and test the page and fix any errors you find.
- Return only the complete HTML, from <!DOCTYPE html> to </html>.
```

Try it on the [Lab text arena]({arena}) with GPT-6.2 Sol and other models side by side, or with the API in the [tutorial](tutorial.md).

## Settings

- **Reasoning setting.** One creator labels their run "MAX". That is the creator's report of their own setting; no measured comparison of settings exists for this model yet.
- **Output budget.** A long page is many output tokens. The API example in the [tutorial](tutorial.md) asks for `max_tokens: 128000`; check the `usage` field in the response to see what a run actually used.

---

Quotes are short excerpts credited to their authors; follow the links for full posts and videos. Translations from Chinese are ours.

[khazix]: https://x.com/Khazix0918/status/2119507514459144677
[cayden]: https://x.com/Cayden970207/status/2119464819229344113
[stargrid]: https://x.com/Stargridcompass/status/2119743048364277820
[arena]: https://www.sandbase.ai/arena/text?models=openai%2Fgpt-6.2-sol&utm_source=github&utm_medium=docs&utm_campaign=awesome-gpt-6-2-sol
