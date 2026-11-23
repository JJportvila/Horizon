---
layout: default
title: "Horizon Summary: 2026-11-23 (ZH)"
date: 2026-11-23
lang: zh
---

> 从 6 条内容中筛选出 2 条重要资讯。

---

**科技新闻**
1. [OpenAI 文章讨论困惑度与智能的关系](#item-tech-news-1) ⭐️ 7.0/10

**科技博客**
1. [在不确定时，故意乱撞](#item-tech-blog-1) ⭐️ 6.0/10

---

## 科技新闻

<a id="item-tech-news-1"></a>
### [OpenAI 文章讨论困惑度与智能的关系](https://openai.com/index/perplexity-and-intelligence/) ⭐️ 7.0/10

OpenAI 发布了一篇讨论困惑度（perplexity）与智能关系的文章，面向关注大模型评估的读者，核心议题是交叉熵和下一 token 预测这类指标能否反映模型进展。该文在 Hacker News 获得 511 分和 352 条评论，讨论集中在指标定义、跨模型可比性，以及它是否仍能解释强化学习时代的模型能力。就现有材料看，这篇文章引发的是评估方法讨论，并非新模型或新版本发布；具体实验设置和结论细节仍需以原文为准。

hackernews · acossta · 11月22日 17:06 · [社区讨论](https://news.ycombinator.com/item?id=50601525)

**「背景：困惑度是什么」** 困惑度（perplexity）衡量语言模型预测下一个 token 时的“惊讶程度”：完全随机猜测时等于词表大小，完美预测时为 1，数值越低越好；它在数学上等于平均交叉熵的指数，因此与预训练损失直接挂钩。据搜索结果，OpenAI 首席科学家 Jakub Pachocki 于 11 月 22 日发表这篇技术文章，讨论该预训练指标与模型能力之间的关系。

**「影响」** 对开发者而言，困惑度可以作为一个简单、低成本的比较信号，但跨模型比较应使用相同的留出评估集，并考虑分词器和词表大小的影响，否则数值差异不能直接当作能力差异。

**「社区讨论」** 有评论指出文章未定义困惑度，并把它解释为模型预测下一 token 的惊讶程度：最差等于词表大小，最好为 1；也有评论惊讶交叉熵在强化学习时代仍呈现清晰趋势。另有人追问 GPT-5 的困惑度是否高于 GPT-4.5，并有评论转述微软将 MAI 模型加入同一评估图表、报告 MAI-2 Base 对数困惑度为 0.819，这些说法尚未在讨论中得到独立验证。

<details><summary>参考链接</summary>
<ul>
<li>OpenAI Chief Scientist Proposes AI Pretraining Limits Tied to Perplexity Benchmarks</li>

</ul>
</details>

**标签**: `#LLM evaluation`, `#perplexity`, `#cross-entropy`, `#OpenAI`, `#model benchmarking`

---

## 科技博客

<a id="item-tech-blog-1"></a>
### [在不确定时，故意乱撞](https://seangoedecke.com/when-in-doubt-flail-about/) ⭐️ 6.0/10

rss · Sean Goedecke · 11月23日 00:00

**「背景」** 面对缺少明确指引、甚至不知道什么会有帮助的模糊情境，作者提出：与其等到理解清楚再行动，不如先“乱撞”。他也承认这是危险建议——乱撞不当会损害技术公司里的声誉，让人显得只有坏点子。

**「方案」** 关键不是盲目试错，而是同时做三件事：大量尝试不同方案，紧盯来自同事和现实结果的反馈，迅速放弃没有正反馈的方向。多方案还能避免对单一计划过度投入，因为大多数想法本就不可行，十个里可能只有一个有效。作者把这种策略分为产品、工程和组织三类：产品未找到市场契合时，可在边缘多做尝试，他以现已退役的 GitHub Models 中“用 GitHub Actions token 运行 AI 推理”最终成为“Continuous AI”种子为例；面对过于复杂或庞大的系统，与其通读全部再改，不如做一批推测性修改，看效果再决定深入；资深工程师面对团队沟通不畅或不满时，可尝试自动化、接手任务、提长期方案等，但这时尤其要敏感于反馈，失败就立刻收手，否则不满会转向自己。作者强调，从内部感受看这像反复失败和出丑，但管理者可能看到的是主动实验；这种不适是心理障碍，不应据此停下。

**「启示」** 作者的核心论点是，在真正不确定且反馈可读的情境里，快速、多方向试探并毫不留恋地淘汰失败方案，比等待完整理解更能尽快变得有用；但这依赖对反馈的敏感度和及时止损，并非所有乱撞都值得鼓励。

**标签**: `#engineering culture`, `#decision-making under uncertainty`, `#experimentation`, `#feedback loops`, `#senior engineers`

---