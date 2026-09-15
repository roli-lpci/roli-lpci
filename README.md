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

## Evidence in the ecosystem

Hermes Labs has **50+ merged external contributions and ecosystem PRs** across AI
frameworks, agent infrastructure, developer tooling, documentation, integrations, and
public technical systems. The [public contribution
ledger](https://hermes-labs.ai/open-source/contributions) keeps the categories separate;
the underlying record is also available as [machine-readable
JSON](https://hermes-labs.ai/contributions.json).

- **LintLang runs in Character.AI's Larch CI** as an operational lint dependency, documented in [Larch's own linting docs](https://github.com/character-ai/larch/blob/main/docs/linting.md) (scoped to Larch's public repo).
- **LintLang is a catalog plugin in MegaLinter**, merged upstream as [oxsecurity/megalinter#8899](https://github.com/oxsecurity/megalinter/pull/8899) (2026-09-11); a catalog listing, not an install-count claim.
- **Independent Gentoo ebuilds for LintLang** are maintained across releases in the [Haven overlay](https://github.com/thehaven/haven-overlay/commit/d052d950b05389fcd7c8f22939033319a5aec348), packaged without our involvement.
- **zer0dex changed an external team's roadmap**: AllSource [documented](https://github.com/all-source-os/all-source/blob/main/apps/web/content/from-zerodex-to-allsource.mdx) how their architecture moved from zer0dex's pattern to their own system (roadmap influence, not a dependency), and [Mnemosyne](https://github.com/oveku/mnemosyne/pull/3) independently implemented a related approach.
- **Little Canary's technique was adapted** in [Preflight](https://github.com/DavidMChan/preflight/commit/186ce43c1ce122aba82c1904e777517834d1bc90) with attribution, and named as the closest prior work in [ProxyCanary's manuscript](https://github.com/JucieOvo/ProxyCanary/blob/master/docs/paper_en.md) (a repository-hosted manuscript citation, not peer review).
- **Hermes Rubric is listed in Inspect AI's extensions gallery** (accepted upstream docs PR, [UKGovernmentBEIS/inspect_ai#5265](https://github.com/UKGovernmentBEIS/inspect_ai/pull/5265), merged 2026-09-09).
- **A CISA Vulnrichment score correction**: CVE-2026-14216 was stored at CVSS 5.3 against a 6.5 vector; a collaborator confirmed the correction and republication in [cisagov/vulnrichment#333](https://github.com/cisagov/vulnrichment/issues/333) ([case study](https://hermes-labs.ai/case-studies/cisa-vulnrichment-score-consistency)). A scoring correction, not a vulnerability discovery, partnership, or endorsement.

---

## Upstream engineering

Merged fixes in AI frameworks and agent infrastructure, each with a regression test:
[Microsoft Semantic Kernel
#13610](https://github.com/microsoft/semantic-kernel/pull/13610) (a chat-history
truncation reducer was silently deleting the system prompt), [LangChain
#35544](https://github.com/langchain-ai/langchain/pull/35544) (dropped a forced
tool_choice that crashed Anthropic extended-thinking requests), [DSPy
#9978](https://github.com/stanfordnlp/dspy/pull/9978) (an empty eval devset failed with
a bare ZeroDivisionError instead of a descriptive one), [crewAI
#7369](https://github.com/crewAIInc/crewAI/pull/7369) (memory access times were updated
even when a read was marked read_only; merged 2026-09-15), and [Hindsight
#4285](https://github.com/vectorize-io/hindsight/pull/4285) (added task-local retain
suspension to the Python client; merged 2026-09-15). A related [Mem0
patch](https://github.com/mem0ai/mem0/pull/5250) fixing a Redis
cosine-distance-to-similarity conversion closed unmerged after a maintainer acknowledged
the conversion in a broader sweep. It is not a merged contribution.

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
