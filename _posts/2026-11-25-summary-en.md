---
layout: default
title: "Horizon Summary: 2026-11-25 (EN)"
date: 2026-11-25
lang: en
---

> From 9 items, 5 important content pieces were selected

---

**Technology News**
1. [OpenAI math preprint claims matrix multiplication exponent equals 9/4](#item-tech-news-1) ⭐️ 8.0/10
2. [Ternary Bonsai 2.5 27B draws strong local-inference reports](#item-tech-news-2) ⭐️ 7.0/10
3. [OpenAI claims GPT-6 can design proteins; commenters question &quot;intrinsic&quot; framing](#item-tech-news-3) ⭐️ 7.0/10
4. [Simon Willison traces three LLM inflection points in twelve months](#item-tech-news-4) ⭐️ 7.0/10

**Financial News**
1. [Fed’s Williams Says More Work Needed to Return Inflation to 2%](#item-finance-news-1) ⭐️ 7.0/10

---

## Technology News

<a id="item-tech-news-1"></a>
### [OpenAI math preprint claims matrix multiplication exponent equals 9/4](https://github.com/openai/math/blob/main/preprints/The-matrix-multiplication-exponent-is-nine-fourths-November-24-2026/paper.pdf) ⭐️ 8.0/10

A paper posted in OpenAI&\#x27;s GitHub math repository under the title &quot;The matrix multiplication exponent is nine fourths&quot; claims the matrix multiplication exponent is 9/4, i.e. Θ\(n^2.25\), a value that would pin down the exact asymptotic cost of the problem rather than just an upper bound. The item supplies only the PDF link and no abstract, so the precise statement, the field it applies to, and whether the bound is proved in both directions are not verifiable from the available material, and the result has not been independently checked. Commenters disagree about what is actually new: one says the paper gives the exact exponent 9/4 over every field, while another says the preprint itself states only O\(n^2.25\) at present, an upper bound that was already known, with the novelty being a matching lower bound of Ω\(n^2.25\). A third notes that a matching O\(n^2.25\) algorithm was published recently but is far from practical.

hackernews · E-Reverance · Nov 25, 01:19 · [Discussion](https://news.ycombinator.com/item?id=50637220)

**「Background」** The matrix multiplication exponent ω is the asymptotic exponent for multiplying n×n matrices, so a Θ\(n^2.25\) claim would require both an algorithm running in O\(n^2.25\) and a proof that no substantially faster method exists. Before this preprint, the best known upper bound was below 2.3716, while lower-bound work had established only much smaller bounds.

**「Impact」** If the lower bound holds up, it would end the decades-long effort to push the exponent below its current best value, since any claimed algorithm beating n^2.25 would have to be wrong; researchers working on upper bounds would instead be left with the narrower task of finding a practical algorithm attaining the bound, which commenters say the existing construction is not. The same commenter also reports that the paper claims polynomial-time algorithms for strongly polynomial linear programming, mean-payoff games, parity games and Condon&\#x27;s simple stochastic games, so the verification burden spans several open problems at once rather than one.

**「Community Discussion」** The main disagreement is about what the preprint actually proves: one commenter reads it as an exact exponent over every field, while others insist the posted version claims only the already-known O\(n^2.25\) upper bound and that the new part is the matching lower bound, arguing the submission&\#x27;s title misstates the result. Commenters also debate OpenAI&\#x27;s motives, speculating that the work came from an unreleased internal model whose recipe is not disclosed, and questioning whether corporate labs will fund this kind of theory work for public benefit the way Bell Labs once did.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Computational_complexity_of_matrix_multiplication">Computational complexity of matrix multiplication - Wikipedia</a></li>
<li><a href="https://www.researchgate.net/publication/377175782_New_Bounds_for_Matrix_Multiplication_from_Alpha_to_Omega">New Bounds for Matrix Multiplication : from Alpha to Omega</a></li>

</ul>
</details>

**Tags**: `#matrix multiplication`, `#algorithms`, `#complexity theory`, `#AI for math`, `#OpenAI`

---

<a id="item-tech-news-2"></a>
### [Ternary Bonsai 2.5 27B draws strong local-inference reports](https://prismml.com/news/bonsai-2-5-27b) ⭐️ 7.0/10

Ternary Bonsai 2.5 27B is a 27-billion-parameter model released in ternary \(Q2\) GGUF form, where weights are restricted to three values so the model fits in consumer memory; the project page itself was unavailable, so every performance figure here comes from commenters&\#x27; own runs. One reports 22–25 tokens/s generation and roughly 223 tokens/s prompt processing on a Mac Mini M5 Pro with 24GB RAM, with 128k context fitting easily in memory. On a self-built long-horizon agentic benchmark, another commenter measured 5 of 8 tasks passed in 296 steps and 76 minutes, versus 358 steps and 107 minutes for the earlier Bonsai 2 on the same tasks. A third says the model scores comparably to Opus 4.6 on SWE-bench Verified but questions how much of that reflects benchmark-specific tuning versus benchmark drift.

hackernews · b0m · Nov 24, 20:08 · [Discussion](https://news.ycombinator.com/item?id=50633922)

**「Background」** Ternary quantization constrains weights to three values, cutting a model&\#x27;s memory footprint far below 16-bit precision — which is how a 27B-parameter model can be packaged in roughly 5.9 GB. PrismML describes Bonsai 2.5 27B as an upgrade to Bonsai 2 27B, built on Qwen3.8 27B and retaining the earlier release&\#x27;s 5.9 GB footprint; the company reports its average score across the AppWorld and τ³-Bench agentic tool-calling benchmarks rising from 60.2 to 82.2. The model documentation lists a 262K-token context within 5.93 GB of ternary weights.

**「Deployment implications」** The 5.93 GB GGUF release with 262K context makes a 27B model practical on consumer hardware, but which runtime you use matters: PrismML says it runs on NVIDIA and Intel GPUs via llama.cpp and on Apple devices \(Mac, iPhone, iPad\) via MLX, so a team standardizing on one inference stack should confirm that path supports the full context length and agentic tooling before committing. Weights are published under Apache 2.0, so self-hosting and internal redistribution carry no licensing barrier.

**「Community discussion」** Commenters accepted the speed reports but pushed on the comparison baseline: hatthew asked for direct runs against equivalently small models, naming a Q1/Q2 quant of Qwen3.8 as an example. nik\_s questioned whether parity with Opus 4.6 on SWE-bench Verified reflects real capability, benchmark-specific tuning, or a moving benchmark, while thepoet&\#x27;s own long-horizon runs — equal pass rates but 17% fewer steps and 29% less time than Bonsai 2 — were presented as evidence the gain is real but incremental.

<details><summary>References</summary>
<ul>
<li><a href="https://prismml.com/news/bonsai-2-5-27b">PrismML — Introducing Ternary Bonsai 2.5 27B: Powering ...</a></li>
<li><a href="https://prismml.com/news/prismml-launches-ternary-bonsai-2-5-27b">PrismML — PrismML Launches Ternary Bonsai 2.5 27B for Agentic ...</a></li>
<li><a href="https://docs.prismml.com/models/bonsai-2-5-27b">Ternary Bonsai 2.5 27B - Bonsai - docs.prismml.com</a></li>
<li><a href="https://prismml.com/news/bonsai-2-5-27b">PrismML — Introducing Ternary Bonsai 2 . 5 27 B : Powering Agentic...</a></li>
<li><a href="https://huggingface.co/prism-ml/Ternary-Bonsai-2.5-27B-GGUF">prism-ml/ Ternary - Bonsai - 2 . 5 - 27 B -GGUF · Hugging Face</a></li>

</ul>
</details>

**Tags**: `#ternary quantization`, `#local LLM inference`, `#model release`, `#SWE-bench`, `#agentic coding`

---

<a id="item-tech-news-3"></a>
### [OpenAI claims GPT-6 can design proteins; commenters question &quot;intrinsic&quot; framing](https://openai.com/index/gpt-6-models-demonstrate-intrinsic-protein-design-capabilities/) ⭐️ 7.0/10

OpenAI published an announcement claiming GPT-6 models can design proteins, stating that GPT-6.2 was given the three-dimensional structures of five target proteins with marked minibinder attachment sites and wrote code to generate 3D minibinder designs &quot;without using specialized protein AI models.&quot; The same announcement, as quoted in comments, says converting those designs into lab-testable proteins required a specialized model called SolubleMPNN to suggest amino acid sequences, plus other specialized protein models to select candidates predicted to fold as designed and bind at the intended site. Hacker News commenters therefore dispute the &quot;intrinsic&quot; framing, arguing that sequence design — which largely determines the protein — remained with specialized tools. The available material contains no independent experimental confirmation, and commenters describe the evidence as heavy on computational work and light on laboratory controls.

hackernews · acossta · Nov 24, 21:02 · [Discussion](https://news.ycombinator.com/item?id=50634658)

**「Why sequence design matters」** Protein design pipelines typically work in stages: propose a 3D backbone structure, then find an amino acid sequence predicted to fold into it, then filter candidates computationally before lab testing. Specialized models such as the MPNN family have handled the sequence and filtering steps, so the division of labor in OpenAI&\#x27;s described workflow is the crux of the dispute.

**「Practical takeaway for designers」** For researchers assessing the claim, the described workflow still depends on SolubleMPNN and other specialized models for sequences and candidate selection, so GPT-6&\#x27;s demonstrated contribution is code generation and orchestration around those tools. Teams should treat the protein-design capability as unverified until results beyond computational candidate ranking — ideally wet-lab binding data — are shown.

**「Community reaction」** Commenters pushed back on the &quot;beyond specialized models&quot; claim: fabian2k asked what GPT-6.2 actually designed if the sequence is what determines the protein, while plaidfuji argued the model functions as a &quot;glue layer&quot; coordinating specialized sub-task tools, which LLMs do well and sometimes better than the specialists. joe-esquibel characterized the evidence as computationally heavy and thin on biological controls, and gopalv credited the result mainly to the model&\#x27;s ability to write code.

**Tags**: `#protein design`, `#GPT-6`, `#AI for science`, `#model capabilities`, `#Hacker News discussion`

---

<a id="item-tech-news-4"></a>
### [Simon Willison traces three LLM inflection points in twelve months](https://simonwillison.net/2026/Nov/24/llm-inflection-points/) ⭐️ 7.0/10

Simon Willison&\#x27;s Nov. 24 retrospective argues that LLM coding agents crossed three practical thresholds in the past twelve months. He dates the first to Claude Opus 4.5&\#x27;s release a year earlier, when Claude Code&\#x27;s default output became generally correct for his daily coding problems; OpenAI&\#x27;s GPT-5.1 Codex releases had a similar effect. The second was the June/July arrival of &quot;Fable class&quot; models—Claude Fable 5 and later peers—which could take a goal and tools and solve problems proactively, though Fable 5 was briefly placed under US export controls and unavailable until July 1. The third was September/October progress in 3D modeling and game development, including an Opus 5.5 run that spent 12 hours playtesting and rebalancing a game after he asked for it to be &quot;a LOT more fun.&quot;

rss · Simon Willison · Nov 24, 23:02

**「Background」** Claude Code is Anthropic&\#x27;s coding agent, launched on February 24, 2025 alongside Claude 3.7 Sonnet, which made it roughly nine months old when Claude Opus 4.5 shipped on November 24, 2025. Willison&\#x27;s retrospective rests on a before-and-after judgment from daily use: earlier models needed enough correction that the agent was not clearly faster than working unaided, whereas Opus 4.5 usually produced the right result by default, and OpenAI&\#x27;s GPT-5.1 family had a comparable effect on its Codex agent around the same time.

**「Impact」** Developers building on frontier models cannot assume uninterrupted access: Willison recounts that Fable 5 was placed under US export controls days after release and was not restored until July 1. His account also raises the practical bar for evaluating coding agents, from plausible demos to default output he can use on daily work.

**Tags**: `#LLM coding agents`, `#AI engineering`, `#Claude Opus 4.5`, `#model evolution`, `#developer tools`

---

## Financial News

<a id="item-finance-news-1"></a>
### [Fed’s Williams Says More Work Needed to Return Inflation to 2%](https://www.cnbc.com/2026/11/23/john-williams-fed-inflation-rate-hikes.html) ⭐️ 7.0/10

New York Fed President John Williams said the Federal Reserve still has “work to do” to bring inflation back to its 2% target, adding that action can unfold “over time.” Ahead of the Dec. 8-9 FOMC meeting, markets are fully pricing a quarter-percentage-point rate increase from the current 3.75%-4% target range, though Williams did not explicitly endorse that move.

rss · CNBC Finance · Nov 24, 13:33

**「Background」** After its late-October meeting, the Fed said it would gather more information before deciding its next policy step; officials have differed over how quickly to raise rates, and the FOMC next meets Dec. 8-9.

<details><summary>References</summary>
<ul>
<li><a href="https://www.cnbc.com/2026/11/23/john-williams-fed-inflation-rate-hikes.html">Fed&#x27;s John Williams indicates higher interest rates likely &#x27;over time&amp;...</a></li>
<li><a href="https://www.fxstreet.com/macroeconomics/central-banks/fed">FOMC &amp; Fed Meeting | News &amp; Analysis</a></li>

</ul>
</details>

**Tags**: `#Federal Reserve`, `#monetary policy`, `#interest rates`, `#inflation`, `#John Williams`

---