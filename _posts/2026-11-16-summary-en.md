---
layout: default
title: "Horizon Summary: 2026-11-16 (EN)"
date: 2026-11-16
lang: en
---

> From 15 items, 8 important content pieces were selected

---

**Technology News**
1. [Universal XSS in uBlock Origin&\#x27;s website-driven element picker](#item-tech-news-1) ⭐️ 8.0/10
2. [Old Bitly Links Reportedly Hijacked](#item-tech-news-2) ⭐️ 7.0/10
3. [Qwen4-Max Released With Four Reasoning-Effort Settings](#item-tech-news-3) ⭐️ 7.0/10
4. [Steve Blank&\#x27;s Nvidia Analysis Sparks Debate on CUDA and Custom Chips](#item-tech-news-4) ⭐️ 7.0/10
5. [Protomaps: Self-Hosting Map Tiles Has Become Cheap and Easy](#item-tech-news-5) ⭐️ 7.0/10
6. [Meta FAIR/NYU: vision encoder pretraining optional, vision-only parameters required in MLLMs](#item-tech-news-6) ⭐️ 7.0/10

**Financial News**
1. [China&\#x27;s October retail sales, industrial output and investment miss forecasts](#item-finance-news-1) ⭐️ 8.0/10
2. [Lutnick faces questions over Cantor Fitzgerald&\#x27;s Nvidia ties](#item-finance-news-2) ⭐️ 7.0/10

---

## Technology News

<a id="item-tech-news-1"></a>
### [Universal XSS in uBlock Origin&\#x27;s website-driven element picker](https://iter.ca/post/ubo-uxss/) ⭐️ 8.0/10

A technical write-up describes a universal XSS in uBlock Origin that arises from the extension&\#x27;s website-driven element picker. The supplied item does not include the original source text, so the precise trigger and scope are not independently detailed here. A commenter reports that users should run uBlock Origin 1.75.4 or uBO Lite 2026.1110.1816 or later, but those version numbers come from the discussion rather than a confirmed advisory in the supplied material.

hackernews · zaik · Nov 16, 02:04 · [Discussion](https://news.ycombinator.com/item?id=50513160)

**「Context: The element picker and page DOM」** uBlock Origin&\#x27;s element picker is a feature that lets a user point at a page element to build a blocking rule, and to interact with the page&\#x27;s own elements the extension renders its picker overlay inside the website&\#x27;s DOM rather than in browser chrome. That design is what makes a website able to reach the extension&\#x27;s UI, and commenters noted the same trade-off affects other extensions, such as password managers that inject suggested-login UI into the page. Discussion of the write-up also pointed to fixed builds at uBlock Origin 1.75.4 and uBO Lite 2026.1110.1816.

**「Impact」** For users, the immediate action is version checking: a commenter lists uBlock Origin 1.75.4 and uBO Lite 2026.1110.1816 as the fixed releases. The discussion also highlights a design consequence for extension developers: UI injected into the page DOM can be observed by page scripts, so isolation choices matter for element pickers and password-manager suggestions.

**「Community Discussion」** Commenters debated why extension UI must be injected into the page&\#x27;s DOM at all. ByteOfWood noted that password-manager suggestions can leak account information to page scripts, jonhohle asked whether a leaked UUID gives sites a tracking fingerprint, and akersten suggested moving the element picker into browser chrome.

**Tags**: `#security`, `#browser extensions`, `#uBlock Origin`, `#XSS`, `#open source`

---

<a id="item-tech-news-2"></a>
### [Old Bitly Links Reportedly Hijacked](https://ransomnews.com/burger-king-tweet-bitly-link-hijack-2026/) ⭐️ 7.0/10

The item reports that old Bitly short links are being hijacked, meaning previously published links may redirect to destinations their original creators did not intend. It provides no technical detail on how the hijacking works, which links are affected, or how Bitly has responded, so the scope remains unconfirmed. The concern applies to anyone who has treated Bitly links as durable references in posts, documents, or other long-lived material.

hackernews · hspeiser · Nov 15, 22:11 · [Discussion](https://news.ycombinator.com/item?id=50511395)

**「How short links get reclaimed」** Bitly is a URL-shortening service that maps a short code to a longer web address. Because the short link is only an alias, if a code becomes dormant or expired and is later claimed by someone else, the same URL can resolve to an entirely different destination. That alias-reuse mechanism is what allows old Bitly links embedded in archived posts to be redirected to unrelated content.

**「Impact」** For affected users, the immediate risk is destination integrity: a short link can still resolve while sending visitors somewhere unintended. Organizations that rely on Bitly links for permanent references should verify or replace business-critical links rather than assume an old URL still points to the original source.

**「Community Discussion」** Commenters argued that outsourced URL shorteners accumulate risk over time because accounts can be deactivated or the company can fail, leaving links broken or redirectable. One commenter reported finding an unregistered Bitly link printed in a book and redirecting it to a site about the book, illustrating how an unclaimed short URL can be taken over.

<details><summary>References</summary>
<ul>
<li><a href="https://www.malwarebytes.com/blog/news/2026/11/hijacked-bitly-links-turn-old-brand-posts-into-offensive-redirects">Hijacked Bitly links turn old brand posts into offensive ...</a></li>
<li><a href="https://ransomnews.com/burger-king-tweet-bitly-link-hijack-2026/">Old Bitly links hijacked in Burger King, McDonald’s and Trump ...</a></li>
<li><a href="https://techbytes.app/posts/old-bitly-links-are-being-hijacked/">Old Bitly Links Are Being Hijacked: Comments | Tech Bytes</a></li>

</ul>
</details>

**Tags**: `#URL shorteners`, `#link hijacking`, `#web security`, `#link rot`, `#Bitly`

---

<a id="item-tech-news-3"></a>
### [Qwen4-Max Released With Four Reasoning-Effort Settings](https://qwen.ai/blog?id=qwen4-max) ⭐️ 7.0/10

Qwen4-Max is a new Qwen LLM release for model users, and community reports say it exposes four reasoning-effort settings: none, low, high, and xhigh. A commenter cites an Artificial Analysis score of 43 at an average cost of $3.27, compared with 46 at $0.36 for GPT-6.1 Sol at medium effort; these are third-party discussion figures and were not independently verified here. The linked Qwen blog was not included in the supplied material, so official availability, context-window, and pricing details remain unconfirmed.

hackernews · ilreb · Nov 16, 02:14 · [Discussion](https://news.ycombinator.com/item?id=50513215)

**「What precedes Qwen4-Max」** Qwen4-Max follows a preview release on November 11, 2026, before the production \`qwen4-max\` model became available. Per published model specifications, it is a 2.4-trillion-parameter sparse mixture-of-experts model with 71 billion active parameters per token and a 1M-token context window \(about 991K input tokens, or 983K in thinking mode\), listed at $1.50 per million input tokens and $4.50 per million output tokens in Singapore. The model also exposes selectable reasoning-effort levels, which commenters have been testing from a &quot;none&quot; setting upward.

**「Cost and verbosity for adopters」** Teams weighing Qwen4-Max for cost-sensitive workloads should budget for its output volume as well as its sticker price: on its Artificial Analysis Intelligence Index run the model generated 127M tokens against a median of 78.6M, and its score of 43 sits below GPT-6.1 Sol&\#x27;s 46 while costing more on average. Pricing data cited from the same comparison page lists GPT-6.1 Sol \(max\) at $1.27 per task and Opus 5.5 \(max\) at $10.01, with GPT-6.1 Sol the only model shown as cheaper than Qwen4-Max, so per-task cost rather than headline benchmark position is the practical selection criterion.

**「Community discussion」** Commenters debate whether Qwen4-Max is meant to compete at the frontier: one argues that Alibaba is not targeting that tier with this class and that its Flash and smaller models are where it is strongest relative to peers. Another reports that serving speed, not just quality, hurt Qwen 3.8 in an agent-arena setup—roughly 30 tokens per second versus about 80 for Opus—and hopes Qwen4-Max serves faster.

<details><summary>References</summary>
<ul>
<li><a href="https://llmlearner.com/models/qwen4-max">Qwen4-Max: Benchmarks, Pricing &amp; Specs | LLMLearner</a></li>
<li><a href="https://kingy.ai/blog/qwen-4-release-date-status/">Qwen4-Max benchmarks, pricing and specs: How it compares</a></li>
<li><a href="https://llm-stats.com/models/qwen4-max-preview">Qwen4-Max-Preview Benchmarks, Pricing &amp; Context Window</a></li>
<li><a href="https://artificialanalysis.ai/models/qwen4-max">Qwen 4 Max - Intelligence, Performance &amp; Price... | Artificial Analysis</a></li>
<li><a href="https://news.ycombinator.com/item?id=50513215">Qwen 4 - Max | Hacker News</a></li>

</ul>
</details>

**Tags**: `#Qwen4-Max`, `#LLM release`, `#AI benchmarks`, `#reasoning models`, `#model cost/performance`

---

<a id="item-tech-news-4"></a>
### [Steve Blank&\#x27;s Nvidia Analysis Sparks Debate on CUDA and Custom Chips](https://steveblank.com/2026/11/15/whats-next-for-nvidia/) ⭐️ 7.0/10

Steve Blank&\#x27;s Nov. 15 post, “What&\#x27;s Next for Nvidia?”, is a strategic analysis rather than a product, roadmap, or earnings announcement, and the supplied material does not include its full text. The Hacker News discussion it generated focuses on whether Nvidia&\#x27;s largest GPU buyers will become competitors by designing custom chips with partners such as Broadcom, whether CUDA&\#x27;s software advantage is eroding as customers build their own abstraction and debugging tools, and how much one CEO can shape a company of Nvidia&\#x27;s scale. No new Nvidia hardware, compatibility change, or measured result is reported.

hackernews · zdw · Nov 15, 23:55 · [Discussion](https://news.ycombinator.com/item?id=50512235)

**「The custom-silicon backdrop」** The debate over Nvidia&\#x27;s moat rests on a shift already under way: its largest customers are building their own AI accelerators rather than buying only GPUs. Broadcom and Marvell have emerged as the primary custom AI chip partners, with Broadcom linked to Alphabet, Meta, Anthropic and OpenAI, and Marvell linked to Microsoft and Amazon, according to a report cited by Tech-Insider. Tom&\#x27;s Hardware, citing industry forecasts, reported that ASIC-based AI server shipments were projected to reach 27.8% of the market in 2026 and that custom ASIC shipments would grow 44.6%.

**「Community Discussion」** Commenters debate the durability of Nvidia&\#x27;s position: one argues that a stabilizing problem space and agent-assisted tooling let large buyers work with Broadcom on custom chips and build their own abstraction and debug layers, making CUDA “less relevant” at a rate “about to go parabolic.” Another holds up Steve Jobs&\#x27;s willingness to let Apple cannibalize its own products as a model, while a third questions whether analysts overemphasize a CEO&\#x27;s influence on an organization with tens of thousands of employees.

<details><summary>References</summary>
<ul>
<li><a href="https://www.tomshardware.com/tech-industry/semiconductors/custom-ai-asics-examined-from-broadcom-to-mtia">The custom AI ASIC state of play (May 2026) — Broadcom deals ...</a></li>
<li><a href="https://tech-insider.org/nvidia-customers-rivals-custom-silicon-race-2026/">Nvidia Customers Become Rivals: Custom Chip Race [2026]</a></li>

</ul>
</details>

**Tags**: `#Nvidia`, `#AI hardware`, `#CUDA`, `#semiconductor strategy`, `#industry analysis`

---

<a id="item-tech-news-5"></a>
### [Protomaps: Self-Hosting Map Tiles Has Become Cheap and Easy](https://bruceroettgers.eu/blog/protomaps/) ⭐️ 7.0/10

A blog post published on November 15 argues that self-hosting map tiles with Protomaps and the PMTiles format has become cheap and easy enough for developers and site operators who want to own their map infrastructure. It is a practical account rather than a product release, and the supplied material includes no version number or independently measured cost comparison. One developer in the discussion reports moving from Maptiler to Protomaps after bills reached €150 per month, with hosting costs now described as almost nothing.

hackernews · bcye · Nov 15, 19:26 · [Discussion](https://news.ycombinator.com/item?id=50509837)

**「Background」** PMTiles packages map tiles into a single archive that can be served from static storage or a CDN, letting clients request byte ranges instead of querying a dedicated tile server. That is the mechanism behind the low-cost pattern, and it is also why Range-request support matters.

**「Impact」** For teams adopting this, the main operational check is whether intermediaries preserve HTTP Range requests; one commenter had to add a proxy endpoint for a corporate anti-malware proxy that stripped the header and requested entire files. The cheaper-static-hosting model therefore depends on testing CDN, corporate-proxy, and client behavior, not just on storing the PMTiles archive.

**「Community Discussion」** Commenters add adjacent options: OpenFreeMap offers a free public instance with no API keys, and another developer runs a similar PMTiles setup behind Cloudflare R2 for privacy and access control. A separate caveat concerns scope: basemaps are compact, but high-resolution satellite imagery becomes large and expensive quickly at higher zoom levels.

**Tags**: `#self-hosting`, `#map tiles`, `#Protomaps`, `#PMTiles`, `#open source`

---

<a id="item-tech-news-6"></a>
### [Meta FAIR/NYU: vision encoder pretraining optional, vision-only parameters required in MLLMs](https://www.reddit.com/r/MachineLearning/comments/1xx1k2o/meta_fair_nyu_unbundling_multimodal_vision/) ⭐️ 7.0/10

A Meta FAIR + NYU study reports that pretraining a vision encoder is optional for multimodal LLMs, while vision-only parameters are not. The authors trained 200+ models from scratch on identical data, counting encoder pretraining against the same lifetime compute budget, using Qwen3-1.7B and 4B backbones with 0.4B vision parameters and a scaling ladder from 0.6B to 6.4B, evaluated on 16 Cambrian VQA benchmarks at 448 px and 12 language benchmarks. Encoders pretrained with contrastive, self-supervised, or captioning objectives at best tied a from-scratch encoder at matched compute, and pretraining MetaCLIP 6.5x longer lifted ImageNet linear-probe accuracy from 80.4% to 84.4% without improving VQA; encoder-free models trailed at every size from 0.6B to 6.4B and needed roughly 3x the compute to catch up. The paper also reports that &quot;in-fusion&quot; placement—adding zero-initialized vision-only attention and FFN weights to the LLM&\#x27;s first 8 layers—matched a separate encoder from 1.7B to 6.4B with about 13% lower time to first token. These are the authors&\#x27; own claims from a preprint \(arXiv 2611.17334\), summarized in a self-disclosed author post rather than independently verified.

reddit · r/MachineLearning · /u/trungh98 · Nov 15, 17:38

**「Background」** Multimodal LLMs typically combine a vision encoder with an LLM, with the encoder separately pretrained and its parameters reserved for visual tokens. Recent published models have diverged on this recipe—some remove the encoder, some train it from scratch, and some restore it—but comparisons across them cannot isolate the encoder&\#x27;s effects because data, compute, and pretraining budgets differ.

**「Impact」** For teams designing multimodal LLMs, the results argue against spending the compute budget on separate encoder pretraining and for allocating dedicated vision-only parameters—either as a standalone encoder or as vision-only branches in early LLM layers, since at 1.7B the layer 1–8 branches scored 45.0 VQA versus 42.3 when text tokens shared those weights and 35.1 when placed in the last 8 layers. Dropping vision-only parameters entirely is the costlier option: the authors report encoder-free variants need roughly 3x the compute to match, a constraint that matters most at the smaller 0.6B–1.7B sizes tested.

**Tags**: `#multimodal LLMs`, `#vision encoders`, `#pretraining`, `#model scaling`, `#empirical study`

---

## Financial News

<a id="item-finance-news-1"></a>
### [China&\#x27;s October retail sales, industrial output and investment miss forecasts](https://www.cnbc.com/2026/11/16/china-retail-sales-october-industrial-output-investment.html) ⭐️ 8.0/10

China&\#x27;s October retail sales, industrial output and fixed-asset investment all missed economists&\#x27; estimates, with retail sales up 0.4% from a year earlier versus a 0.8% forecast and industrial output up 4.8% versus 5.3%. January-October fixed-asset investment fell 8.1%, worse than the 7% decline expected.

rss · CNBC Finance · Nov 16, 03:53

**「Background」** The weakness reflects a property-market downturn now in its fifth year, which has eroded household wealth, and analysts say it has left growth more reliant on exports.

**「Impact」** China&\#x27;s exporters, especially in AI-related technology and equipment, are exposed to a pullback in global AI capital spending, which has driven much of the recent export strength, analysts warn.

**Tags**: `#China economy`, `#macroeconomic data`, `#retail sales`, `#industrial output`, `#fixed-asset investment`

---

<a id="item-finance-news-2"></a>
### [Lutnick faces questions over Cantor Fitzgerald&\#x27;s Nvidia ties](https://www.cnbc.com/2026/11/13/howard-lutnick-nvidia-jensen-huang-china-cantor-fitzgerald.html) ⭐️ 7.0/10

Commerce Secretary Howard Lutnick is facing questions over his former firm Cantor Fitzgerald’s Nvidia ties after Nvidia CEO Jensen Huang resigned Thursday, with CNBC reporting that Cantor cut its disclosed Nvidia shareholding by 49% between September 2025 and March 2026, from 3.5 million to 1.78 million shares, while continuing to finance Nvidia business partners.

rss · CNBC Finance · Nov 16, 12:14

**「Background」** Cantor Fitzgerald is the Wall Street firm Howard Lutnick formerly ran; he became commerce secretary in February 2025, and his sons Brandon and Kyle now lead it. Commerce oversees the export-control entity list central to the Nvidia chip-smuggling scrutiny.

**Tags**: `#Nvidia`, `#US export controls`, `#Lutnick ethics`, `#Cantor Fitzgerald`, `#US-China tech`

---