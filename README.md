# Roli Bosch

**Founder of [Hermes Labs](https://hermes-labs.ai), an AI reliability engineering lab
building tools, research, and autonomous infrastructure for agents and LLM systems.**

I work on the operational language layer of AI systems: instructions, tool interfaces,
retrieval, memory, prompt injection, runtime policy, evaluation, and the evidence needed
to reconstruct what an agent actually did.

**Start here:** [Hermes Labs](https://hermes-labs.ai) · [GitHub org](https://github.com/hermes-labs-ai) · [LintLang](https://github.com/hermes-labs-ai/lintlang) · [Research](https://hermes-labs.ai/research) · [Contribution ledger](https://hermes-labs.ai/open-source/contributions)

[![LinkedIn](https://img.shields.io/badge/LinkedIn-rolibosch-0A66C2?logo=linkedin&logoColor=white)](https://www.linkedin.com/in/rolibosch/)
[![X](https://img.shields.io/badge/X-%40rolibosch-000000?logo=x&logoColor=white)](https://x.com/rolibosch)
[![Substack](https://img.shields.io/badge/Substack-rolibosch-FF6719?logo=substack&logoColor=white)](https://rolibosch.substack.com/)
[![Site](https://img.shields.io/badge/hermes--labs.ai-visit-4F46E5)](https://hermes-labs.ai)
[![Hermes Labs on GitHub](https://img.shields.io/badge/GitHub-%40hermes--labs--ai-181717?logo=github&logoColor=white)](https://github.com/hermes-labs-ai)

---

## Open-source systems

- **[LintLang](https://github.com/hermes-labs-ai/lintlang)**: static linter for agent configs, tool descriptions, and system prompts; no LLM call. [lintlang.ai](https://lintlang.ai) · [playground](https://hermes-labs.ai/lintlang#playground)
- **[Little Canary](https://github.com/hermes-labs-ai/little-canary)**: prompt-injection detection through sacrificial canary-model probes. [littlecanary.ai](https://littlecanary.ai)
- **[Fidelis Memory](https://github.com/hermes-labs-ai/fidelis)**: agent memory that returns original passages verbatim instead of a paraphrase.
- **[Hermes Rubric](https://github.com/hermes-labs-ai/hermes-rubric)**: evidence-first LLM-as-judge scoring; every dimension ties to a quoted file:line, hedged on thin evidence.
- **[Hermes Blind](https://github.com/hermes-labs-ai/hermes-blind)**: recovers the original goal of a long agent session from its first turn, for multi-turn drift recovery.
- **[zer0dex](https://github.com/hermes-labs-ai/zer0dex)**: local dual-layer memory pattern for agents, pairing a markdown index with local semantic retrieval.

Full catalog with evidence boundaries: [hermes-labs.ai/open-source](https://hermes-labs.ai/open-source)

---

## Contributions beyond Hermes Labs

<!-- hermes-contributions:start -->
**71 Upstream Contributions** · **8 Integrations & Adoption outcomes** (as of 2026-10-20).

### Upstream Contributions

Engineering and technical documentation accepted by external projects, plus reports that led to implemented upstream fixes.

- [microsoft/semantic-kernel #13610](https://github.com/microsoft/semantic-kernel/pull/13610) — Preserve the first system/developer message during Python chat-history truncation and handle the target_count=1 boundary. [Case study](https://hermes-labs.ai/case-studies/fixing-semantic-kernel-deleted-system-prompts).
- [langchain-ai/langchain #35544](https://github.com/langchain-ai/langchain/pull/35544) — Drop forced tool_choice with a warning when Anthropic extended thinking is enabled; preserve auto and unaffected requests. [Case study](https://hermes-labs.ai/case-studies/fixing-langchain-thinking-tools-crash).
- [microsoft/semantic-kernel #13635](https://github.com/microsoft/semantic-kernel/pull/13635) — Use value equality to avoid duplicate null entries in strict JSON Schema type arrays, with three regression tests. [Case study](https://hermes-labs.ai/case-studies/fixing-semantic-kernel-duplicate-null-schema).
- [stanfordnlp/dspy #9978](https://github.com/stanfordnlp/dspy/pull/9978) — Reject an empty Evaluate devset with a descriptive ValueError before metric-summary division, with a regression test. [Case study](https://hermes-labs.ai/case-studies/fixing-dspy-empty-devset).

### Integrations & Adoption

Working integrations accepted upstream, and independent developers building on our tools and ideas.

- **Promptfoo:** [Hermeneutic wording assertion](https://github.com/promptfoo/promptfoo/pull/10663) and [LintLang prompt-linting recipe](https://github.com/promptfoo/promptfoo/pull/11294).
- **LintLang in other workflows:** [Character.AI Larch CI](https://github.com/character-ai/larch/blob/ef7ee4b7f946f29fa51981f5422a1a93e83c79a7/.github/workflows/requirements-agent-linters.txt) and [independent Gentoo Haven packaging](https://github.com/thehaven/haven-overlay/tree/fbed4463d4e213a3bce98babbfc72ef78722d255/dev-util/lintlang).
- **Little Canary in other projects:** [Orbit's agent adapter](https://github.com/samvitgersappa/Orbit/pull/1) and [Preflight's independently adapted inspection techniques](https://github.com/DavidMChan/preflight/commit/186ce43c1ce122aba82c1904e777517834d1bc90).
- **zer0dex-inspired memory architecture:** independent implementations in [AllSource](https://github.com/all-source-os/all-source/blob/5d5cd154a165ee3bc1c1d95c47559f0be22ccf78/apps/web/content/from-zerodex-to-allsource.mdx) and [Mnemosyne](https://github.com/oveku/mnemosyne/pull/3).

[Full record and attribution](https://hermes-labs.ai/open-source/contributions) · [Structured ledger](https://hermes-labs.ai/contributions.json) · Verified 2026-10-20. Listings and pending submissions are excluded from these totals.
<!-- hermes-contributions:end -->

---

## Autonomous engineering

Many contributions from this account are independently discovered and executed by
**Hermes Labs' autonomous engineering infrastructure**, rather than beginning with me
selecting or prompting the specific task. I set objectives, operating constraints, and
authorization boundaries; steer or review where needed; and remain the responsible human
for work published from this account. The machinery is part of the experiment: can an
AI-native engineering institution notice useful work, investigate it, make bounded
changes, preserve evidence, and stop appropriately without requiring a human to
originate every individual action?

---

## Research

Hermes Labs publishes research and technical notes on AI reliability, epistemic failure,
measurement validity, agent-tool semantics, prompt injection, and the limits of model
self-report. Current work includes **Tool Differentia**, **Behavioral Canarying for
Prompt Injection**, **The Generative Horizon**, **Precise Records, Unstable Meanings**,
**A Taxonomy of Epistemic Failure Modes in Large Language Models**, and **The Asymmetric
Burden of Proof**.

- [Tool Differentia: Relational Static Analysis for AI Agent Tool Descriptions](https://doi.org/10.5281/zenodo.21817243)
- [Behavioral Canarying for Prompt Injection](https://doi.org/10.5281/zenodo.21818564)
- [The Generative Horizon](https://doi.org/10.5281/zenodo.21659634)
- [Precise Records, Unstable Meanings](https://doi.org/10.5281/zenodo.21652317)
- [A Taxonomy of Epistemic Failure Modes in Large Language Models](https://doi.org/10.5281/zenodo.19042469)
- [The Asymmetric Burden of Proof](https://doi.org/10.5281/zenodo.18867694)

[hermes-labs.ai/research](https://hermes-labs.ai/research) · [hermes-labs-ai/hermes-publications](https://github.com/hermes-labs-ai/hermes-publications)

---

## Where this came from

Hermes Labs emerged from an exploration of **philosophy of language, phenomenology, and
hermeneutics applied to AI systems**. The practical consequence became an engineering
thesis: in agent systems, language is part of the runtime. System prompts, tool
descriptions, retrieved passages, memory, summaries, policies, and evaluation criteria
do not merely describe a system. They participate in what it notices, chooses,
remembers, and does. Hermes Labs treats that layer as an engineering surface: something
that can be inspected before deployment, tested under adversarial conditions, controlled
at runtime, and verified afterward.

---

*[hermes-labs.ai](https://hermes-labs.ai) · [github.com/hermes-labs-ai](https://github.com/hermes-labs-ai)*
