# Roli Bosch

**Founder, [Hermes Labs](https://hermes-labs.ai) · AI assurance infrastructure for high-stakes systems**

I study how language models fail — then build tools from what I find.

[![LinkedIn](https://img.shields.io/badge/LinkedIn-rolando--bosch-0A66C2?logo=linkedin&logoColor=white)](https://www.linkedin.com/in/rolando-bosch/)
[![X](https://img.shields.io/badge/X-%40rolibosch-000000?logo=x&logoColor=white)](https://x.com/rolibosch)
[![Substack](https://img.shields.io/badge/Substack-LPCI-FF6719?logo=substack&logoColor=white)](https://lpci.substack.com/)
[![Site](https://img.shields.io/badge/hermes--labs.ai-visit-4F46E5)](https://hermes-labs.ai)

---

## What I work on

Hermes Labs studies structural reasoning failures in large language models and builds audit, runtime, and evidence tooling from what the research surfaces. The thesis: high-stakes AI deployments need a layer between model behavior and enterprise risk that isn't policy theater.

---

## Research

Two public papers, both on Zenodo with DOIs:

- **[The Asymmetric Burden of Proof](https://doi.org/10.5281/zenodo.18867694)** — LLMs systematically discount null findings. Matched-vignette benchmark across GPT-4o, GPT-5.2 Thinking, and Claude Haiku 4.5: 19.6–56.7 percentage-point probability gaps in 23 of 24 test conditions.
- **[A Taxonomy of Epistemic Failure Modes in LLMs](https://doi.org/10.5281/zenodo.19042469)** — Seven structural failure modes: null-result asymmetry, source-status credibility bias, agency dissolution, performative hedging, constraint evasion, silent instruction relaxation, controversy-truth conflation.

1,500+ controlled adversarial evaluations feeding this work. 5 US patent filings — 1 non-provisional pending, 4 provisional.

---

## Open-source contributions

<!-- hermes-contributions:start -->
The [canonical external contribution record](https://hermes-labs.ai/open-source/contributions) reports current, dated totals and separates merged engineering work, submitted fixes, integrations, documentation, ecosystem listings and research-index submissions. [Structured ledger](https://hermes-labs.ai/contributions.json).

Merged AI/framework fixes contributed by Roli Bosch (roli-lpci), founder of Hermes Labs:

- [microsoft/semantic-kernel #13610](https://github.com/microsoft/semantic-kernel/pull/13610) — Preserve the first system/developer message during Python chat-history truncation and handle the target_count=1 boundary. [Case study](https://hermes-labs.ai/case-studies/fixing-semantic-kernel-deleted-system-prompts).
- [langchain-ai/langchain #35544](https://github.com/langchain-ai/langchain/pull/35544) — Drop forced tool_choice with a warning when Anthropic extended thinking is enabled; preserve auto and unaffected requests. [Case study](https://hermes-labs.ai/case-studies/fixing-langchain-thinking-tools-crash).
- [microsoft/semantic-kernel #13635](https://github.com/microsoft/semantic-kernel/pull/13635) — Use value equality to avoid duplicate null entries in strict JSON Schema type arrays, with three regression tests. [Case study](https://hermes-labs.ai/case-studies/fixing-semantic-kernel-duplicate-null-schema).
- [stanfordnlp/dspy #9978](https://github.com/stanfordnlp/dspy/pull/9978) — Reject an empty Evaluate devset with a descriptive ValueError before metric-summary division, with a regression test. [Case study](https://hermes-labs.ai/case-studies/fixing-dspy-empty-devset).

[Mem0 #5250](https://github.com/mem0ai/mem0/pull/5250) contributed a Redis cosine-distance-to-similarity patch with regression coverage. It closed without merge after a maintainer acknowledged the conversion in a broader sweep. The [case study](https://hermes-labs.ai/case-studies/auditing-mem0-retrieval-scoring) preserves earlier community provenance and the patch’s missing clamp. Other substantive unmerged fixes remain visible in the ledger.

Typing modernization in PyTorch Ignite and Optuna, compatibility work and dependency maintenance remain credited in their own classes. Community-list and research-index submissions do not count as merged code contributions.
<!-- hermes-contributions:end -->

---

## Public tools

All under the Hermes Labs org: **[@hermes-labs-ai](https://github.com/hermes-labs-ai)**

| Tool | What it does | Install |
|------|---|---|
| [**lintlang**](https://github.com/hermes-labs-ai/lintlang) | Static linter for AI agent configs, tool descriptions, system prompts. Zero LLM calls. | `pip install lintlang` |
| [**little-canary**](https://github.com/hermes-labs-ai/little-canary) | Prompt injection detection via sacrificial canary-model probes. | `pip install little-canary` |
| [**zer0dex**](https://github.com/hermes-labs-ai/zer0dex) | Dual-layer memory for AI agents — compressed index plus vector retrieval. | `pip install zer0dex` |
| [**claude-router**](https://github.com/hermes-labs-ai/claude-router) | Routes prompts to the right Claude tier via local embeddings. | `pip install claude-router` |
| [**suy-sideguy**](https://github.com/hermes-labs-ai/suy-sideguy) | Runtime policy guard for autonomous agents. | `pip install suy-sideguy` |
| [**agent-convergence-scorer**](https://github.com/hermes-labs-ai/agent-convergence-scorer) | Score how similar N agent outputs are. | `pip install agent-convergence-scorer` |

Full catalog: [github.com/hermes-labs-ai](https://github.com/hermes-labs-ai)

---

## Background

Philosophy of language (Wittgenstein, Gadamer, Heidegger) applied to AI systems. The traditions that spent centuries studying how meaning breaks down have a lot to say about why language models fail the way they do.

**LPCI** — Linguistically Persistent Cognitive Interface — is the throughline: persistent language between human and agent as the real substrate of reasoning in otherwise stateless models.

---

*[hermes-labs.ai](https://hermes-labs.ai) · [rbosch@lpci.ai](mailto:rbosch@lpci.ai)*
