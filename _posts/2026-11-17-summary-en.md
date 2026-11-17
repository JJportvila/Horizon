---
layout: default
title: "Horizon Summary: 2026-11-17 (EN)"
date: 2026-11-17
lang: en
---

> From 19 items, 4 important content pieces were selected

---

**Technology News**
1. [vLLM v0.34.0 enables extensible KV cache by default, removes Model Runner V1](#item-tech-news-1) ⭐️ 8.0/10
2. [Carnegie Mellon launches CS Learn with free full-semester courses on YouTube](#item-tech-news-2) ⭐️ 7.0/10
3. [Jiff 1.0 Brings a New Datetime Library to Rust](#item-tech-news-3) ⭐️ 7.0/10

**Financial News**
1. [Nvidia CEO Jensen Huang resigns; analysts recut AI trade](#item-finance-news-1) ⭐️ 8.0/10

---

## Technology News

<a id="item-tech-news-1"></a>
### [vLLM v0.34.0 enables extensible KV cache by default, removes Model Runner V1](https://github.com/vllm-project/vllm/releases/tag/v0.34.0) ⭐️ 8.0/10

vLLM v0.34.0 is out with 1,061 commits from 412 contributors, 10 new models, and an extensible KV cache enabled by default on CUDA and ROCm. The new cache sizing uses memory actually free after CUDA graph capture and warmup; vLLM reports MiniMax-M3 on H200 growing from 433k to 672k tokens, while per-token decode latency can rise 6–18% at concurrency 128 on some H200 models. The release also reports up to 1.95× decode for Step5 on 4×GB200 and 1.6× output throughput for GLM-5.3-Flash. Upgraders face breaking changes: Model Runner V1 is removed, the default block size is now 64 instead of 16, ROCm 7.2 artifacts are dropped in favor of ROCm 10.0, and \`huggingface\_hub &gt;= 2.0.0\` is required.

github · khluu · Nov 16, 23:22

**「Background」** vLLM is an open-source engine for serving large language models, and its KV cache holds attention state for tokens already processed so generation does not recompute them. Earlier releases used Model Runner V1 alongside V2 and estimated KV-cache capacity before warmup; v0.34.0 removes V1 and switches to sizing the cache from memory actually free after warmup.

**「Upgrade impact」** Operators must update launch configurations and dependencies before upgrading: remove \`VLLM\_USE\_V2\_MODEL\_RUNNER=0\`, pass \`--block-size 16\` to preserve the old block behavior, and move ROCm deployments to 10.0; the new default \`gpu\_memory\_utilization=1.0\` also changes memory sizing.

**Tags**: `#vLLM`, `#LLM inference`, `#KV cache`, `#GPU performance`, `#open source`

---

<a id="item-tech-news-2"></a>
### [Carnegie Mellon launches CS Learn with free full-semester courses on YouTube](https://www.cs.cmu.edu/learn/) ⭐️ 7.0/10

Carnegie Mellon has launched CS Learn, which publishes full semesters of lectures from current CMU computer science courses for free on YouTube. Phillip Compeau, who runs the project in CMU&\#x27;s Griffin School of Computer Science, said one course is premiering each day this week and that more courses will come in January. He said students built tools that automate much of the production work, allowing a small team to publish the material.

hackernews · pcompeau · Nov 16, 20:43 · [Discussion](https://news.ycombinator.com/item?id=50522980)

**「Background」** CS Learn is an open-courseware project that posts recorded lectures and course material publicly. In the discussion, Compeau acknowledged that MIT began similar open-courseware publishing about 25 years earlier, saying MIT &quot;got here 25 years ago.&quot;

**「Impact」** Learners can follow current CMU lectures for free on YouTube, but the initial release is lecture-centered. One commenter observed that courseware is listed as coming next and argued that projects and feedback are important for lectures not to &quot;fall flat.&quot;

**「Community discussion」** Commenters welcomed specific courses, including 15-259 Probability and Computing and Tianqi Chen&\#x27;s ML Systems, and one argued that learning fundamentals properly makes AI a power tool rather than a replacement. Another cautioned that lectures alone can fall flat without projects and feedback, and that advanced courses should be posted alongside introductory ones.

**Tags**: `#computer science education`, `#open courseware`, `#online learning`, `#Carnegie Mellon`, `#machine learning systems`

---

<a id="item-tech-news-3"></a>
### [Jiff 1.0 Brings a New Datetime Library to Rust](https://burntsushi.net/jiff/) ⭐️ 7.0/10

Jiff 1.0 has been released as a datetime library for Rust, published at burntsushi.net and discussed on Hacker News. The release gives Rust developers another option for date and time handling alongside established libraries such as chrono. The supplied material does not include API details, supported time scales, or a compatibility statement beyond the 1.0 version number.

hackernews · burntsushi · Nov 16, 16:53 · [Discussion](https://news.ycombinator.com/item?id=50519744)

**「Why another Rust datetime crate」** The discussion frames chrono as the incumbent Rust datetime crate: a former maintainer said its stable API was a major reason for adoption, while attempts to improve it met resistance. Jiff is positioned as an alternative focused on high-level primitives that are difficult to misuse and on reasonable performance.

**「Impact」** For teams evaluating Rust datetime crates, Jiff 1.0 is a new alternative to assess; the supplied evidence does not establish a migration path or compatibility with chrono, and commenters treat wider adoption as a hope rather than a demonstrated shift.

**「Community Discussion」** A commenter who says they maintained chrono for about half a decade argued that users valued chrono’s stable API and resisted incremental improvements, and said burnout led them to stop maintaining it while expressing gratitude to burntsushi for Jiff. Other commenters praised Jiff’s willingness to state that it is not the right tool for every use case and hoped the wider Rust ecosystem would adopt it over chrono.

<details><summary>References</summary>
<ul>
<li><a href="https://docs.rs/jiff/latest/jiff/">jiff - Rust - Docs.rs</a></li>

</ul>
</details>

**Tags**: `#Rust`, `#datetime`, `#libraries`, `#open-source`, `#time-scales`

---

## Financial News

<a id="item-finance-news-1"></a>
### [Nvidia CEO Jensen Huang resigns; analysts recut AI trade](https://www.cnbc.com/2026/11/14/nvidia-ai-trade-data-centers-congress.html) ⭐️ 8.0/10

Nvidia chief executive Jensen Huang has resigned, and Yorkville Ives cut its price target on the chipmaker to $225 from $300 while keeping a buy rating, with the stock closing the week at $162.85. Speaking on CNBC&\#x27;s &quot;ETF Edge,&quot; investing experts said Big Tech and other chipmakers such as AMD could pick up demand if investors lose trust in Nvidia.

rss · CNBC Finance · Nov 16, 12:13

**「Background」** Nvidia announced on Nov. 12 that founder Jensen Huang had resigned as CEO, naming CFO Colette Kress as interim CEO, while Democratic gains in the Nov. 3 midterms have prompted lawmakers to call for tougher limits on AI data centers.

**「Impact」** Yorkville Ives&\#x27; Dan Ives estimates that Democratic control of Congress, won in the Nov. 3 elections, could mean 10% of planned data centers are not built at the low end, or 15%–20% at the high end — a possible constraint for data-center developers and the cloud companies that depend on their computing capacity.

<details><summary>References</summary>
<ul>
<li><a href="https://investor.nvidia.com/news/press-release-details/2026/NVIDIA-Announces-CEO-Transition/">NVIDIA Corporation - NVIDIA Announces CEO Transition</a></li>
<li><a href="https://fxmacrowire.com/wire/top-democrats-call-to-rein-in-ai-buildout-after-midterms-sweep">Top Democrats call to rein in AI buildout after... | FXMacro Wire</a></li>

</ul>
</details>

**Tags**: `#Nvidia`, `#AI trade`, `#ETFs`, `#semiconductors`, `#data-center policy`

---