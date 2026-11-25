---
layout: default
title: "Horizon Summary: 2026-11-25 (ZH)"
date: 2026-11-25
lang: zh
---

> 从 9 条内容中筛选出 5 条重要资讯。

---

**科技新闻**
1. [OpenAI 预印本声称矩阵乘法指数为 9/4](#item-tech-news-1) ⭐️ 8.0/10
2. [Ternary Bonsai 2.5 27B：三元量化模型可在 24GB Mac 本地运行](#item-tech-news-2) ⭐️ 7.0/10
3. [GPT-6 蛋白质设计被指依赖专用模型](#item-tech-news-3) ⭐️ 7.0/10
4. [Simon Willison 回顾 LLM 编码代理的三个拐点](#item-tech-news-4) ⭐️ 7.0/10

**财经新闻**
1. [纽约联储主席威廉姆斯：通胀回落到 2%仍需时日，暗示未来将进一步加息](#item-finance-news-1) ⭐️ 7.0/10

---

## 科技新闻

<a id="item-tech-news-1"></a>
### [OpenAI 预印本声称矩阵乘法指数为 9/4](https://github.com/openai/math/blob/main/preprints/The-matrix-multiplication-exponent-is-nine-fourths-November-24-2026/paper.pdf) ⭐️ 8.0/10

OpenAI 在 GitHub 的 math 仓库发布了一篇预印本，声称矩阵乘法的复杂度为 Θ\(n^2.25\)，即指数为 9/4。来源目前只有标题和 PDF 链接，没有正文摘要、同行评审或独立复现，因此这是一项尚待验证的声明。若结论成立，它将把矩阵乘法的已知上界与新的下界合并为精确指数；但社区讨论已对标题中的 O/Θ 表述以及该结果究竟证明上界还是下界提出质疑。

hackernews · E-Reverance · 11月25日 01:19 · [社区讨论](https://news.ycombinator.com/item?id=50637220)

**「背景」** 矩阵乘法指数 ω 是使两个 n×n 矩阵可在 O\(n^α\) 时间内相乘的指数 α 的下确界；相关研究在讨论条件下界时引用 ω&lt;2.3716（Vas+24）作为当前上界（tool-2-2）。一个外部核查视频提到，2026 年 10 月 OpenAI 曾发布论文声称 ω≤9/4；本次预印本标题则把主张推进为精确的 9/4，这一变化仍待独立验证（tool-2-3）。

**「社区讨论」** 评论者 orlp 和 brandonb 指出，标题中的 O\(n^2.25\) 表述不准确，应写作 Θ\(n^2.25\)；他们称该结果证明的是 Ω\(n^2.25\) 下界，而 2.25 的上界此前已经知道。另有评论提到近期已有达到 O\(n^2.25\) 的算法，但距离实用仍很远。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.researchgate.net/publication/377175782_New_Bounds_for_Matrix_Multiplication_from_Alpha_to_Omega">New Bounds for Matrix Multiplication : from Alpha to Omega</a></li>
<li><a href="https://www.youtube.com/watch?v=Z2akygaVh8Q">A 32-Year-Old Did the Matrix Math Experts Thought... - YouTube</a></li>

</ul>
</details>

**标签**: `#matrix multiplication`, `#algorithms`, `#complexity theory`, `#AI for math`, `#OpenAI`

---

<a id="item-tech-news-2"></a>
### [Ternary Bonsai 2.5 27B：三元量化模型可在 24GB Mac 本地运行](https://prismml.com/news/bonsai-2-5-27b) ⭐️ 7.0/10

Ternary Bonsai 2.5 27B 发布，这是一个三元量化（Q2 GGUF）的 27B 本地模型。由于原始发布页面内容不可用，目前可核实的细节全部来自社区评论：有用户报告在 24GB 内存的 Mac Mini M5 Pro 上生成速度约 22–25 tokens/s，首个 token 约 2 秒，提示词处理约 223 tokens/s，并可轻松装下 128k 上下文，因此可用于 agentic 编码。另有评论者称该模型在 SWE-bench Verified 上的成绩与 2026 年 2 月发布的 Opus 4.6 相当，但本人也表示不确定这有多少来自基准“刷分”或基准本身的漂移，属于未经验证的社区说法。

hackernews · b0m · 11月24日 20:08 · [社区讨论](https://news.ycombinator.com/item?id=50633922)

**「背景」** Bonsai 系列由 PrismML 发布，采用三值（ternary）权重量化，把 27B 参数模型压缩到约 5.9 GB 的体积，使其能在消费级内存的机器上本地运行。据 PrismML 介绍，2.5 版本是此前 Ternary Bonsai 2 27B 的升级，沿用 Qwen3.8 27B 底座并保持相同的 5.9 GB 体积，在 AppWorld 与 τ³-Bench 等智能体工具调用基准上的平均分由此前版本的 60.2 提升到 82.2。官方文档还称，其 5.93 GB 三值权重可支持 262K token 上下文与接近 FP16 水平的工具调用能力。

**「本地部署与兼容性」** 模型权重已按 Apache 2.0 发布，可通过 llama.cpp 在 NVIDIA 与 Intel GPU 上运行，也可通过 MLX 在 Mac、iPhone、iPad 上运行，因此已有本地推理栈的用户无需更换硬件即可试用。官方 Hugging Face 页面称 5.93 GB 的量化文件即可提供 262K 上下文，并给出 SWE-bench Verified 75.6、Terminal-Bench 2.1 60.1 的厂商自报成绩；这些数字尚非独立复现，团队在用于仓库级编码代理前应在自己的任务上验证三值量化带来的精度损失。

**「社区讨论」** 评论者 ariwilson 给出了具体实测速度，并认为长上下文使其“可能”适合批量 agentic 编码，但尚未完成一次完整 agent 任务验证。thepoet 用自建的长程任务基准对比两代模型：Bonsai 2.5 与 Bonsai 2 都是 8 项通过 5 项，但步数减少 17%、总耗时减少 29%（从 107 分钟降到 76 分钟）；hatthew 则希望看到与同尺寸量化模型（如 Qwen 系列的 Q1/Q2 量化版）的直接对比。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://prismml.com/news/bonsai-2-5-27b">PrismML — Introducing Ternary Bonsai 2.5 27B: Powering ...</a></li>
<li><a href="https://prismml.com/news/prismml-launches-ternary-bonsai-2-5-27b">PrismML — PrismML Launches Ternary Bonsai 2.5 27B for Agentic ...</a></li>
<li><a href="https://docs.prismml.com/models/bonsai-2-5-27b">Ternary Bonsai 2.5 27B - Bonsai - docs.prismml.com</a></li>
<li><a href="https://prismml.com/news/bonsai-2-5-27b">PrismML — Introducing Ternary Bonsai 2 . 5 27 B : Powering Agentic...</a></li>
<li><a href="https://huggingface.co/prism-ml/Ternary-Bonsai-2.5-27B-GGUF">prism-ml/ Ternary - Bonsai - 2 . 5 - 27 B -GGUF · Hugging Face</a></li>

</ul>
</details>

**标签**: `#ternary quantization`, `#local LLM inference`, `#model release`, `#SWE-bench`, `#agentic coding`

---

<a id="item-tech-news-3"></a>
### [GPT-6 蛋白质设计被指依赖专用模型](https://openai.com/index/gpt-6-models-demonstrate-intrinsic-protein-design-capabilities/) ⭐️ 7.0/10

OpenAI 公告声称，GPT-6 系列模型（评论中具体引述为 GPT-6.2）在获得五个靶蛋白的三维结构和指定结合位点后，能自行编写代码生成候选 minibinder 的三维设计，且这一步不使用专门的蛋白质 AI 模型。但据评论引述的公告内容，要把这些设计变成可实验测试的蛋白质，仍需用 SolubleMPNN 等专门模型给出氨基酸序列，并由其他专用模型筛选可能正确折叠和结合的候选。因此，所谓“内在”蛋白质设计能力主要覆盖三维骨架和代码编排，并未覆盖序列生成与候选筛选等关键环节。现有材料未提供可独立核验的实验验证细节，该能力目前仍属 OpenAI 的声明。

hackernews · acossta · 11月24日 21:02 · [社区讨论](https://news.ycombinator.com/item?id=50634658)

**「背景」** 蛋白质设计通常先确定希望获得的三维结构，再反推能折叠成该结构的氨基酸序列，并用折叠与结合预测模型筛选候选；minibinder 是设计用来结合特定靶点的小型蛋白。通用大模型擅长写代码和串联工具，但这不等于替代专门的序列设计与筛选模型。

**「影响」** 对蛋白质工程团队而言，评估这类结果时应把“生成三维骨架”和“生成可折叠序列、筛选候选”分开核查；如果候选序列仍由 SolubleMPNN 等模型产生，就不能把整个流程算作通用模型的端到端设计能力。

**「社区讨论」** Hacker News 评论的核心争议是 GPT-6 究竟设计出了什么：fabian2k 指出氨基酸序列才是蛋白质的结构，而序列由 SolubleMPNN 生成，因此通用模型的贡献被夸大；plaidfuji 则认为更准确的定位是 LLM 充当连接专门模型与工作流的“胶水层”，并可能在某些子任务上更强。joe-esquibel 还质疑所展示证据偏重计算、实验室生物对照不足。

**标签**: `#protein design`, `#GPT-6`, `#AI for science`, `#model capabilities`, `#Hacker News discussion`

---

<a id="item-tech-news-4"></a>
### [Simon Willison 回顾 LLM 编码代理的三个拐点](https://simonwillison.net/2026/Nov/24/llm-inflection-points/) ⭐️ 7.0/10

Simon Willison 在 11 月 24 日的文章中，以 Claude Opus 4.5 发布一周年为起点，回顾过去 12 个月 LLM 与编码代理的三个能力拐点。他称，2025 年 11 月的 Opus 4.5 以及同期发布的 GPT-5.1/Codex 是第一个拐点，让编码代理从需要频繁纠错变为默认结果通常可用；第二个拐点是 2026 年 6—7 月的“Fable 类”模型，能在给定目标和工具后自主解决问题；第三个拐点是 2026 年 9—10 月前沿模型在 Blender/Three.js 3D 建模和游戏开发上的明显进步。文章还提到，Fable 5 曾因美国出口管制短暂下架并于 7 月 1 日恢复，以及 Opus 5.5 用 12 小时试玩并重新平衡游戏，使其从乏味变得有趣。

rss · Simon Willison · 11月24日 23:02

**「背景」** Claude Code 于 2025 年 2 月 24 日随 Claude 3.7 Sonnet 推出，是 Anthropic 的编程代理；到 2025 年 11 月 24 日 Claude Opus 4.5 发布时，它已存在约九个月。Willison 此前因需要频繁纠错而未把 Claude Code 当作日常主力，Opus 4.5 则让多数日常编程任务的默认结果可直接采用，这成为他回顾随后一年三个能力拐点的基线。

**「影响」** 对使用编码代理的开发者来说，这一回顾把选型标准具体化为：模型能否在给定目标和工具后减少人工纠错并自主推进。作者称 Opus 4.5 是首个让他觉得默认结果基本正确的 Claude Code 模型，而 Opus 5.5 已能通过长时间试玩迭代游戏可玩性。

**标签**: `#LLM coding agents`, `#AI engineering`, `#Claude Opus 4.5`, `#model evolution`, `#developer tools`

---

## 财经新闻

<a id="item-finance-news-1"></a>
### [纽约联储主席威廉姆斯：通胀回落到 2%仍需时日，暗示未来将进一步加息](https://www.cnbc.com/2026/11/23/john-williams-fed-inflation-rate-hikes.html) ⭐️ 7.0/10

纽约联储主席威廉姆斯周一表示，要让通胀回到美联储 2%的目标“仍有工作要做”，并称必须在“一段时间内”采取行动，确保通胀及时且持续地回落；他还预计通胀将在 2027 年更接近 2%，并在随后一年达标。市场目前完全定价 12 月 8-9 日议息会议加息 25 个基点，将联邦基金利率目标区间从 3.75%-4%上调，而威廉姆斯的讲话预计是会议前最后一场重要的官员政策表态。

rss · CNBC Finance · 11月24日 13:33

**「背景」** 美联储的长期通胀目标是 2%，而当前通胀仍明显高于该目标；负责制定利率的联邦公开市场委员会下一次会议定于 12 月 8 日至 9 日，市场已充分计入加息 25 个基点、将目标区间从 3.75%-4%上调的预期。

**「影响」** 若 12 月加息按市场定价落地，与政策利率挂钩的信用卡、浮动利率贷款等借款人的还款成本会随之上升；目前这仍属市场预期，并非已宣布的政策决定。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.cnbc.com/2026/11/23/john-williams-fed-inflation-rate-hikes.html">Fed&#x27;s John Williams indicates higher interest rates likely &#x27;over time&amp;...</a></li>
<li><a href="https://www.fxstreet.com/macroeconomics/central-banks/fed">FOMC &amp; Fed Meeting | News &amp; Analysis</a></li>

</ul>
</details>

**标签**: `#Federal Reserve`, `#monetary policy`, `#interest rates`, `#inflation`, `#John Williams`

---