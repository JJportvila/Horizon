---
layout: default
title: "Horizon Summary: 2026-11-17 (ZH)"
date: 2026-11-17
lang: zh
---

> 从 19 条内容中筛选出 4 条重要资讯。

---

**科技新闻**
1. [vLLM v0.34.0：KV 缓存默认扩展并移除 Model Runner V1](#item-tech-news-1) ⭐️ 8.0/10
2. [卡内基梅隆推出 CS Learn，免费发布完整课程](#item-tech-news-2) ⭐️ 7.0/10
3. [Jiff 1.0 发布：Rust 日期时间库](#item-tech-news-3) ⭐️ 7.0/10

**财经新闻**
1. [黄仁勋辞职后，ETF 专家称 AI 交易或转向大型科技股](#item-finance-news-1) ⭐️ 8.0/10

---

## 科技新闻

<a id="item-tech-news-1"></a>
### [vLLM v0.34.0：KV 缓存默认扩展并移除 Model Runner V1](https://github.com/vllm-project/vllm/releases/tag/v0.34.0) ⭐️ 8.0/10

vLLM 发布 v0.34.0，包含 1,061 个提交和 10 个新模型，例如 Mistral Large 4、MiniMax-M3.1-Flash 与 Nemotron-3.5-Transcribe。该版本默认启用可扩展 KV 缓存，按预热后实际空闲显存确定缓存大小；发布说明举例称 MiniMax-M3 在 H200 上从 433k 增至 672k tokens，但部分模型在并发 128 时 TPOT 上升 6–18%。Model Runner V1 被移除，V2 成为唯一 GPU runner；发布说明还列出 Blackwell 和 MI355X 上最高 1.95× decode 等加速。升级前需注意默认 block size 从 16 改为 64、ROCm 7.2 制品不再发布、要求 huggingface\_hub &gt;= 2.0.0，以及 QuTLASS/fp\_quant 和 Marlin W4A8 被移除。

github · khluu · 11月16日 23:22

**「背景」** vLLM 是面向大语言模型推理与在线服务的开源引擎，KV 缓存保存注意力计算所需的键和值，其容量会直接影响并发吞吐与首 token 延迟。此前 vLLM 通过 \`gpu\_memory\_utilization\` 预留显存比例来估算缓存大小，并在 GPU 执行层保留 Model Runner V1 与 V2 两条路径。v0.34.0 将 V2 变为唯一 runner，并改为在预热后按实际空闲显存确定 KV 缓存容量。

**「升级影响」** 现有部署升级时，若仍设置 \`VLLM\_USE\_V2\_MODEL\_RUNNER=0\` 会在启动时失败，V1 logits processor 需迁移到 \`vllm.v1.worker.gpu.sample.logits\_processor\`；要保留旧的缓存大小计算方式，可显式传入 \`--gpu-memory-utilization 0.9\` 或 \`--no-enable-extensible-kv-cache\`。

**标签**: `#vLLM`, `#LLM inference`, `#KV cache`, `#GPU performance`, `#open source`

---

<a id="item-tech-news-2"></a>
### [卡内基梅隆推出 CS Learn，免费发布完整课程](https://www.cs.cmu.edu/learn/) ⭐️ 7.0/10

卡内基梅隆大学格里芬计算机科学学院讲师 Phillip Compeau 推出 CS Learn，在 YouTube 免费发布当前 CMU 计算机科学课程的完整学期讲座，本周每天上线一门，并计划明年 1 月增加更多课程。项目由一个小团队运营，部分学生开发工具自动完成大量制作工作。已提到的课程包括 Tianqi Chen 的机器学习系统课程，15-259《概率与计算》也预告即将上线。

hackernews · pcompeau · 11月16日 20:43 · [社区讨论](https://news.ycombinator.com/item?id=50522980)

**「背景」** Compeau 在讨论中承认，MIT 大约 25 年前就把课程公开上网，因此开放课程本身并不新。CS Learn 的差异在于发布当前 CMU 课程的完整学期讲座，并借助学生开发的自动化制作工具，降低制作所需的人力。

**「影响」** 对独立学习者而言，CS Learn 提供了免费获取 CMU 当前课程完整讲座的渠道；但评论指出，若缺少配套项目、作业和反馈，讲座的学习效果会受限，配套课程材料是否以及何时推出值得关注。

**「社区讨论」** JSR\_FDED 认为，扎实掌握基础会让 AI 成为学习者的强力工具，否则更可能被 AI 取代；ecshafer 则提醒，讲座若缺少项目和反馈，效果会打折扣，并指出这类发布常只覆盖入门课程而缺少研究生编译器等高阶课程。

**标签**: `#computer science education`, `#open courseware`, `#online learning`, `#Carnegie Mellon`, `#machine learning systems`

---

<a id="item-tech-news-3"></a>
### [Jiff 1.0 发布：Rust 日期时间库](https://burntsushi.net/jiff/) ⭐️ 7.0/10

Jiff 1.0 已作为 Rust 日期时间库发布，为 Rust 开发者提供了一个处理日期和时间的新选择；项目文档同时明确说明它并非适用于所有场景。该库由 burntsushi 开发，发布后在 Hacker News 上引发了围绕 datetime API 设计、TAI/UT1 等时间尺度以及生态采用的讨论。现有材料没有给出 1.0 的变更日志、性能数据或与 chrono 的兼容性细节，因此这些方面尚不能确认。

hackernews · burntsushi · 11月16日 16:53 · [社区讨论](https://news.ycombinator.com/item?id=50519744)

**「背景」** Rust 生态长期将 chrono 作为常用的日期时间库；在本条讨论中，曾维护 chrono 约五年的 quodlibetor 描述了其 API 稳定但难以改进的取舍。Jiff 由 BurntSushi 开发，其仓库将 Jiff 定位为提供难以误用的高层日期时间原语，并可通过 crate feature 嵌入时区数据库、启用 serde 支持。

**「影响」** 对正在选型的 Rust 项目来说，Jiff 1.0 提供了一个可评估的 chrono 替代方案，但是否迁移仍取决于 API 兼容性、时间尺度支持和生态库集成；评论区的采用期待不构成迁移证据。

**「社区讨论」** 一位自称维护 chrono 约五年的评论者表示，chrono 的 API 稳定性既是用户采用的原因，也使改进遭遇阻力，并称对 burntsushi 的新库心怀感激；另一位评论者赞赏 Jiff 明确承认自己并非适用于所有场景。还有开发者追问 TAI、UT1 等时间尺度以及百万年到十亿年跨度下的精度处理，显示时间尺度支持是实际使用中的关注点。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/BurntSushi/jiff">GitHub - BurntSushi/jiff: A datetime library for Rust that ...</a></li>
<li><a href="https://docs.rs/jiff/latest/jiff/">jiff - Rust - Docs.rs</a></li>

</ul>
</details>

**标签**: `#Rust`, `#datetime`, `#libraries`, `#open-source`, `#time-scales`

---

## 财经新闻

<a id="item-finance-news-1"></a>
### [黄仁勋辞职后，ETF 专家称 AI 交易或转向大型科技股](https://www.cnbc.com/2026/11/14/nvidia-ai-trade-data-centers-congress.html) ⭐️ 8.0/10

英伟达 CEO 黄仁勋辞职后，CNBC 的 ETF（交易所交易基金）专家认为，若民主党掌控的国会放缓数据中心建设，AI（人工智能）交易可能转向大型科技公司和替代芯片商；Yorkville Ives 同时将英伟达目标价从 300 美元下调至 225 美元，维持买入评级，该股当周收于 162.85 美元。

rss · CNBC Finance · 11月16日 12:13

**「背景」** 英伟达于 11 月 12 日宣布黄仁勋辞去 CEO 等职务，此前路透报道称其因婚外情曝光而陷入危机。11 月 3 日中期选举后民主党赢得国会控制权，部分民主党人随后呼吁限制 AI 数据中心建设。

**「影响」** 据 Yorkville Ives 估计，民主党掌控国会若收紧数据中心建设，低端为 10%、高端为 15%-20%的已规划数据中心可能无法落地，这将影响云与数据中心运营商，但该公司称需求仍以 4 比 1 超过供应。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.reuters.com/business/retail-consumer/nvidia-ceo-jensen-huang-step-down-big-blow-ai-boom-2026-11-12/">Nvidia CEO Jensen Huang resigns in blow to AI boom he helped ...</a></li>
<li><a href="https://fxmacrowire.com/wire/top-democrats-call-to-rein-in-ai-buildout-after-midterms-sweep">Top Democrats call to rein in AI buildout after... | FXMacro Wire</a></li>

</ul>
</details>

**标签**: `#Nvidia`, `#AI trade`, `#ETFs`, `#semiconductors`, `#data-center policy`

---