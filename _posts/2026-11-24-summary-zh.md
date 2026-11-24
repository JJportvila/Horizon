---
layout: default
title: "Horizon Summary: 2026-11-24 (ZH)"
date: 2026-11-24
lang: zh
---

> 从 14 条内容中筛选出 6 条重要资讯。

---

**科技新闻**
1. [Ladybird 首个 Alpha 版开放下载](#item-tech-news-1) ⭐️ 8.0/10
2. [英伟达董事会恢复黄仁勋 CEO 职务](#item-tech-news-2) ⭐️ 7.0/10
3. [Arm 要求第三方文档站 12 月 4 日下线](#item-tech-news-3) ⭐️ 7.0/10
4. [Z.ai 发布 GLM-5.4：首个循环 Transformer 编码模型](#item-tech-news-4) ⭐️ 7.0/10

**科技博客**
1. [vLLM 插件实现 ERNIE 5.5 Flash 首发支持](#item-tech-blog-1) ⭐️ 6.0/10

**财经新闻**
1. [纽约联储威廉姆斯：通胀回 2%仍“有工作要做”，暗示加息可逐步推进](#item-finance-news-1) ⭐️ 7.0/10

---

## 科技新闻

<a id="item-tech-news-1"></a>
### [Ladybird 首个 Alpha 版开放下载](https://ladybird.org/posts/alpha/) ⭐️ 8.0/10

Ladybird 发布了首个 Alpha 版，macOS 和 Linux 用户现在可以直接下载安装，无需自行编译。这个从零实现的浏览器只沿用 HarfBuzz、Skia、ffmpeg 和 SQLite 等少数外部组件；试用中 WebAssembly 版 ffmpeg 与 Pyodide 能正常运行，但依赖 service worker 的 Datasette Lite 因缺少 \`navigator.serviceWorker.startMessages\` 而失败。官方强调这仍是 alpha：部分网站会打不开，浏览器有时会崩溃，并邀请用户报告坏站和安全问题。

hackernews · janvdberg · 11月23日 16:13 · [社区讨论](https://news.ycombinator.com/item?id=50614249)

**「背景」** Ladybird 的浏览器引擎大部分从零实现，文本整形、2D 图形、视频和 SQLite 等少数部分则采用 HarfBuzz、Skia、ffmpeg 和 SQLite 等外部组件，另有一些代码继承自其前身项目 SerenityOS。2026 年 2 月，项目开始借助 AI 编程代理把 LibJS 的部分实现从 C++ 移植到 Rust；到 10 月，它又通过针对 web-platform-tests 的集中修补把通过的子测试数推到约 218 万，在该月统计中超过 Safari，这些工作为本次 alpha 打下了基础。

**「影响」** 官方对 alpha 的定位意味着它现阶段不适合作为唯一的日常浏览器：遇到网站损坏可从浏览器内报告，崩溃后可先查看报告再决定是否发送。对 Web 开发者而言，依赖 service worker 等尚未实现 API 的站点需要先做兼容性测试，已有相关失败案例。

**「社区讨论」** 早期试用者的反馈总体正面：多人称常见网站乃至 ProxMox/NoVNC 等复杂页面能正确加载，NoVNC 甚至比 Firefox 更流畅，但也有人指出页面滚动略显卡顿。另有评论者希望 Ladybird 后续认真处理浏览器指纹识别问题，提供更严格的权限控制，而不是只追求兼容性。

**标签**: `#browser engines`, `#open source`, `#Ladybird`, `#alpha release`, `#web standards`

---

<a id="item-tech-news-2"></a>
### [英伟达董事会恢复黄仁勋 CEO 职务](https://www.cnbc.com/2026/11/23/nvidia-jensen-huang-ceo.html) ⭐️ 7.0/10

据 CNBC 报道，英伟达董事会决定恢复黄仁勋（Jensen Huang）的 CEO 职务。相关声明称，董事会在作出决定前听取了美国联邦政府高级层级的意见，并据此认为黄仁勋回归不构成国家安全风险。现阶段提供的材料只有标题、声明片段和评论，未包含完整报道正文，因此黄仁勋此前离任的具体原因、恢复职务的生效时间以及董事会投票细节仍无法独立核实。

hackernews · jaz · 11月23日 14:00 · [社区讨论](https://news.ycombinator.com/item?id=50611576)

**「事件背景」** 据半岛电视台报道，黄仁勋在本次复职前约一周多辞职，辞职背景涉及婚外情，其中一段关系涉及一名被指为中国间谍的女性。Nvidia 于 11 月 23 日发布的官方新闻稿称，复职立即生效，黄仁勋恢复总裁、CEO 和董事职务。

**「治理与合规影响」** 按报道所引的董事会声明，Nvidia 在决定让黄仁勋复职时听取了美国政府高层意见；其董事会此前还设立了监督国家安全政策和美国出口管制合规的委员会。对依赖 Nvidia 芯片的客户和投资者来说，后续对华销售与出口许可将同时受董事会合规监督和政府输入影响，许可条件和合规限制的变化是比 CEO 人事更直接的风险点。

**「社区讨论」** 评论区最集中的争论是政府介入是否让董事会免于责任：有评论引用特拉华州 Caremark 判例和司法部不起诉的说法，认为董事的个人责任可能被消除；也有人质疑外界在缺乏证据的情况下预设英伟达有罪，并把此事与此前 OpenAI 董事会风波类比，认为名义治理结构不等于实际治理结构。另有评论批评美国在要求 ASML 和日本芯片企业配合对华制裁的同时，却对英伟达网开一面。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://investor.nvidia.com/news/press-release-details/2026/NVIDIA-Board-Reinstates-Jensen-Huang-as-President-CEO-and-Board-Director/default.aspx">NVIDIA Corporation - NVIDIA Board Reinstates Jensen Huang as...</a></li>
<li><a href="https://www.aljazeera.com/economy/2026/11/23/nvidia-board-reinstates-jensen-huang-as-ceo">Nvidia board reinstates Jensen Huang as CEO | Al Jazeera</a></li>
<li><a href="https://www.cbsnews.com/news/nvidia-export-control-committee-china-chips/">Nvidia&#x27;s board forms export oversight panel after scrutiny ...</a></li>

</ul>
</details>

**标签**: `#Nvidia`, `#corporate governance`, `#US export controls`, `#semiconductor policy`, `#national security`

---

<a id="item-tech-news-3"></a>
### [Arm 要求第三方文档站 12 月 4 日下线](https://arm.jonpalmisc.com/) ⭐️ 7.0/10

Arm 已要求第三方 Arm 架构文档站点 arm.jonpalmisc.com 于 2026 年 12 月 4 日停止运营，站点标题也宣布届时下线。维护者 jonpalmisc 表示，Arm 给出的理由是托管其文档使用了 Arm 的商标和知识产权，并称在保持站点有用性的同时很难规避这一点；他还在考虑他人提出的镜像、法律咨询以及在不含 Arm IP 的前提下公开源码等方案。上述为 Arm 向维护者提出的要求，并非法院裁决或已完成的强制执行。

hackernews · tech234a · 11月23日 19:17 · [社区讨论](https://news.ycombinator.com/item?id=50617499)

**「背景」** 被要求下线的 Jon&\#x27;s Arm Reference 是一个非官方的在线参考站，用于查阅 AArch64 指令和系统寄存器，内容覆盖 Armv8-A 与 Armv9-A 架构。

**「影响」** 依赖该站浏览 Arm 架构文档的开发者需在 12 月 4 日前改用官方文档或其他镜像；维护者正在评估镜像和去除 Arm IP 后公开源码等方案，因此替代站点的可用性尚不确定。

**「社区讨论」** 有评论者称，Arm 的机器可读架构规范（MRAS）若干版本采用 BSD 风格许可，因此质疑该侵权主张的适用范围；另一人则把该站与斯坦福托管的类似 arm64 文档页面相比较，推测两者可能都是用转换工具从官方文档生成。也有评论认为，针对此类项目采取法律行动只会给为 Arm 生态提供价值的开发者增加负担。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://news.lavx.hu/article/jon-s-arm-reference-to-shut-down-dec-4-after-arm-legal-request">Jon&#x27;s Arm Reference to Shut Down Dec. 4 After Arm Legal Request</a></li>
<li><a href="https://zeli.app/story/50617499">Arm&#x27;s Lawyers Force Shutdown of Popular · Hacker News | Zeli</a></li>

</ul>
</details>

**标签**: `#Arm`, `#documentation takedown`, `#trademark/IP`, `#hardware documentation`, `#developer access`

---

<a id="item-tech-news-4"></a>
### [Z.ai 发布 GLM-5.4：首个循环 Transformer 编码模型](https://simonwillison.net/2026/Nov/23/glm-54/) ⭐️ 7.0/10

Z.ai 发布 GLM-5.4，这是该公司首个采用循环 Transformer（looped transformer）架构的模型，定位为通用编码模型。按 Z.ai 的说法，该架构让一组共享权重的层在一次前向传播中多次迭代、不断细化上一轮的隐藏状态，从而在不增加参数量的情况下加深网络。GLM-5.4 目前尚未开放权重，也无法通过常规 API 访问，只能通过 Z.ai 的 Coding Plan 订阅使用；Coding Plan 与常规 API 共用位于 https://api.z.ai/api/v1 的 OpenAI 兼容 Responses API，订阅密钥可直接调用新模型。Simon Willison 用它做了“骑自行车鹈鹕”测试，认为效果一般，并称其与未做同项测试的 GLM-5.3 水平相近；他为此发布了 llm-glm 插件，但表示现有的 llm-zai 插件一旦支持新模型，他就会停用自己的版本。

rss · Simon Willison · 11月23日 23:40

**「背景」** 在标准 Transformer 中，每一层在一次前向传播中只运行一次；循环 Transformer 则让一组共享权重的层重复运行多轮，用迭代计算换取更深的有效网络，而不增加参数规模。这一思路在一周内第二次出现：Thinking Machines Lab 于 11 月 20 日发布的 Inkling 2 Mini 同样把模型中间层对每个 token 运行三次，并称这能让模型以更少 token 完成智能体编码等依赖推理质量的任务。Willison 还对比了四代 GLM 的鹈鹕图，指出 5.1 和 5.2 的生成风格与 OpenAI、Anthropic 模型差异明显，而从 5.3 起风格明显转向接近主流模型。

**「影响」** 希望试用 GLM-5.4 的开发者目前必须先订阅 Coding Plan，而不能直接走常规 API；好在两者共用同一套 OpenAI 兼容接口，只要把 base URL 指向 https://api.z.ai/api/v1 并填入订阅密钥即可调用。在工具链方面，已有的 llm-zai 插件尚未适配新模型，用户需改用 Willison 临时发布的 llm-glm 插件，或等待前者更新。

**标签**: `#looped transformers`, `#GLM-5.4`, `#Z.ai`, `#AI models`, `#coding models`

---

## 科技博客

<a id="item-tech-blog-1"></a>
### [vLLM 插件实现 ERNIE 5.5 Flash 首发支持](https://vllm.ai/blog/2026-11-24-ernie-5-5-flash-preview) ⭐️ 6.0/10

rss · vLLM Blog · 11月24日 00:00

**「背景」** 百度 ERNIE 团队与 vLLM 合作，在 ERNIE 5.5 Flash Preview 发布当天提供支持。该模型是 280B 总参数、每 token 激活 14B 的稀疏 MoE，面向 1M token 上下文、思考式回答和长程 Agent 工具调用；难点在于让新架构直接运行在官方 vLLM 上，而不必维护分支或专用镜像。

**「方案」** 作者的核心做法是把 ERNIE 专属模型代码和内核优化封装为独立的 vLLM-ERNIE 插件，通过 vllm.general\_plugins 入口自动注册，与 PyPI 上的 vllm==0.32.0 同环境安装即可；插件只在 config.json 指定 ERNIE 架构时导入模型代码，避免影响其他模型。模型侧，43 层中 37 层用 HCA、6 层用 MLA-DSA，并引入 VHA、Multi-Router Latent MoE、mHC 和 MultiMax 等结构；团队为这些结构设计融合内核，把低秩混合、FP8 量化、路由 GEMM、分段激活等合并，作者称单内核比朴素实现快 1.55×–6.53×。FlashIndexer 用动态头路由和阈值预过滤加速稀疏索引，作者报告 1M 上下文下约 1.4× 加速；默认检查点将路由专家量化为 MXFP4（W4A8）、其余权重 FP8，KV 缓存 FP8。DSpark 三层 MoE 草稿模型每步最多提议 7 个 token，作者称在真实编程和 Agent 负载上平均接受长度超过 4.0。上述性能数字主要是团队自述，原文未给出完整基准方法，部署收益仍需结合实际负载验证。

**「启示」** 这项工作展示了用独立插件把新模型架构与 vLLM 核心解耦的可行路径：模型团队可更快交付专属内核和量化方案，同时继续复用 vLLM 的调度、并行与服务能力；其价值最终取决于这些加速在真实生产负载中的可复现性。

**标签**: `#vLLM`, `#ERNIE`, `#MoE inference`, `#kernel fusion`, `#speculative decoding`

---

## 财经新闻

<a id="item-finance-news-1"></a>
### [纽约联储威廉姆斯：通胀回 2%仍“有工作要做”，暗示加息可逐步推进](https://www.cnbc.com/2026/11/23/john-williams-fed-inflation-rate-hikes.html) ⭐️ 7.0/10

纽约联储主席威廉姆斯（John Williams）周一表示，美联储在把通胀拉回 2%目标方面“仍有工作要做”，并暗示后续政策行动可以随时间逐步展开。市场目前对 12 月 8-9 日议息会议加息 25 个基点、把目标区间从 3.75%-4%上调已完全定价。

rss · CNBC Finance · 11月23日 21:02

**「背景」** 威廉姆斯预计通胀将在 2027 年更接近 2%、并在随后一年达到目标；他把当前通胀压力归因于伊朗冲突、人工智能建设带来的商品需求以及关税，但称关税作为压力来源的影响“已基本消退”。

**「影响」** 若 12 月加息落地，以浮动利率计息的贷款和信用卡等借款成本将随之上行，直接加重相关家庭和企业的利息负担。

**标签**: `#Federal Reserve`, `#monetary policy`, `#interest rates`, `#inflation`, `#John Williams`

---