---
layout: default
title: "Horizon Summary: 2026-11-22 (EN)"
date: 2026-11-22
lang: en
---

> From 7 items, 3 important content pieces were selected

---

**Technology News**
1. [Purported Lean verification of Riemann Hypothesis draws checker-trust debate](#item-tech-news-1) ⭐️ 9.0/10
2. [Graham Dumpleton&\#x27;s Muru: AI-assisted Rust server for ASGI and WSGI Python apps](#item-tech-news-2) ⭐️ 7.0/10

**Technology Blog**
1. [Good Programming Is Mostly Blunder Avoidance](#item-tech-blog-1) ⭐️ 5.0/10

---

## Technology News

<a id="item-tech-news-1"></a>
### [Purported Lean verification of Riemann Hypothesis draws checker-trust debate](https://leanprover-community.github.io/blog/posts/riemann-hypothesis/) ⭐️ 9.0/10

A purported Lean formal verification of the Riemann Hypothesis is being widely discussed, framed around an AI-assisted proof and independent checkers. The item provides no primary source content, so the exact formal statement, authorship, proof dependencies, and whether the Lean kernel accepted the result remain unconfirmed.

hackernews · g-b-r · Nov 21, 14:36 · [Discussion](https://news.ycombinator.com/item?id=50589618)

**「Background」** Lean is an interactive theorem prover whose proofs are checked by a small kernel, and Mathlib is its community-maintained library of formalized mathematics. According to the Lean community blog, the Riemann Hypothesis statement used in the verification was already part of Mathlib as \`RiemannHypothesis\` and had been vetted by Lean and number-theory experts.

**「Impact」** For Lean users and number theorists, the claim is not actionable until the exact formal statement and kernel-check record are audited, because the item supplies no primary proof text and commenters note that a prior fake Collatz refutation passed a checker.

**「Community discussion」** Commenters disagree about how much the independent checkers settle: one argues that a shared kernel bug is now vanishingly unlikely because multiple implementations carry consistency proofs, while another notes that a fake Collatz refutation previously passed one checker and that the public claim does not rest on human review. Others credit Levent for eliciting the result and describe the formalization as covering a large amount of mathematics, though those are community characterizations rather than confirmed details.

<details><summary>References</summary>
<ul>
<li><a href="https://leanprover-community.github.io/blog/posts/riemann-hypothesis/">Lean verification of the Riemann Hypothesis | Lean community blog</a></li>

</ul>
</details>

**Tags**: `#formal verification`, `#Lean`, `#Riemann Hypothesis`, `#AI-assisted theorem proving`, `#mathematics`

---

<a id="item-tech-news-2"></a>
### [Graham Dumpleton&\#x27;s Muru: AI-assisted Rust server for ASGI and WSGI Python apps](https://simonwillison.net/2026/Nov/21/muru/) ⭐️ 7.0/10

Graham Dumpleton, creator of mod\_wsgi, has started Muru, a new AI-assisted Rust server intended to run both ASGI and WSGI Python applications in development and production. The project is at an early, introductory stage: Simon Willison&\#x27;s post links to the GitHub repository and to 18 design and development write-ups published between November 4 and November 21, 2026, covering worker internals, &quot;import once, fork many&quot; startup, HTTPS in development, running WSGI and ASGI together, releases without restarts, canary deployments without a service mesh, Kubernetes integration, scaling to zero, and a per-page toolbar with tracing. No benchmarks, release artifacts, or adoption are cited, so the posts describe intended design and work in progress rather than demonstrated production performance. Dumpleton says AI does much of the surface work but that judging what is not good enough remains his job, drawing on two decades of mod\_wsgi experience.

rss · Simon Willison · Nov 21, 23:56

**「Background」** mod\_wsgi, which Graham Dumpleton started 20 years ago, is his long-standing way of serving Python web applications; Muru is a separate Rust server rather than an extension of that project. It is intended to run both WSGI, the older synchronous Python web-server interface, and ASGI, the asynchronous interface used by newer Python frameworks.

**「Impact」** For Python web infrastructure teams, Muru is not yet presented as a drop-in production replacement for existing WSGI/ASGI servers, given the absence of published benchmarks or adoption. Its stated scope bundles capabilities that often require separate tooling — development-time TLS, canary releases, scale-to-zero, Kubernetes-aware operation, and built-in tracing — so the design posts are the practical material available to assess whether those claims hold.

**Tags**: `#Python`, `#web servers`, `#ASGI/WSGI`, `#Rust`, `#open source`

---

## Technology Blog

<a id="item-tech-blog-1"></a>
### [Good Programming Is Mostly Blunder Avoidance](https://seangoedecke.com/to-code-well-avoid-blunders/) ⭐️ 5.0/10

rss · Sean Goedecke · Nov 22, 00:00

**「Background」** Many engineers treat programming as a search for brilliant insights or beautiful new abstractions, but Sean Goedecke argues that good code depends more on avoiding catastrophic mistakes. He focuses on large commercial codebases with big teams—what he calls “impure engineering”—where one bad decision can undo a great deal of careful work.

**「Solution」** Goedecke’s central claim is that software offers no durable winning advantage: unlike a basketball lead, an elegant codebase can become janky after a single blunder. He lists examples such as introducing a parallel system for the same task, creating a second source of truth, turning a safe synchronous operation into a delicate asynchronous one, adding subtle failure points, or complicating a key interface. The cardinal sins are inconsistency and unnecessary requirements. Inconsistency breaks trust, forcing engineers to hunt for surprises instead of assuming code behaves sensibly; unnecessary requirements are sticky because later engineers must assume they are needed, and they interact combinatorially with new features, making large codebases hard to change. He therefore urges engineers to fit each task most normally into the existing codebase and trim it to the smallest requirement set, treating impulses toward clever patterns as warning signs. The advice applies whether code is written by hand or by an AI agent, though he observes that coding agents are worse at avoiding unnecessary requirements.

**「Takeaway」** Goedecke’s thesis is that good programming is largely disciplined conservatism: maintain consistency, reject unnecessary requirements, and spend attention on avoiding blunders rather than chasing cleverness, because in large team codebases one bad decision can outweigh many elegant ones.

**Tags**: `#software engineering`, `#code quality`, `#complexity`, `#consistency`, `#maintainability`

---