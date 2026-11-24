---
layout: default
title: "Horizon Summary: 2026-11-24 (EN)"
date: 2026-11-24
lang: en
---

> From 14 items, 6 important content pieces were selected

---

**Technology News**
1. [Ladybird releases first alpha for macOS and Linux](#item-tech-news-1) ⭐️ 8.0/10
2. [Nvidia Board Reinstates Jensen Huang as CEO, Citing U.S. Government Input](#item-tech-news-2) ⭐️ 7.0/10
3. [Third-Party Arm Documentation Site to Shut Down on 4 December 2026](#item-tech-news-3) ⭐️ 7.0/10
4. [Z.ai Releases GLM-5.4, Its First Looped-Transformer Coding Model](#item-tech-news-4) ⭐️ 7.0/10

**Technology Blog**
1. [vLLM Day-0 Support for ERNIE 5.5 Flash Preview](#item-tech-blog-1) ⭐️ 6.0/10

**Financial News**
1. [Fed&\#x27;s Williams Says More Work Needed to Return Inflation to 2%](#item-finance-news-1) ⭐️ 7.0/10

---

## Technology News

<a id="item-tech-news-1"></a>
### [Ladybird releases first alpha for macOS and Linux](https://ladybird.org/posts/alpha/) ⭐️ 8.0/10

The Ladybird project released its first alpha, publishing precompiled macOS and Linux builds of a browser built largely from scratch rather than on Chromium or Gecko. It includes its own HTML parsing, CSS engine, layout, JavaScript, and WebAssembly implementations, while relying on external HarfBuzz, Skia, ffmpeg, and SQLite; tabs run in separate processes. Early testing loaded ffmpeg-in-WebAssembly and Pyodide pages, but Datasette Lite failed because navigator.serviceWorker.startMessages is unimplemented. Ladybird&\#x27;s October update added 75,650 web-platform-tests passes, moving it ahead of Safari on that suite but still behind Firefox and Chrome; the project warns the alpha will break some sites and crash.

hackernews · janvdberg · Nov 23, 16:13 · [Discussion](https://news.ycombinator.com/item?id=50614249)

**「Background」** Ladybird originates from SerenityOS, the from-scratch operating-system project, from which it has brought in code; it is now an independent browser engine with its own HTML parser, CSS engine, layout, JavaScript and WebAssembly implementations, while still relying on external components such as HarfBuzz, Skia, ffmpeg and SQLite. Before this alpha, the project had leaned heavily on AI coding agents: its October 2026 newsletter reported a 75,650-pass gain in web-platform-tests, including a five-day jump of roughly 60,000 passes.

**「Impact」** Users can install and test Ladybird without building it, but the alpha is not suitable as a dependable daily browser: the project says some sites will fail and crashes will occur, and it provides in-browser broken-site reporting plus optional crash reports. The Datasette Lite failure marks service-worker-heavy web apps as a concrete compatibility gap to watch.

**「Community discussion」** Commenters reported that many sites rendered correctly, including Proxmox and NoVNC, with one saying NoVNC felt snappier than in Firefox, while another noticed slightly jerky scrolling. Others asked about fingerprinting protections and what precautions to take while the browser is alpha.

**Tags**: `#browser engines`, `#open source`, `#Ladybird`, `#alpha release`, `#web standards`

---

<a id="item-tech-news-2"></a>
### [Nvidia Board Reinstates Jensen Huang as CEO, Citing U.S. Government Input](https://www.cnbc.com/2026/11/23/nvidia-jensen-huang-ceo.html) ⭐️ 7.0/10

Nvidia&\#x27;s board has reinstated Jensen Huang as CEO, according to the headline of a CNBC report dated Nov. 23, 2026. A statement quoted in the discussion says the board received input from senior levels of the U.S. government and concluded that Huang&\#x27;s reinstatement &quot;poses no national security risk,&quot; making government consultation an explicit part of the decision. The supplied item contains only the headline, links, and comment fragments rather than the article body, so the board vote, the circumstances of Huang&\#x27;s departure, and the terms of his return are not independently detailed here.

hackernews · jaz · Nov 23, 14:00 · [Discussion](https://news.ycombinator.com/item?id=50611576)

**「Background」** Jensen Huang had resigned a little more than a week before the board&\#x27;s November 23 decision, amid reports of extramarital affairs including one with a woman alleged to be a Chinese spy, according to Al Jazeera&\#x27;s account. Nvidia&\#x27;s announcement said the reinstatement was effective immediately and restored his board seat along with the president and CEO titles, reversing a departure that had lasted only about a week.

**「Oversight path for export decisions」** Nvidia&\#x27;s board set up a committee to oversee its national security policies and compliance with U.S. export controls only days before the reported reinstatement decision, so any change in how the company ships AI chips to China would run through that board-level review rather than resting on the CEO alone. Reporting on smuggling cases shows continued appetite for Nvidia&\#x27;s chips in China, which means customers and partners should expect licensing and end-use scrutiny to persist regardless of who holds the CEO title.

**「Community Discussion」** Commenters treated the board&\#x27;s citation of U.S. government input as the operative justification, with one arguing that Delaware&\#x27;s Caremark standard plus a reported Justice Department decision not to prosecute would shield directors from individual liability. Others questioned the unanimous reversal within roughly two weeks and compared it to OpenAI&\#x27;s 2023 board episode, arguing that a company&\#x27;s formal governance structure may not reflect its real one; several also criticized what they described as inconsistent U.S. enforcement of chip export controls against Nvidia versus ASML and Japanese chip companies.

<details><summary>References</summary>
<ul>
<li><a href="https://investor.nvidia.com/news/press-release-details/2026/NVIDIA-Board-Reinstates-Jensen-Huang-as-President-CEO-and-Board-Director/default.aspx">NVIDIA Corporation - NVIDIA Board Reinstates Jensen Huang as...</a></li>
<li><a href="https://www.aljazeera.com/economy/2026/11/23/nvidia-board-reinstates-jensen-huang-as-ceo">Nvidia board reinstates Jensen Huang as CEO | Al Jazeera</a></li>
<li><a href="https://www.cbsnews.com/news/nvidia-export-control-committee-china-chips/">Nvidia&#x27;s board forms export oversight panel after scrutiny ...</a></li>
<li><a href="https://apnews.com/article/ai-chips-nvidia-huawei-china-1ae6228c4928ddbb43f984e9b38f49dd">Nvidia loses its AI chip edge in China as US export controls ...</a></li>

</ul>
</details>

**Tags**: `#Nvidia`, `#corporate governance`, `#US export controls`, `#semiconductor policy`, `#national security`

---

<a id="item-tech-news-3"></a>
### [Third-Party Arm Documentation Site to Shut Down on 4 December 2026](https://arm.jonpalmisc.com/) ⭐️ 7.0/10

The third-party site arm.jonpalmisc.com, which hosts browsable Arm architecture documentation, will be discontinued on 4 December 2026 at Arm&\#x27;s request. The maintainer says Arm cited his use of its trademarks and intellectual property and that avoiding that claim while keeping the site useful is difficult. He said he is considering offers to host mirrors, seek legal advice, and release the site&\#x27;s source code without Arm IP so others can generate a similar site for personal use. The notice&\#x27;s exact wording and legal basis were not supplied, so the details remain unconfirmed beyond the maintainer&\#x27;s account.

hackernews · tech234a · Nov 23, 19:17 · [Discussion](https://news.ycombinator.com/item?id=50617499)

**「Background」** Jon&\#x27;s Arm Reference was an unofficial, searchable guide to AArch64 instructions and system registers for the Armv8-A and Armv9-A architectures, rather than Arm&\#x27;s own documentation portal. It was described as widely used by developers as a convenience reference. The site&\#x27;s creator said Arm&\#x27;s lawyers had notified him to remove the site or face legal action, and the site is now set to close on 4 December 2026.

**「Impact」** Developers who used the site as an accessible HTML reference will lose that route after 4 December 2026. Mirrors and a source-only release are alternatives the maintainer is considering, not replacements that have been announced or confirmed.

**「Community Discussion」** Commenters questioned whether publishing hardware documentation is fair use and whether Arm can restrict access to information about publicly sold chips. One compared the pages with a Stanford-hosted Arm64 reference, while another said Arm&\#x27;s machine-readable specification appears to be distributed under a BSD-style license.

<details><summary>References</summary>
<ul>
<li><a href="https://zeli.app/story/50617499">Arm&#x27;s Lawyers Force Shutdown of Popular · Hacker News | Zeli</a></li>
<li><a href="https://arm.jonpalmisc.com/">Jon&#x27;s Arm Reference</a></li>

</ul>
</details>

**Tags**: `#Arm`, `#documentation takedown`, `#trademark/IP`, `#hardware documentation`, `#developer access`

---

<a id="item-tech-news-4"></a>
### [Z.ai Releases GLM-5.4, Its First Looped-Transformer Coding Model](https://simonwillison.net/2026/Nov/23/glm-54/) ⭐️ 7.0/10

Z.ai released GLM-5.4, its first model built on a looped-transformer architecture and aimed at generalized coding. The model runs a group of weight-shared layers for multiple iterations, which Z.ai says yields a deeper network without increasing parameter count. It is not yet available as open weights, and access currently requires a Z.ai Coding Plan subscription because the model is not exposed through the regular API. The account includes no benchmark results; Simon Willison&\#x27;s informal pelican test found 5.4 broadly similar to 5.3 and closer in style to OpenAI and Anthropic outputs than earlier GLM versions.

rss · Simon Willison · Nov 23, 23:40

**「Background」** In a standard Transformer, each layer runs once per forward pass; a looped transformer reuses a group of weight-shared layers over multiple iterations to refine hidden states. Z.ai says this produces a deeper effective network without increasing the parameter count. The approach surfaced days earlier in Thinking Machines Lab&\#x27;s Inkling 2 Mini, which runs its middle layers three times for every token.

**「Impact」** Developers cannot yet self-host GLM-5.4 or reach it through Z.ai&\#x27;s regular API; testing requires a Coding Plan subscription, though its key works against the shared OpenAI-compatible Responses API at https://api.z.ai/api/v1. Tooling also needs updating: the existing llm-zai plugin does not yet support the model, which led Simon Willison to publish a separate llm-glm plugin.

**Tags**: `#looped transformers`, `#GLM-5.4`, `#Z.ai`, `#AI models`, `#coding models`

---

## Technology Blog

<a id="item-tech-blog-1"></a>
### [vLLM Day-0 Support for ERNIE 5.5 Flash Preview](https://vllm.ai/blog/2026-11-24-ernie-5-5-flash-preview) ⭐️ 6.0/10

rss · vLLM Blog · Nov 24, 00:00

**「Background」** ERNIE 5.5 Flash Preview is a 280B-parameter sparse mixture-of-experts model with 14B parameters active per token and a 1M-token context. Baidu’s ERNIE team and vLLM say they enabled day-0 serving through a standalone plugin rather than a fork, custom Docker image, or nightly build.

**「Solution」** The vLLM-ERNIE plugin installs beside the official vllm==0.32.0 wheel and registers ERNIE through vllm.general\_plugins, loading model code only when an ERNIE config appears while vLLM supplies attention, KV-cache, speculative-decoding, parallelism, and serving components. To reduce kernel launches and intermediate-memory traffic, the authors fold VHA cross-head mixing into a single matrix and fuse FP8 quantization, merge Multi-Router Latent MoE routing, single-pass the MultiMax output head, and fuse gated attention, reporting 1.55×–6.53× per-kernel gains over naive implementations. FlashIndexer adds a small per-token head router trained by distillation plus threshold pre-filtering, which the post credits with about a 1.4× speedup at 1M context; routed experts use MXFP4 W4A8 with quantization-aware training, other weights and the KV cache use FP8, and a bundled three-layer DSpark draft model proposes up to seven tokens per step, with mean acceptance reported above 4.0 on coding and agent workloads. These are vendor-reported results without detailed benchmark methodology.

**「Takeaway」** The authors present the plugin as a template for timely day-0 support: a specialized model can reuse vLLM’s infrastructure while shipping fixes on its own schedule, without affecting other models. The performance claims remain promising but unverified until independent benchmarks appear.

**Tags**: `#vLLM`, `#ERNIE`, `#MoE inference`, `#kernel fusion`, `#speculative decoding`

---

## Financial News

<a id="item-finance-news-1"></a>
### [Fed&\#x27;s Williams Says More Work Needed to Return Inflation to 2%](https://www.cnbc.com/2026/11/23/john-williams-fed-inflation-rate-hikes.html) ⭐️ 7.0/10

New York Fed President John Williams said the Federal Reserve still has work to do to return inflation to its 2% target, indicating further rate action can unfold gradually and forecasting inflation will reach the goal in 2028. Markets are fully pricing a quarter-point increase at the Dec. 8-9 meeting from the current 3.75%-4% range.

rss · CNBC Finance · Nov 23, 21:02

**「Background」** Inflation has stayed above the Fed&\#x27;s goal even as the economy has continued to grow, and officials have split over how quickly to raise rates, with Williams favoring a measured approach.

**Tags**: `#Federal Reserve`, `#monetary policy`, `#interest rates`, `#inflation`, `#John Williams`

---