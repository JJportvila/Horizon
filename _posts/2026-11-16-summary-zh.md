---
layout: default
title: "Horizon Summary: 2026-11-16 (ZH)"
date: 2026-11-16
lang: zh
---

> 从 15 条内容中筛选出 8 条重要资讯。

---

**科技新闻**
1. [uBlock Origin 元素选择器被指存在通用 XSS](#item-tech-news-1) ⭐️ 8.0/10
2. [旧 Bitly 链接被劫持，第三方短链风险受关注](#item-tech-news-2) ⭐️ 7.0/10
3. [Qwen4-Max 发布：四档推理强度与成本争议](#item-tech-news-3) ⭐️ 7.0/10
4. [Steve Blank 谈 Nvidia 下一步：客户自研芯片与 CUDA 护城河](#item-tech-news-4) ⭐️ 7.0/10
5. [Protomaps：自托管地图瓦片更便宜、更易部署](#item-tech-news-5) ⭐️ 7.0/10
6. [Meta FAIR/NYU 200+ 模型实验：视觉预训练可选，专用参数不可省](#item-tech-news-6) ⭐️ 7.0/10

**财经新闻**
1. [中国 10 月零售、工业产出与投资均低于预期](#item-finance-news-1) ⭐️ 8.0/10
2. [卢特尼克因坎托与英伟达的关系面临质疑](#item-finance-news-2) ⭐️ 7.0/10

---

## 科技新闻

<a id="item-tech-news-1"></a>
### [uBlock Origin 元素选择器被指存在通用 XSS](https://iter.ca/post/ubo-uxss/) ⭐️ 8.0/10

一篇技术文章披露，uBlock Origin 的网站驱动元素选择器可被网页利用，造成通用跨站脚本（uXSS），影响使用该功能的扩展用户及其浏览器环境。文章把问题归因于扩展界面与网页 DOM 的交互；讨论中列出的修复版本为 uBlock Origin 1.75.4 和 uBO Lite 2026.1110.1816，但版本信息来自评论，尚未经过独立验证。现有材料没有说明是否已有在野利用、受影响浏览器版本范围，也没有提供厂商公告。

hackernews · zaik · 11月16日 02:04 · [社区讨论](https://news.ycombinator.com/item?id=50513160)

**「背景」** uBlock Origin 的“元素选择器”允许用户直接点选页面上的元素来生成过滤规则。为了定位并高亮目标元素，该界面被注入网页自身的 DOM，而不是停留在浏览器界面层；页面脚本因此可以读取甚至操纵这块由扩展创建的界面，这是此类 universal XSS 得以成立的前提。相关修复版本的信息来自读者在讨论中的核对，而非文章本身。

**「实际影响」** 对扩展开发者而言，这个案例表明，把规则创建等需要特权的界面放进网页 DOM 会扩大攻击面；对用户而言，应核对自己的 uBlock Origin 和 uBO Lite 是否达到讨论中提到的 1.75.4 和 2026.1110.1816，并关注官方修复说明。

**「社区讨论」** 评论者批评扩展为实现元素选择、密码管理器登录建议等界面而把内容注入网页 DOM，认为这可能向页面泄露账号信息或扩展标识；也有人追问 uBlock 是否暴露 UUID，从而形成可跟踪指纹，但该说法在讨论中只是疑问。另有评论质疑，为什么规则创建界面不能放在浏览器界面层，而要留在网页 DOM 中。

**标签**: `#security`, `#browser extensions`, `#uBlock Origin`, `#XSS`, `#open source`

---

<a id="item-tech-news-2"></a>
### [旧 Bitly 链接被劫持，第三方短链风险受关注](https://ransomnews.com/burger-king-tweet-bitly-link-hijack-2026/) ⭐️ 7.0/10

据 ransomnews 报道，旧 Bitly 短链接正被劫持；报道没有提供攻击方式、影响范围或 Bitly 的回应，因此这目前仍是媒体报告，而非经独立验证的大规模事件。对仍依赖 Bitly 链接的发布者、营销人员和普通用户来说，旧短链接可能不再指向最初目标，长期可靠性因此成为直接问题。

hackernews · hspeiser · 11月15日 22:11 · [社区讨论](https://news.ycombinator.com/item?id=50511395)

**「短链接别名的回收」** Bitly 是 URL 缩短服务，短链接本质上只是指向长地址的别名；当原账户失效或链接停用后，该别名可能被他人重新注册。此次事件中，汉堡王 2011 年 7 月 24 日推文里的短链接在 2026 年 11 月 15 日被他人重新注册并指向维基百科的纳粹集中营列表；Bitly 随后禁用了汉堡王、麦当劳等旧帖中遭劫持的链接。

**「实际影响」** 如果机构仍在网页、印刷品或旧帖子中使用 Bitly 短链接，用户可能被带到非预期页面；相关团队应核查这些链接的账户控制权和跳转目标，并把无法控制的链接替换为自有域名。

**「社区讨论」** 评论者 xp84 认为，外包短链接比自建更糟，因为账户停用、公司倒闭或数据丢失都会留下可能无法修复的死链；101008 则讲述了书中未注册的 Bit.ly 链接在出版日被其注册并改向的经历。silisili 对 Bitly 设有 Trust and Safety 团队感到意外，原以为它只是极少数人维护的副项目。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.malwarebytes.com/blog/news/2026/11/hijacked-bitly-links-turn-old-brand-posts-into-offensive-redirects">Hijacked Bitly links turn old brand posts into offensive ...</a></li>
<li><a href="https://ransomnews.com/burger-king-tweet-bitly-link-hijack-2026/">Old Bitly links hijacked in Burger King, McDonald’s and Trump ...</a></li>
<li><a href="https://techbytes.app/posts/old-bitly-links-are-being-hijacked/">Old Bitly Links Are Being Hijacked: Comments | Tech Bytes</a></li>

</ul>
</details>

**标签**: `#URL shorteners`, `#link hijacking`, `#web security`, `#link rot`, `#Bitly`

---

<a id="item-tech-news-3"></a>
### [Qwen4-Max 发布：四档推理强度与成本争议](https://qwen.ai/blog?id=qwen4-max) ⭐️ 7.0/10

Qwen4-Max 已发布，提供 none、low、high、xhigh 四档推理强度，用户可按任务调整推理开销。社区引用 Artificial Analysis 的数据称，该模型得分 43、平均成本 3.27 美元；作为对比，GPT-6.1 Sol（medium）得分 46、平均成本 0.36 美元。上述基准与价格来自评论转述，Qwen4-Max 的完整规格、定价单位和实际服务速度尚未得到独立确认。

hackernews · ilreb · 11月16日 02:14 · [社区讨论](https://news.ycombinator.com/item?id=50513215)

**「背景」** 据 LLM-Stats 的记录，阿里云 Qwen 团队先在 2026 年 11 月 11 日发布了 Qwen4-Max-Preview，本次正式版本与预览版相隔仅五天（tool-2-3）。在 Hacker News 的讨论中，用户 pu\_pe 提到上一代 Qwen3-Max 于 9 月发布，并认为这一旗舰系列并不以冲击前沿水平为目标，其优势更多体现在低一两档的 Flash、27B 等型号上。

**「接入成本与延迟需按 token 实测」** 对准备接入的开发者来说，Artificial Analysis 给出 Qwen4-Max 智能指数 43，但它在评测中生成 1.27 亿 token，远高于同类中位数 7860 万，因此按 token 计费的调用成本和延迟都会偏高。同一页面的单任务成本对比显示，GPT-6.1 Sol \(max\) 为 1.27 美元，Opus 5.5 \(max\) 为 10.01 美元，而 Qwen4-Max 是除前者外唯一更便宜的模型，所以选型时应针对自己的任务实测 token 用量，并根据 none 或 low 等 reasoning effort 档位设定预算与超时，而不能只看榜单分数。

**「社区讨论」** 有评论认为阿里的 Max 系列并不追求绝对前沿，真正有竞争力的是低一档的 Flash/27B 型号，这使 Qwen4-Max 更像“够用但非领先”的选择。另有开发者报告，上一代 Qwen3.8 仅约 30 tokens/s（Opus 接近 80），拖累了模型对战评分，并希望 Qwen4-Max 的服务更快。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://llm-stats.com/models/qwen4-max-preview">Qwen4-Max-Preview Benchmarks, Pricing &amp; Context Window</a></li>
<li><a href="https://artificialanalysis.ai/models/qwen4-max">Qwen 4 Max - Intelligence, Performance &amp; Price... | Artificial Analysis</a></li>
<li><a href="https://news.ycombinator.com/item?id=50513215">Qwen 4 - Max | Hacker News</a></li>

</ul>
</details>

**标签**: `#Qwen4-Max`, `#LLM release`, `#AI benchmarks`, `#reasoning models`, `#model cost/performance`

---

<a id="item-tech-news-4"></a>
### [Steve Blank 谈 Nvidia 下一步：客户自研芯片与 CUDA 护城河](https://steveblank.com/2026/11/15/whats-next-for-nvidia/) ⭐️ 7.0/10

Steve Blank 于 11 月 15 日发表《What&\#x27;s Next for Nvidia?》，这是一篇讨论 Nvidia 未来竞争位置的分析文章，而不是 Nvidia 的产品或财务公告。文章及相关讨论的核心论点是：随着问题空间趋于稳定，最大 GPU 买家可能借助 Broadcom 等公司开发自研芯片，并利用 agent 构建自己的抽象层和调试工具，从而降低 CUDA 的相关性。所给素材未提供出货量、性能、客户订单或时间表，因此这些判断应视为作者和评论者的观点，而非已证实的市场结果。

hackernews · zdw · 11月15日 23:55 · [社区讨论](https://news.ycombinator.com/item?id=50512235)

**「背景」** 这里的背景是，英伟达的大客户已同时布局自研 AI 芯片：谷歌的 TPU、亚马逊的 Trainium、微软的 Maia，以及 OpenAI 与博通合作的项目，构成了 GPU 之外的定制芯片路线；博通和 Marvell 被视为这一路线的主要合作方。行业预测还称，2026 年基于 ASIC 的 AI 服务器出货占比将升至 27.8%，定制 ASIC 出货量增长 44.6%，这正是讨论“客户变竞争者”的直接产业背景。布兰克的文章即在这一趋势下追问 CUDA 生态与英伟达的下一步。

**「影响」** 对 Nvidia 的客户和开发者而言，需要关注的具体兼容性问题是：自研芯片项目能否覆盖现有 CUDA 工具链之外的抽象层、调试和部署流程；评论者认为这正在变得更容易，但素材没有给出迁移规模或性能数据，不能据此认定 Nvidia 的订单或利润率已经受到影响。

**「社区讨论」** 评论者 01100011 认为最大威胁来自客户变成竞争者：大买家可与 Broadcom 等合作造芯片，并用 agent 建立抽象层和调试工具，使 CUDA 的重要性下降、利润率承压。另一条评论则质疑是否过度强调 CEO 的个人作用，认为数万人组织的命运不能简单系于一人；这两种看法都属评论者观点。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.tomshardware.com/tech-industry/semiconductors/custom-ai-asics-examined-from-broadcom-to-mtia">The custom AI ASIC state of play (May 2026) — Broadcom deals ...</a></li>
<li><a href="https://tech-insider.org/nvidia-customers-rivals-custom-silicon-race-2026/">Nvidia Customers Become Rivals: Custom Chip Race [2026]</a></li>
<li><a href="https://tech-insider.org/nvidia-custom-chip-rivals-openai-google-microsoft-amazon-2026/">Nvidia Faces 4 Custom Chip Rivals After OpenAI Move</a></li>

</ul>
</details>

**标签**: `#Nvidia`, `#AI hardware`, `#CUDA`, `#semiconductor strategy`, `#industry analysis`

---

<a id="item-tech-news-5"></a>
### [Protomaps：自托管地图瓦片更便宜、更易部署](https://bruceroettgers.eu/blog/protomaps/) ⭐️ 7.0/10

对需要自建地图服务的开发者来说，Protomaps/PMTiles 的自托管方案正被实践者描述为成本低、部署简单；一篇相关博文在 Hacker News 上引发了部署经验与替代方案的讨论。评论中，Cartes.app 称其因 MapTiler 账单达到每月 150 欧元而转向 Protomaps，托管成本几乎为零；也有团队在 Cloudflare R2 后自托管瓦片，以掌握隐私和访问控制。实践仍有兼容性问题：有评论者遇到企业反恶意软件代理剥离 Range 请求头，只能额外做代理端点来支持传统 WMTS 式请求；高缩放级别的高分辨率卫星影像也会迅速变大变贵。相关成本说法来自博文与评论者的部署经验，并非独立基准测试。

hackernews · bcye · 11月15日 19:26 · [社区讨论](https://news.ycombinator.com/item?id=50509837)

**「背景」** 地图应用通常依赖第三方瓦片服务，按请求或用量计费，流量增长后费用会快速累积。Protomaps/PMTiles 属于把瓦片作为可托管文件、避免运行专用瓦片服务器的思路，评论中提到的 OpenFreeMap 也采用仅用 nginx 提供服务的做法。这使得开发者可以在自有存储或 CDN 后面提供地图，而不必完全依赖商业 API。

**「影响」** 对打算采用 Protomaps/PMTiles 的开发者，上线前要验证客户端与中间代理是否支持 HTTP Range 请求；若不支持，按需读取会退化为整文件下载，需要增加兼容传统 WMTS 请求的代理端点。若业务依赖高缩放级别卫星影像，还应单独评估存储和带宽成本，不能套用矢量底图“几乎为零”的成本结论。

**「社区讨论」** 有评论者提出，自托管真正麻烦的不是托管费，而是内容控制：既然瓦片在自己手里，就会想调 Tilemaker 的 processing.lua 并花时间设计 MapLibre 样式。也有人推荐 OpenFreeMap 作为替代，称其公共实例不限制地图浏览量或请求数、无需注册和 API key；这是项目方介绍，不是独立测得的容量结论。

**标签**: `#self-hosting`, `#map tiles`, `#Protomaps`, `#PMTiles`, `#open source`

---

<a id="item-tech-news-6"></a>
### [Meta FAIR/NYU 200+ 模型实验：视觉预训练可选，专用参数不可省](https://www.reddit.com/r/MachineLearning/comments/1xx1k2o/meta_fair_nyu_unbundling_multimodal_vision/) ⭐️ 7.0/10

Meta FAIR 与 NYU 的作者在 Reddit 介绍了一项预印本研究：用相同数据和计入编码器预训练的总算力预算，从零训练 200 多个多模态 LLM，分别检验视觉编码器的独立预训练、视觉专用参数和编码器放置位置三个因素。作者报告，独立视觉预训练在匹配算力下至多只能追平随 LLM 从零训练的编码器；即便把 MetaCLIP 预训练延长 6.5 倍使 ImageNet 线性探测从 80.4% 升至 84.4%，VQA 也未提升。但视觉专用参数不可省：无编码器模型在 0.6B 到 6.4B 各规模都落后，约需 3 倍算力才能追上。编码器放在 LLM 之前也非必需：将零初始化视觉专用权重注入 LLM 前 8 层的“in-fusion”方案在 1.7B 到 6.4B 与编码器相当，并报告首 token 时间低约 13%；1.7B 时其 VQA 为 45.0，编码器为 44.4。

reddit · r/MachineLearning · /u/trungh98 · 11月15日 17:38

**「背景」** 多模态大模型通常采用“视觉编码器 + 语言模型”的结构：先用对比学习等目标单独预训练一个视觉编码器（如 CLIP、MetaCLIP），再由它把图像转成视觉 token 交给 LLM。因此，编码器预训练长期被视为默认的必要步骤，而编码器自带的独立参数和“置于 LLM 之前”的串联位置也常被捆绑在一起，难以单独评估。

**「影响」** 对从零训练多模态模型的团队，这项结果意味着算力可优先留给视觉专用参数和语言主干，而不必先做独立的编码器预训练；若采用 in-fusion，还可省去独立编码器并降低首 token 延迟。但作者结论基于 Qwen3-1.7B/4B、0.4B 视觉容量、448 像素输入和特定 VQA/语言基准，迁移到其他数据、分辨率或架构前仍需复现。

**标签**: `#multimodal LLMs`, `#vision encoders`, `#pretraining`, `#model scaling`, `#empirical study`

---

## 财经新闻

<a id="item-finance-news-1"></a>
### [中国 10 月零售、工业产出与投资均低于预期](https://www.cnbc.com/2026/11/16/china-retail-sales-october-industrial-output-investment.html) ⭐️ 8.0/10

中国 10 月社会消费品零售总额同比增长 0.4%，低于分析师预期的 0.8%，并较 9 月的 1.1%放缓；规模以上工业增加值同比增长 4.8%，也低于 5.3%的预期。前 10 个月固定资产投资同比下降 8.1%，降幅大于分析师预期的 7%。

rss · CNBC Finance · 11月16日 03:53

**「背景」** 零售疲软与持续五年的房地产市场低迷侵蚀家庭财富有关，而强劲出口在一定程度上支撑了增长。

**「影响」** 分析人士警告，增长日益依赖外部需求使中国出口企业更易受外部冲击影响，包括欧盟可能加码贸易限制和全球人工智能资本开支回调。

**标签**: `#China economy`, `#macroeconomic data`, `#retail sales`, `#industrial output`, `#fixed-asset investment`

---

<a id="item-finance-news-2"></a>
### [卢特尼克因坎托与英伟达的关系面临质疑](https://www.cnbc.com/2026/11/13/howard-lutnick-nvidia-jensen-huang-china-cantor-fitzgerald.html) ⭐️ 7.0/10

CNBC 报道，美国商务部长霍华德·卢特尼克因其曾执掌、现由其子经营的坎托·菲茨杰拉德与英伟达的关系面临质疑。据 CNBC 对证券文件的分析，坎托报告的英伟达持股在 2025 年 9 月至 2026 年 3 月间减少 49%，从约 350 万股降至 178 万股；报道同时称，没有证据表明卢特尼克泄露非公开信息，也没有证据表明持股变动与情报警告有关。

rss · CNBC Finance · 11月16日 12:14

**「背景」** 黄仁勋因与一名被美方怀疑为中国从事间谍活动的新加坡科技高管的关系接受调查，近日辞去英伟达 CEO 职务，由首席财务官 Colette Kress 暂代；卢特尼克此前执掌 Cantor Fitzgerald，转任商务部长后，商务部正是负责执行芯片出口管制和“实体清单”（限制与特定企业交易的名录）的机构。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://abcnews.com/Business/nvidia-ceo-jensen-huang-resigns-amid-alleged-affair/story?id=138076256">Nvidia CEO Jensen Huang resigns amid alleged affair with ...</a></li>
<li><a href="https://www.usatoday.com/story/tech/2026/11/12/jensen-huang-nvidia-ceo-resigns-affair-investigation/92734431007/">Jensen Huang out as Nvidia CEO amid Chinese spy investigation</a></li>

</ul>
</details>

**标签**: `#Nvidia`, `#US export controls`, `#Lutnick ethics`, `#Cantor Fitzgerald`, `#US-China tech`

---