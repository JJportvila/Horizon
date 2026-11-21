---
layout: default
title: "Horizon Summary: 2026-11-21 (ZH)"
date: 2026-11-21
lang: zh
---

> 从 15 条内容中筛选出 8 条重要资讯。

---

**科技新闻**
1. [Levent Alpöge 宣称证明广义黎曼猜想，附约 1.3GB Lean 归档](#item-tech-news-1) ⭐️ 8.0/10
2. [GitHub 仓库宣称给出纳维–斯托克斯方程有限时间爆破](#item-tech-news-2) ⭐️ 8.0/10
3. [Inkling 2 Mini：循环架构开放权重模型引发本地推理讨论](#item-tech-news-3) ⭐️ 7.0/10
4. [arXiv 论文称语言模型可不靠梯度重写自身权重](#item-tech-news-4) ⭐️ 7.0/10
5. [Signal 讨论限制移动操作系统上的 AI 代理抓取数据](#item-tech-news-5) ⭐️ 7.0/10

**科技博客**
1. [输出缓存为何收效甚微](#item-tech-blog-1) ⭐️ 6.0/10

**财经新闻**
1. [沃什回避利率指引，美联储官员公开表态反而增多](#item-finance-news-1) ⭐️ 7.0/10
2. [美国公司转向净发行股票，或成牛市供给逆风](#item-finance-news-2) ⭐️ 7.0/10

---

## 科技新闻

<a id="item-tech-news-1"></a>
### [Levent Alpöge 宣称证明广义黎曼猜想，附约 1.3GB Lean 归档](https://alpo.ge/remark.pdf) ⭐️ 8.0/10

Levent Alpöge 于 2026 年 11 月 20 日在个人站点发布 PDF（alpo.ge/remark.pdf），宣称给出了广义黎曼猜想（GRH）的证明。该文稿目前只是作者单方面发布的声明，尚无同行评审或独立验证；Hacker News 讨论中出现的配套材料同样未经核实。评论者 djoldman 称配套 Lean 形式化证明约 1.3GB、约 1500 万行代码，并贴出将 14 个分卷下载、合并解压并统计体积与行数的命令，但没有报告该归档是否已在 Lean 中编译通过。另有评论者 Jaxan 指向 math216.wordpress.com 上一份被称为“纯人类证明”的“匆忙公告”，以及一条相关的 Masullo GRH 讨论帖。

hackernews · iamronaldo · 11月20日 14:16 · [社区讨论](https://news.ycombinator.com/item?id=50574968)

**「背景」** 广义黎曼猜想（GRH）是黎曼猜想的推广：经典版本约束素数计数偏离预测值的幅度，广义版本则对等差数列中的素数给出类似界。Levent Alpöge 是 Anthropic 的数学家，他于 2026 年 11 月 20 日在个人网站发布 PDF 与 Lean 代码，称与 Claude 一起得到了黎曼猜想及其推广形式的证明；State of Proof 表示尚未审查该证明。

**「影响与待验证之处」** 对关心形式验证的读者来说，决定性的检验不是归档体积，而是这份约 1.3GB 的 Lean 代码能否在 Lean 内核中完整编译通过；截至目前，公开讨论只涉及下载、解压和行数统计，没有编译验证结果。在独立复核出现之前，把 GRH 当作已证定理来引用其条件性结论的研究者应继续按未验证处理。

**「社区讨论」** 评论者对这一声明的可信度看法不一：z7 引用陶哲轩一个月前的说法，称 AI 公司即便暗中投入也“碰不到”黎曼猜想，可能需要到 2050 年前后靠人机结合才有进展；synapsomorphy 则感慨进展之快，并表达了对 AI 风险与“暂停”的担忧。Jaxan 的评论提供了另一条线索，即同时存在一份非机器生成的证明文稿，但该说法同样只是评论者的一家之言。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://stateofproof.org/paper-watch/paper-2026-11-20-a-claimed-proof-of-the-riemann-hypothesis">A Claimed Proof of the Riemann Hypothesis — Paper Watch ...</a></li>
<li><a href="https://explainx.ai/blog/levent-alpoge-anthropic-riemann-hypothesis-claude-lean-proof-claimed-vs-verified-2026">Riemann Hypothesis Proof Claim: Claimed vs Verified ...</a></li>

</ul>
</details>

**标签**: `#Generalized Riemann Hypothesis`, `#Lean theorem proving`, `#formal verification`, `#AI for mathematics`, `#mathematical proof`

---

<a id="item-tech-news-2"></a>
### [GitHub 仓库宣称给出纳维–斯托克斯方程有限时间爆破](https://github.com/tristanbuckmaster/navier-stokes/) ⭐️ 8.0/10

2026 年 11 月 20 日，一个位于 tristanbuckmaster/navier-stokes 的 GitHub 仓库在 Hacker News 上被提交并引发大量讨论，其标题宣称给出了纳维–斯托克斯方程的有限时间爆破结果。但所提供的材料中没有该仓库的任何正文内容：没有证明概要、预印本链接，也没有同行评议或独立复核记录，因此这目前只是发布者的单方面声明，无法核实。评论者称该结果针对的是无外力（unforced）的方程，与更早一个据称借助专门设计的外部力构造反例的工作不同，并把此事与“千禧年难题”联系在一起。仅凭现有信息，无法判断该证明是否成立。

hackernews · trotro · 11月20日 15:34 · [社区讨论](https://news.ycombinator.com/item?id=50576232)

**「背景」** 纳维–斯托克斯方程的存在性与光滑性问题，问的是从光滑初值出发是否总有全局光滑解，还是可能在有限时间内发生爆破、使解失去光滑性；该问题被列为千禧年大奖难题之一。\[tool-1-1\]\[tool-1-2\] 此次仓库所附论文声称处理的是无强迫方程，而非带光滑外力的版本，并称其爆破论证依赖一个经区间算术检验的近似自相似剖面证书。\[tool-1-1\]\[tool-1-2\] 仓库说明论文作者为 L. Alpöge 与 T. Buckmaster，内容还包括一个将论文陈述与证明形式化的 Lean 4 包。\[tool-1-3\]

**「影响」** 对研究者和评审者而言，实际差别在于判定标准：OpenAI 在 2026 年 9 月公布的结果被描述为借助精心设计的外力使方程在有限时间失效，而这里声称的是无外力版本，若成立，对应的正是千禧年问题的原始表述，无需额外构造 forcing 项。可对照的是，OpenAI 当时同时公布了证明文稿与 Lean 形式化，因此评估这一新声称的第一步应是查证仓库中是否附有同等可核查的完整论证，而非依据社区转述判断。

**「社区讨论」** 评论者主要在争论这一结果的分量与性质：xianshou 认为，连同广义黎曼猜想和 OpenAI 十月的发布，这一天堪称数学史上最重要的日子之一；tancop 则指出这是无外力版本，比依赖人为设计外力的构造更“真实”。jrflo 提到关于 Anthropic 与某项千禧年难题的传闻，称 Buckmaster 和 Alpoge 可能因此被“抢先”；ninkendo 追问能否用实时数值模拟直观展示爆破过程，并质疑 OpenAI 此前发布的龙卷风状箭头图是否只是示意图。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Navier%E2%80%93Stokes_priority_controversy">Navier–Stokes priority controversy - Wikipedia</a></li>
<li><a href="https://aixiv.online/abs/2611.02204">[2611.02204] Finite-time blow-up for the Navier–Stokes ...</a></li>
<li><a href="https://hotrepo.ai/tristanbuckmaster/navier-stokes">tristanbuckmaster/navier-stokes: Lean 4 formalization of a ...</a></li>
<li><a href="https://openai.com/index/navier-stokes-solution/">On the Navier–Stokes Millennium Prize Problem | OpenAI</a></li>
<li><a href="https://www.scientificamerican.com/article/ai-just-solved-the-real-navier-stokes-problem/">AI just solved the “real” Navier-Stokes problem</a></li>

</ul>
</details>

**标签**: `#Navier-Stokes`, `#mathematics`, `#fluid dynamics`, `#proof`, `#Hacker News`

---

<a id="item-tech-news-3"></a>
### [Inkling 2 Mini：循环架构开放权重模型引发本地推理讨论](https://thinkingmachines.ai/news/inkling-2-mini/) ⭐️ 7.0/10

新的开放权重语言模型 Inkling 2 Mini 正受到关注，其特点是采用循环（looped）Transformer 架构，并强调面向本地使用。目前缺少可核验的原始发布文章，社区提到的“达到 Qwen3.8-27B 水平”等基准说法尚未得到独立验证。已有用户在 llama.cpp/GGUF 上试跑：有人报告 Ryzen 395 上约 27 tokens/s、M1 Pro 32GB 上约 10 tokens/s，但需要若干未合并 PR 和一个据称可提速约 30% 的补丁，结果尚待复现。初步编码测试评价不一，简单 Python 脚本任务完成良好，较复杂的识别任务则失败。

hackernews · jasondavies · 11月20日 20:12 · [社区讨论](https://news.ycombinator.com/item?id=50581260)

**「背景」** 循环式 Transformer（looped transformer）与常规模型每个 token 只依次过一遍各层不同：它让中间层对同一个 token 重复计算多次，以增加单个 token 的计算量来换取更少的输出 token 完成推理，官方称这对 agentic 编程等依赖推理质量的任务尤其有意义。Inkling 2 Mini 采用 26B 总参数、每 token 激活 5.4B 的 MoE 结构，定位为可在 32GB 以上内存的 Mac 上本地运行。

**「本地部署影响」** 对本地用户而言，模型可在 16GB 至 24GB 内存的设备上通过 llama.cpp 或 Unsloth 运行，但早期适配仍不完整：有测试者指出需先合入多个尚未合并的 llama.cpp PR，并自行打补丁才能获得约 30% 的推理提速。实际吞吐因硬件和量化而异，M1 Pro 32GB 上约 10 tokens/s，Ryzen 395 配合 Vulkan 约 27 tokens/s，部署前需按自身配置验证。

**「社区讨论」** 评论者一方面认为，若基准在真实场景成立，循环架构模型达到 Qwen3.8-27B 级别会“非常惊人”；另一方面，实际试跑显示本地速度可用但编码能力不稳定，简单任务通过、复杂任务失败。还有评论转述开发者称训练端到端使用 nvfp4、模型尺寸参考了本地用户需求，并有人提出开放权重循环架构对安全与可解释性的影响值得关注。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://thinkingmachines.ai/news/inkling-2-mini/">Introducing Inkling 2 Mini - Thinking Machines Lab</a></li>
<li><a href="https://ollama.com/library/inkling-2-mini">inkling - 2 - mini</a></li>
<li><a href="https://thinkingmachines.ai/news/inkling-2-mini/">Introducing Inkling 2 Mini - Thinking Machines Lab</a></li>
<li><a href="https://unsloth.ai/docs/models/inkling-2-mini">Inkling 2 Mini - Run Locally Guide | Unsloth Documentation</a></li>

</ul>
</details>

**标签**: `#LLMs`, `#open weights`, `#looped transformers`, `#local inference`, `#model release`

---

<a id="item-tech-news-4"></a>
### [arXiv 论文称语言模型可不靠梯度重写自身权重](https://arxiv.org/abs/2611.21885) ⭐️ 7.0/10

一篇发布在 arXiv 的论文（编号 2611.21885，11 月 20 日出现在 Hacker News 讨论中）声称，语言模型首次能够仅凭自身推理重写自己的权重并变得更好，全程不使用梯度、也不进行训练。据讨论区引述的摘要，模型会在练习题上检验自己的编辑，只提交有效的改动，且每次编辑都在上一次基础上改进，在连续八次会话中准确率持续上升。目前没有提供论文正文，因此具体模型、基准数据集、准确率数值以及改进幅度都无法核实。评论者还指出，演示中唯一可见的自我改进是缩短推理链以避开 token 上限，这使“自我提升”的适用范围显得相当狭窄。

hackernews · lwhsiao · 11月20日 16:29 · [社区讨论](https://news.ycombinator.com/item?id=50577265)

**「背景」** 按照目前的常规做法，语言模型一旦训练完成，权重就被冻结；想让它变得更强，通常需要再跑一次训练，或者依赖提示词、外部框架和推理阶段的额外计算。这些手段一旦任务结束就失效，不会在模型权重中留下任何痕迹，arXiv 摘要正是把这一点作为对比前提。此前一个相关的探索是 Google 的 SLEEP 框架：它在离线的“睡眠”阶段解锁预先分配的 MoE 记忆块，并用模型自己生成的练习题更新数值权重（tool-3-1），而这篇论文声称自己是首个不借助梯度、也不经过训练，仅凭模型自身推理改写权重的工作。

**「影响」** 对打算跟进或复现这条路线的人，首要的检查点是基线模型本身是否存在明显缺陷：评论者 aesthesia 指出，本次自我编辑带来的收益来自缩短推理轨迹、避免触及 token 限制，其性质与近期一项权重空间编程工作的结论相似，即在此类明显缺陷被修复后，模型性能便难以继续提升。因此，在引用“无需训练即可自我改进”的结论前，应区分模型在自选练习题上的通过率与真实任务上的表现。

**「社区讨论」** 评论者主要质疑“新颖性”与“无训练”这两个说法：aesthesia 认为唯一有效的自我修改就是缩短推理链以避开 token 上限，并把这一点与已有的权重空间编程结果相比较；Toutouxc 则追问，在练习题上筛选“只提交有效编辑”的做法与训练究竟有何实质区别。gavinray 提到 Google 的 Sleep 框架同样会在离线阶段用自生成样本更新权重，而 LarsDu88 从安全角度提出担忧，认为自主运行的模型可能借类似机制抑制与安全对齐相关的激活。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arxiv.org/abs/2611.21885">[2611.21885] Language Models Can Rewrite Their Own Weights</a></li>
<li><a href="https://research.google/blog/the-sleep-framework-a-new-way-for-llms-to-retain-knowledge-in-continual-learning/">The sleep framework : A new way for LLMs to retain knowledge in...</a></li>

</ul>
</details>

**标签**: `#self-modifying models`, `#weight editing`, `#LLM research`, `#AI safety`, `#arXiv`

---

<a id="item-tech-news-5"></a>
### [Signal 讨论限制移动操作系统上的 AI 代理抓取数据](https://signal.org/blog/protecting-your-privacy/) ⭐️ 7.0/10

Signal 发布博客文章，讨论在移动操作系统层面限制 AI 代理抓取敏感用户数据。由于未提供博客正文，现有材料没有给出具体版本、适用平台、已上线的拦截机制或可验证的测试结果；目前能确认的是文章聚焦平台级隐私控制，而非发布一项新功能。

hackernews · dotcoma · 11月20日 09:42 · [社区讨论](https://news.ycombinator.com/item?id=50572348)

**「背景」** Signal 此前已在应用内实施截图阻断，据 The Register 报道，该措施最初用于对抗微软的 Recall 屏幕记录功能。Signal 在博客中主张，AI 代理被直接整合进操作系统却缺乏基本约束，会对应用层隐私以及独立开发者保护敏感数据的能力构成威胁。路透社报道称，Signal 于 11 月 20 日宣布将这一限制扩展至阻止 AI 代理读取手机上的私密聊天。

**「社区讨论」** 评论者 pajamasam 援引 Meredith Whittaker 的说法称，风险不只来自用户自己安装的 AI 应用：联系人设备上的代理也可能读取 Signal 聊天并造成泄露，并称 Signal 对相关限制持谨慎乐观态度。另一些评论者认为应用层防截图治标不治本，呼吁公开取证结果并让用户重新掌控操作系统；也有用户抱怨 Signal 的 VPN/验证码流程和 Windows 截图限制影响正常使用。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://signal.org/blog/protecting-your-privacy/">Signal is Serious About Protecting Your Privacy</a></li>
<li><a href="https://www.reuters.com/legal/litigation/signal-restricts-screenshots-block-ai-agents-reading-messages-2026-11-20/">EXCLUSIVE: Signal restricts screenshots to block AI agents ...</a></li>
<li><a href="https://www.theregister.com/security/2026/11/20/signal-slams-door-on-prying-ai-agents-to-protect-privacy/5311466">Signal slams door on prying AI agents to protect privacy</a></li>

</ul>
</details>

**标签**: `#privacy`, `#security`, `#mobile OS`, `#AI agents`, `#Signal`

---

## 科技博客

<a id="item-tech-blog-1"></a>
### [输出缓存为何收效甚微](https://seangoedecke.com/why-output-caching-doesnt-work/) ⭐️ 6.0/10

rss · Sean Goedecke · 11月21日 00:00

**「背景」** LLM 推理成本很大程度上取决于缓存输入，以免每条消息都重算完整对话；作者由此追问：输出是否也应缓存，毕竟重复输出既浪费 token，又比输入 token 更贵。

**「方案」** 作者设想的输出缓存并非缓存最终文本，而是让模型用“src/script.py:12-15”这类引用代替重复粘贴，再由 harness 透明展开实际内容。但他认为，这只能优化用户可见的输出，而模型内部思维链通常不必重复已有信息；根据他自己的 agent 历史，可见输出仅约占 6%，推理 token 占 50%，工具调用占 44%。因此受 Amdahl 定律限制，即便乐观地省掉可见输出三分之二的 token，也只能减少总输出 token 的约 4%。他指出，要真正降低输出成本，必须减少那 94% 的不可见 token，这主要取决于模型智能，也部分取决于 harness 质量；更强模型能用更少推理和工具调用得到答案，甚至出现单价贵 5 倍但总 token 少 6 倍、总成本反而更低的情况。作者也承认自己无法读取前沿模型的思维链，对工具调用是否重复并不确定，相关判断只是基于开放模型和自身经验的推测。

**「启示」** 作者的核心结论是，输出缓存只能触及很小一部分可见输出，真正降低输出成本要靠更聪明的模型和更高效的 harness；更贵但更强的模型可能因 token 用量大幅减少而总体更便宜。

**标签**: `#LLM inference economics`, `#output caching`, `#coding agents`, `#token costs`, `#Amdahl&\#x27;s law`

---

## 财经新闻

<a id="item-finance-news-1"></a>
### [沃什回避利率指引，美联储官员公开表态反而增多](https://www.cnbc.com/2026/11/20/warsh-fed-forward-guidance-rate-hikes.html) ⭐️ 7.0/10

据报道，美联储主席凯文·沃什上任六个月来一直避免就利率走向给出前瞻指引，而美国银行的分析显示，过去两周美联储官员的公开讲话（即所谓“美联储讲话”）数量为 2025 年初以来同期最多；该行经济学家认为，沃什不引导市场可能反而促使其他 FOMC 委员更多发声。报道称，联邦公开市场委员会（FOMC）分歧加深，行长克里斯托弗·沃勒提出 12 月下次会议可能加息半个百分点（50 个基点），而据芝商所 FedWatch，交易员认为 12 月至少加息 25 个基点的概率为 100%。

rss · CNBC Finance · 11月20日 21:10

**「背景」** 凯文·沃什于 2026 年出任美联储主席，此前他公开反对“前瞻指引”，即央行提前向市场暗示未来利率路径的做法。美联储在 10 月会议上以 10 比 2 的票数决定将基准利率维持在 3.75%至 4.00%不变，两名官员则主张加息 25 个基点。

**「影响」** 据芝商所 FedWatch 工具，交易员认为 12 月至少加息 25 个基点的概率为 100%；若这一预期兑现，信用卡和浮动利率贷款等与政策利率挂钩的借贷成本将上升，对利率敏感的家庭与企业会最先受到影响。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Kevin_Warsh">Kevin Warsh - Wikipedia</a></li>
<li><a href="https://economics.td.com/us-fomc-minutes">U.S. FOMC Meeting Minutes (October 28, 2026) - TD</a></li>
<li><a href="https://www.cmegroup.com/markets/interest-rates/cme-fedwatch-tool?redirect=/trading/interest-rates/fed-funds.html">FedWatch - CME Group</a></li>

</ul>
</details>

**标签**: `#Federal Reserve`, `#monetary policy`, `#interest rates`, `#forward guidance`, `#FOMC`

---

<a id="item-finance-news-2"></a>
### [美国公司转向净发行股票，或成牛市供给逆风](https://www.cnbc.com/2026/11/20/equity-issuance-bull-market-problem.html) ⭐️ 7.0/10

美国公司已从回购股票转向净发行股票；Acadian Asset Management 的分析显示，截至上周晚些时候，净新股发行相当于总市值的 3.1%，仍低于科技泡沫和新冠泡沫时期的峰值。该机构投资经理 Owen Lamont 称，这可能给已持续四年的牛市增加供给压力。

rss · CNBC Finance · 11月20日 14:15

**「背景」** 多年来，公司回购会减少可交易股票数量，从而帮助推高股价并抬高每股收益；如今转为净发行，则增加市场需要消化的股票供给。Lamont 在投资者信中把这一变化概括为“聪明钱为何卖出”，并称不能排除当前处于 AI 泡沫之中。

**「影响」** 对现有股东而言，股票供给增加可能在需求不变时稀释每股收益，并成为估值面临的潜在逆风；但这是 Acadian 分析提出的市场压力，并非已经实现的结果。

**标签**: `#equity issuance`, `#share buybacks`, `#stock market supply`, `#IPOs`, `#AI capex`

---