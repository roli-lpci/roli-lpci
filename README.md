# Roli Bosch

**Founder, [Hermes Labs](https://hermes-labs.ai) · Research and engineering on the language layer of LLM systems and agents**

I study how language models fail, mislead, and break, then build tools from what I find.

[![LinkedIn](https://img.shields.io/badge/LinkedIn-rolibosch-0A66C2?logo=linkedin&logoColor=white)](https://www.linkedin.com/in/rolibosch/)
[![X](https://img.shields.io/badge/X-%40rolibosch-000000?logo=x&logoColor=white)](https://x.com/rolibosch)
[![Substack](https://img.shields.io/badge/Substack-rolibosch-FF6719?logo=substack&logoColor=white)](https://rolibosch.substack.com/)
[![Site](https://img.shields.io/badge/hermes--labs.ai-visit-4F46E5)](https://hermes-labs.ai)

---

## What I work on

My background is philosophy of language. Instructions, tool descriptions, retrieved passages, memory summaries, and grading rubrics are all text, and text changes meaning when it is compressed, retrieved, handed off, or rewritten. A history reducer in Microsoft Semantic Kernel was treating the system prompt as one more message to trim, so the instruction that governs a conversation quietly disappeared mid-run. That is an interpretation error written in code. I fixed it upstream. The same pattern shows up wherever language changes hands in a system.

Hermes Labs is an independent AI research and engineering lab built around that layer. We study how it breaks, build tools that catch it, and integrate working systems for teams shipping LLM applications and agents.

---

## Research

Papers and technical notes, each with a DOI, each stating what its evidence does and does not support:

- [Tool Differentia: Relational Static Analysis for AI Agent Tool Descriptions](https://doi.org/10.5281/zenodo.21817243)
- [Behavioral Canarying for Prompt Injection](https://doi.org/10.5281/zenodo.21818564)
- [The Generative Horizon](https://doi.org/10.5281/zenodo.21659634)
- [Precise Records, Unstable Meanings](https://doi.org/10.5281/zenodo.21652317)
- [A Taxonomy of Epistemic Failure Modes in Large Language Models](https://doi.org/10.5281/zenodo.19042469)
- [The Asymmetric Burden of Proof](https://doi.org/10.5281/zenodo.18867694)

Abstracts, hosted copies, and citation exports: [hermes-labs.ai/research](https://hermes-labs.ai/research)

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
| [**lintlang**](https://github.com/hermes-labs-ai/lintlang) | Static linter for agent configs, tool descriptions, and system prompts. No LLM call. | `pip install lintlang` |
| [**fidelis**](https://github.com/hermes-labs-ai/fidelis) | Fidelis Memory: agent memory that returns your original passages verbatim. | `pip install fidelis-memory` |
| [**little-canary**](https://github.com/hermes-labs-ai/little-canary) | Prompt-injection detection through sacrificial canary-model probes. | `pip install little-canary` |
| [**agent-gorgon**](https://github.com/hermes-labs-ai/agent-gorgon) | Runtime policy guard for autonomous agents, with forensic evidence. | `pip install agent-gorgon` |
| [**hermeneutic**](https://github.com/hermes-labs-ai/hermeneutic) | Mines corrections from agent chat logs and gates the next response. | `pip install hermeneutic` |
| [**langstate**](https://github.com/hermes-labs-ai/langstate) | Inspectable context compression for LLM conversations. | `pip install langstate` |

Full catalog with evidence boundaries: [hermes-labs.ai/open-source](https://hermes-labs.ai/open-source)

---

## Background

Philosophy of language (Wittgenstein, Gadamer, Heidegger) applied to AI systems. The traditions that spent centuries studying how meaning breaks down have a lot to say about why language models fail the way they do.

**LPCI** — Linguistically Persistent Cognitive Interface — is the throughline: persistent language between human and agent as the real substrate of reasoning in otherwise stateless models.

---

*[hermes-labs.ai](https://hermes-labs.ai) · [roli@hermes-labs.ai](mailto:roli@hermes-labs.ai)*
