---
layout: default
title: "Horizon Summary: 2026-11-23 (EN)"
date: 2026-11-23
lang: en
---

> From 6 items, 2 important content pieces were selected

---

**Technology News**
1. [OpenAI Examines Perplexity as a Measure of LLM Intelligence](#item-tech-news-1) ⭐️ 7.0/10

**Technology Blog**
1. [The Case for Deliberate Flailing Under Uncertainty](#item-tech-blog-1) ⭐️ 6.0/10

---

## Technology News

<a id="item-tech-news-1"></a>
### [OpenAI Examines Perplexity as a Measure of LLM Intelligence](https://openai.com/index/perplexity-and-intelligence/) ⭐️ 7.0/10

OpenAI has published an article, “Perplexity and Intelligence,” for LLM researchers and evaluators that examines the relationship between perplexity—next-token prediction loss measured through cross-entropy—and model intelligence in benchmarking. The supplied source contains no article body, so the post’s specific model comparisons, methodology, and conclusions cannot be verified here.

hackernews · acossta · Nov 22, 17:06 · [Discussion](https://news.ycombinator.com/item?id=50601525)

**「Background」** Perplexity is the exponentiated cross-entropy of a language model&\#x27;s next-token predictions: it measures how surprised the model is by a text, with lower values indicating better prediction. OpenAI&\#x27;s essay, attributed to Chief Scientist Jakub Pachocki, examines how that pre-training metric relates to broader model capability and benchmarking.

**「Impact」** Developers comparing checkpoints should treat a perplexity score as meaningful only alongside the evaluation set and vocabulary it was computed on; the thread’s exchange over GPT-5 versus GPT-4.5 shows how easily a single number can be read as a capability ranking without that context.

**「Community Discussion」** Commenters debated the metric itself: one noted the article never defines perplexity and supplied a next-token-surprise explanation, while another called the cross-entropy trend “pretty shocking” and argued that prediction/compression rate is exactly the quantity that should track learned world models. Others questioned why GPT-5 would have higher perplexity than GPT-4.5 and noted a reported Microsoft commitment to publish MAI base-model perplexity on a common held-out set.

<details><summary>References</summary>
<ul>
<li>OpenAI Chief Scientist Proposes AI Pretraining Limits Tied to Perplexity Benchmarks</li>

</ul>
</details>

**Tags**: `#LLM evaluation`, `#perplexity`, `#cross-entropy`, `#OpenAI`, `#model benchmarking`

---

## Technology Blog

<a id="item-tech-blog-1"></a>
### [The Case for Deliberate Flailing Under Uncertainty](https://seangoedecke.com/when-in-doubt-flail-about/) ⭐️ 6.0/10

rss · Sean Goedecke · Nov 23, 00:00

**「Background」** When engineers face ambiguous product, engineering, or organizational problems, waiting for full understanding can be slower than deliberate “flailing,” Sean Goedecke argues—though he warns that doing it badly can damage a reputation.

**「Solution」** The method requires trying many things to contact reality directly and avoid overinvestment; because most guesses will be wrong, the engineer must treat feedback from users, metrics, and colleagues as decisive and ruthlessly drop anything without a strong positive response. In product work, Goedecke says, this means probing an uncertain market’s edges: at GitHub Models many features did not work, but letting AI inference run from a GitHub Actions token proved sticky and seeded “Continuous AI.” For tangled or unfamiliar systems, he favors speculative refactors or performance changes before fully mapping the codebase, then investigating only the promising ones; AI agents, he notes, make generating several candidate refactors easier. Organizational flailing—automating manual work, volunteering, or proposing long-term plans—is the most delicate case: even failed attempts can show effort, but if the engineer misses feedback and presses on, colleagues’ frustration can turn on them. Goedecke adds that the process feels like repeated failure from the inside even when a manager sees a proactive experimenter, and his argument rests mainly on this first-hand example rather than measurements.

**「Takeaway」** The broader point is that under genuine uncertainty, fast, feedback-driven experimentation can beat waiting for clarity—provided the experimenter stays reputationally careful and disciplined about killing losing bets.

**Tags**: `#engineering culture`, `#decision-making under uncertainty`, `#experimentation`, `#feedback loops`, `#senior engineers`

---