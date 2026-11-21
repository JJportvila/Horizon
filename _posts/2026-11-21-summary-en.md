---
layout: default
title: "Horizon Summary: 2026-11-21 (EN)"
date: 2026-11-21
lang: en
---

> From 15 items, 8 important content pieces were selected

---

**Technology News**
1. [Levent Alpöge Claims a Proof of the Generalized Riemann Hypothesis](#item-tech-news-1) ⭐️ 8.0/10
2. [Unverified GitHub claim of finite-time blow-up for Navier–Stokes](#item-tech-news-2) ⭐️ 8.0/10
3. [Inkling 2 Mini: open-weight looped LLM draws local-inference tests](#item-tech-news-3) ⭐️ 7.0/10
4. [arXiv Paper Claims LLM Can Rewrite Its Own Weights Without Training](#item-tech-news-4) ⭐️ 7.0/10
5. [Signal Blog Examines Limits on AI Agents Capturing Mobile Data](#item-tech-news-5) ⭐️ 7.0/10

**Technology Blog**
1. [Why caching repeated LLM output barely reduces costs](#item-tech-blog-1) ⭐️ 6.0/10

**Financial News**
1. [Fed officials talk more as Warsh withholds rate guidance](#item-finance-news-1) ⭐️ 7.0/10
2. [U.S. Companies Shift to Net Equity Issuance, Adding Stock Supply](#item-finance-news-2) ⭐️ 7.0/10

---

## Technology News

<a id="item-tech-news-1"></a>
### [Levent Alpöge Claims a Proof of the Generalized Riemann Hypothesis](https://alpo.ge/remark.pdf) ⭐️ 8.0/10

Levent Alpöge has posted a PDF claiming a proof of the Generalized Riemann Hypothesis \(GRH\), a claim that remains unverified in the supplied material. Hacker News commenters describe an accompanying Lean formalization as about 1.3 GB and roughly 15 million lines, and one points to a separate human proof announcement by Alessandro Masullo. No independent confirmation or completed Lean check is reported, so this is an announced proof claim rather than an established result for mathematicians or formal-verification teams.

hackernews · iamronaldo · Nov 20, 14:16 · [Discussion](https://news.ycombinator.com/item?id=50574968)

**「Background」** The Riemann Hypothesis constrains how far prime counts can stray from their predicted totals; its generalized form extends comparable bounds to primes in arithmetic progressions through Dirichlet L-functions. The claim posted on November 20, 2026 comes from Levent Alpöge, a mathematician at Anthropic, who says he and Claude found a proof and released a PDF note with Lean code; State of Proof says it has not examined the proof.

**「Impact」** For mathematicians and formal-verification teams, the immediate task is verification: the community-reported ~1.3 GB, ~15 million-line Lean artifact would need to be independently built and checked, and the human proof assessed, before the GRH claim can be relied on.

**「Community Discussion」** Commenters focused on the scale of the claimed Lean development—about 1.3 GB and ~15 million lines—and on whether the result is AI-generated or has a human proof; one linked a separate human proof announcement, while another quoted Terence Tao&\#x27;s earlier skepticism that current AI alone could tackle the Riemann hypothesis. The thread does not establish agreement on whether the claim is correct, and no comment reports an independent verification.

<details><summary>References</summary>
<ul>
<li><a href="https://stateofproof.org/paper-watch/paper-2026-11-20-a-claimed-proof-of-the-riemann-hypothesis">A Claimed Proof of the Riemann Hypothesis — Paper Watch ...</a></li>
<li><a href="https://explainx.ai/blog/levent-alpoge-anthropic-riemann-hypothesis-claude-lean-proof-claimed-vs-verified-2026">Riemann Hypothesis Proof Claim: Claimed vs Verified ...</a></li>

</ul>
</details>

**Tags**: `#Generalized Riemann Hypothesis`, `#Lean theorem proving`, `#formal verification`, `#AI for mathematics`, `#mathematical proof`

---

<a id="item-tech-news-2"></a>
### [Unverified GitHub claim of finite-time blow-up for Navier–Stokes](https://github.com/tristanbuckmaster/navier-stokes/) ⭐️ 8.0/10

A GitHub item titled “Finite-time blow-up for the Navier–Stokes equations” claims a finite-time singularity for the equations; commenters describe it as the unforced version, distinguishing it from an earlier forced-equation construction they attribute to OpenAI. The supplied material contains only the repository link and discussion, with no accessible proof details or independent verification, so the claim’s validity, precise assumptions, and scope remain unconfirmed for mathematicians and fluid-dynamics researchers.

hackernews · trotro · Nov 20, 15:34 · [Discussion](https://news.ycombinator.com/item?id=50576232)

**「Background」** The Navier–Stokes existence and smoothness problem asks whether smooth three-dimensional initial data always produce globally smooth solutions with bounded kinetic energy, or whether finite-time breakdown can occur; it is one of the Clay Millennium Prize problems. The GitHub repository accompanies a paper by L. Alpöge and T. Buckmaster that claims finite-time blow-up for the unforced equations, supported by an approximate self-similar profile checked with interval arithmetic, and includes a Lean 4 formalization mapping the formal statements to the paper’s Theorems 1.1 and 7.1 and related results.

**「Verification burden」** For mathematicians and anyone citing this result, the immediate consequence is a verification burden: the claim arrives as a GitHub repository with no Lean formalization or peer review described in the supplied material, so treating the unforced Navier–Stokes problem as resolved—or building further work on the claimed blow-up—would be premature until the argument is checked independently. That contrasts with OpenAI&\#x27;s September Navier–Stokes claim, which was released with both a writeup and a Lean formalization, giving reviewers a machine-checkable artifact to audit.

**「Community discussion」** Commenters frame the key distinction as unforced versus forced equations, and one asks whether a real-time simulation could make the blow-up intuitively visible and show where the equations diverge from physical reality. Others speculate about priority and describe the same-day combination of this claim with a claimed generalized Riemann Hypothesis result as an exceptionally significant day for mathematics.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Navier%E2%80%93Stokes_priority_controversy">Navier–Stokes priority controversy - Wikipedia</a></li>
<li><a href="https://aixiv.online/abs/2611.02204">[2611.02204] Finite-time blow-up for the Navier–Stokes ...</a></li>
<li><a href="https://hotrepo.ai/tristanbuckmaster/navier-stokes">tristanbuckmaster/navier-stokes: Lean 4 formalization of a ...</a></li>
<li><a href="https://openai.com/index/navier-stokes-solution/">On the Navier–Stokes Millennium Prize Problem | OpenAI</a></li>

</ul>
</details>

**Tags**: `#Navier-Stokes`, `#mathematics`, `#fluid dynamics`, `#proof`, `#Hacker News`

---

<a id="item-tech-news-3"></a>
### [Inkling 2 Mini: open-weight looped LLM draws local-inference tests](https://thinkingmachines.ai/news/inkling-2-mini/) ⭐️ 7.0/10

Inkling 2 Mini, a new open-weight LLM built on a looped-transformer architecture, is drawing attention for claims that it can run well on local hardware; the underlying announcement was not supplied, so its benchmarks and performance claims remain unverified. Community discussion compared its benchmark level to Qwen3.8-27B and noted that the model was trained end-to-end in nvfp4, with a commenter linking to an Unsloth GGUF build for llama.cpp and Ollama. Early user reports were mixed: one commenter measured about 27 tokens/s decode on a Ryzen 395 using llama.cpp Vulkan, while another reported about 10 tokens/s on a 32GB M1 Pro at q4. A coding test produced a correct Python CSV-sorting script, but a separate coin-identification test failed after roughly 12,000 tokens of inconclusive output.

hackernews · jasondavies · Nov 20, 20:12 · [Discussion](https://news.ycombinator.com/item?id=50581260)

**「What a looped transformer does」** Inkling 2 Mini is built on a looped transformer, an architecture that reuses its middle layers for multiple passes per token — three in this model — rather than emitting more tokens, so extra computation goes into reasoning within each token step. Thinking Machines pairs that design with a mixture-of-experts layout of roughly 26B parameters, of which about 5.4B are active per token, keeping the model small enough to target machines with 32GB of memory. Because the looping and quantization scheme are non-standard, local runtime support is a prerequisite: Unsloth documentation specifies a build with looped-layer support and per-expert NVFP4 scales.

**「Local deployment friction」** Because Inkling 2 Mini is sized to run at full precision within 16 GB of RAM, local users can try it through llama.cpp or Unsloth, and a GGUF build is available for Ollama and llama.cpp. Expect build friction in the meantime: one commenter testing on a Ryzen 395 with llama.cpp Vulkan reported needing several unmerged PRs \(32694, 32657, 32429, 32704\) plus a small patch for roughly a 30% speedup to reach about 27 tokens/s decode.

**「Community discussion」** Commenters were enthusiastic about an open-weight looped model reaching benchmark territory comparable to Qwen3.8-27B, but some framed that as conditional on the results holding up in real use. Reported local tests were mixed, and one commenter raised safety and interpretability questions about looped architectures becoming widely available.

<details><summary>References</summary>
<ul>
<li><a href="https://thinkingmachines.ai/news/inkling-2-mini/">Introducing Inkling 2 Mini - Thinking Machines Lab</a></li>
<li><a href="https://ollama.com/library/inkling-2-mini">inkling - 2 - mini</a></li>
<li><a href="https://unsloth.ai/docs/models/inkling-2-mini">Inkling 2 Mini - Run Locally Guide | Unsloth Documentation</a></li>
<li><a href="https://thinkingmachines.ai/news/inkling-2-mini/">Introducing Inkling 2 Mini - Thinking Machines Lab</a></li>
<li><a href="https://unsloth.ai/docs/models/inkling-2-mini">Inkling 2 Mini - Run Locally Guide | Unsloth Documentation</a></li>

</ul>
</details>

**Tags**: `#LLMs`, `#open weights`, `#looped transformers`, `#local inference`, `#model release`

---

<a id="item-tech-news-4"></a>
### [arXiv Paper Claims LLM Can Rewrite Its Own Weights Without Training](https://arxiv.org/abs/2611.21885) ⭐️ 7.0/10

An arXiv paper claims a language model can rewrite its own weights through its own reasoning, without gradients or training, and that its accuracy rose across eight consecutive self-edit sessions. The supplied material does not include the full experimental setup or independent verification, and the claimed self-improvement appears narrow: commenter aesthesia said the only modification was shortening reasoning traces to avoid the token limit. The paper is therefore best read as a reported self-modification result whose generality and novelty are still being debated, not as an established general self-improvement capability.

hackernews · lwhsiao · Nov 20, 16:29 · [Discussion](https://news.ycombinator.com/item?id=50577265)

**「Background」** A language model’s weights are its learned parameters, and once training ends they are normally fixed; improving the model usually requires another training run or inference-time prompting and scaffolding that does not persist. Google’s SLEEP framework has proposed one way around that by updating numerical weights from self-generated practice examples during an offline phase, unlocking pre-allocated mixture-of-experts memory blocks. The self-rewriting paper instead claims a model can make persistent weight changes through its own reasoning, without gradients or a training run.

**「Impact」** For developers and safety evaluators, the claimed mechanism implies that a single pre-deployment evaluation of a fixed checkpoint may not cover the model after it has edited its own weights; capability and alignment checks would need to be repeated after accepted edits. The supplied evidence does not show that such edits preserve safety behavior or broad capability.

**「Community discussion」** Commenters questioned both novelty and framing. aesthesia argued the reported gain came only from shortening reasoning traces to avoid token limits and compared it with prior weight-space programming work, while gavinray cited Google&\#x27;s SLEEP framework as an earlier example; Toutouxc added that testing edits and keeping only what works sounds like training despite the &quot;no training&quot; claim.

<details><summary>References</summary>
<ul>
<li><a href="https://arxiv.org/abs/2611.21885">[2611.21885] Language Models Can Rewrite Their Own Weights</a></li>
<li><a href="https://research.google/blog/the-sleep-framework-a-new-way-for-llms-to-retain-knowledge-in-continual-learning/">The sleep framework : A new way for LLMs to retain knowledge in...</a></li>

</ul>
</details>

**Tags**: `#self-modifying models`, `#weight editing`, `#LLM research`, `#AI safety`, `#arXiv`

---

<a id="item-tech-news-5"></a>
### [Signal Blog Examines Limits on AI Agents Capturing Mobile Data](https://signal.org/blog/protecting-your-privacy/) ⭐️ 7.0/10

Signal published a blog post examining efforts to restrict AI agents on mobile operating systems from capturing sensitive user data. The supplied material does not detail specific technical measures, versions, or confirm that new protections have shipped. The discussion frames the issue around platform-level privacy and app security for mobile users and developers.

hackernews · dotcoma · Nov 20, 09:42 · [Discussion](https://news.ycombinator.com/item?id=50572348)

**「Background」** The concern is that AI agents built into mobile operating systems can capture content displayed in other apps, a screen-level access path that app sandboxing and end-to-end encryption do not automatically close. Signal had already restricted screenshots as a defense against Microsoft Recall’s screen capture, and its new post argues that the same risk now applies to agents embedded in phone operating systems.

**「Impact」** For Signal users, the risk described in the discussion is indirect: a contact&\#x27;s AI-enabled app could capture chat data even if the user has not installed such an app, according to a commenter. That makes mobile OS permissions and app access the practical control point rather than in-app protections alone.

**「Community Discussion」** Commenters debated whether app-level defenses are sufficient, with one asking Signal to publish forensics findings so smaller developers could benefit. Another argued that screenshot blocking will not work long term and that users need greater control over the operating system, citing alternatives such as GrapheneOS and Linux.

<details><summary>References</summary>
<ul>
<li><a href="https://signal.org/blog/protecting-your-privacy/">Signal is Serious About Protecting Your Privacy</a></li>
<li><a href="https://www.theregister.com/security/2026/11/20/signal-slams-door-on-prying-ai-agents-to-protect-privacy/5311466">Signal slams door on prying AI agents to protect privacy</a></li>

</ul>
</details>

**Tags**: `#privacy`, `#security`, `#mobile OS`, `#AI agents`, `#Signal`

---

## Technology Blog

<a id="item-tech-blog-1"></a>
### [Why caching repeated LLM output barely reduces costs](https://seangoedecke.com/why-output-caching-doesnt-work/) ⭐️ 6.0/10

rss · Sean Goedecke · Nov 21, 00:00

**「Background」** LLM inference already relies on input caching—storing the KV cache so the conversation history is not recomputed each turn—and output tokens are more expensive because they must be generated one at a time. Sean Goedecke asks whether repeated output should be cached in the same spirit.

**「Solution」** He describes agents repeatedly quoting code, evidence documents, and sample outputs, and suggests a model could instead emit references such as “src/script.py:12-15” for the harness to expand. His central objection is that this only targets visible output: he believes models rarely repeat themselves in internal reasoning, though he is only moderately confident. In his own agent histories, visible output is about 6% of output tokens, reasoning is 50%, and tool calls are 44%; even saving two-thirds of visible tokens would cut total output tokens by just 4%, an Amdahl’s-law ceiling. The remaining 94% is largely a function of intelligence, since smarter models can need fewer reasoning and tool-call tokens—so a model that costs 5x more per token can be cheaper if it uses 6x fewer tokens. A better harness also helps, but the author doubts it creates much durable advantage because improvements can be copied; he also flags uncertainty about whether tool calls repeat content from reasoning.

**「Takeaway」** The author concludes that reducing repeated visible output is a minor optimization; the meaningful lever is model intelligence—and secondarily harness quality—which reduces the far larger invisible reasoning and tool-call budget.

**Tags**: `#LLM inference economics`, `#output caching`, `#coding agents`, `#token costs`, `#Amdahl&\#x27;s law`

---

## Financial News

<a id="item-finance-news-1"></a>
### [Fed officials talk more as Warsh withholds rate guidance](https://www.cnbc.com/2026/11/20/warsh-fed-forward-guidance-rate-hikes.html) ⭐️ 7.0/10

Federal Reserve officials have spoken publicly about interest rates more in the past two weeks than in any similar stretch since the start of 2025, according to a Bank of America analysis, while Chair Kevin Warsh continues to avoid signaling where policy is headed. Traders are pricing a 100% probability of at least a quarter-percentage-point rate hike at the December meeting, with a small chance of a half-point move, according to CME Group&\#x27;s FedWatch.

rss · CNBC Finance · Nov 20, 21:10

**「Background」** Kevin Warsh, who became Federal Reserve chair in 2026, has rejected forward guidance—the practice of signaling future rate decisions—leaving other officials to shape market expectations in his place.

**「Market impact」** Bank of America warns the public back-and-forth is producing “undue rates volatility” in already turbulent markets, a condition that matters most for rate-sensitive borrowers and investors.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Kevin_Warsh">Kevin Warsh - Wikipedia</a></li>
<li><a href="https://www.cnbc.com/2026/07/18/warshgpt-federal-reserve-communications-task-force-warsh.html">&#x27;WarshGPT&#x27;: Wall Street adapts to new era of Federal Reserve ...</a></li>
<li><a href="https://www.cmegroup.com/markets/interest-rates/cme-fedwatch-tool?redirect=/trading/interest-rates/fed-funds.html">FedWatch - CME Group</a></li>

</ul>
</details>

**Tags**: `#Federal Reserve`, `#monetary policy`, `#interest rates`, `#forward guidance`, `#FOMC`

---

<a id="item-finance-news-2"></a>
### [U.S. Companies Shift to Net Equity Issuance, Adding Stock Supply](https://www.cnbc.com/2026/11/20/equity-issuance-bull-market-problem.html) ⭐️ 7.0/10

U.S. companies have switched from share repurchases to net equity issuance, with net new shares equal to 3.1% of total market capitalization as of late last week, according to an Acadian Asset Management analysis cited by CNBC. Acadian calls the added supply a potential headwind for the four-year-old bull market, though net issuance remains below the peaks of the tech bubble and COVID bubble.

rss · CNBC Finance · Nov 20, 14:15

**「Background」** The shift reverses years in which buybacks reduced the number of shares available to trade and mechanically lifted earnings per share, a trend investors had cited as support for higher prices.

**「Impact」** Investors in large equity issuers are exposed to more shares in circulation and potential dilution, as Alphabet&\#x27;s $84.8 billion June raise to fund AI infrastructure and Meta&\#x27;s $25 billion October common-stock offering show.

**Tags**: `#equity issuance`, `#share buybacks`, `#stock market supply`, `#IPOs`, `#AI capex`

---