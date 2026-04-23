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

**26 PRs merged upstream.** Four landed in major AI framework repos:

- [**LangChain #35544**](https://github.com/langchain-ai/langchain/pull/35544) — dropped a forced `tool_choice` injection that broke Claude extended-thinking mode
- [**Microsoft Semantic Kernel #13610**](https://github.com/microsoft/semantic-kernel/pull/13610) — fixed the truncation reducer silently deleting system prompts
- [**PyTorch Ignite #3591**](https://github.com/pytorch/ignite/pull/3591) — typing modernization in `tqdm_logger`
- [**Optuna #6478**](https://github.com/optuna/optuna/pull/6478) — simplified a Union alias under `TYPE_CHECKING`

The other 22 land in the tooling stacks that ship with production AI: React Router, Nuxt, Cloudflare Workers, Sentry, Meta's jscodeshift, MobX, ngrx, and others.

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
