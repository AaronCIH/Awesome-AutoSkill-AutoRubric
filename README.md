# Awesome AutoSkill & AutoRubric & Harness Evolution [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

A curated collection of papers and repositories on **Auto-Skill** (self-evolving agent strategies), **Auto-Rubric** (automated rubric discovery from preference data), and **Harness Evolution** (automatic evolution of agent harnesses — prompts, tools, memory, and orchestration logic). Contributions welcome!

---

## Table of Contents

- [Auto-Skill: Self-Evolving Agent Strategies](#auto-skill-self-evolving-agent-strategies)
  - [Skill Learning & Evolution](#skill-learning--evolution)
  - [Benchmarks & Evaluation](#benchmarks--evaluation)
- [Auto-Rubric: Automated Rubric Discovery from Preferences](#auto-rubric-automated-rubric-discovery-from-preferences)
  - [Rubric Learning from Preference Data](#rubric-learning-from-preference-data)
  - [Rubric-Guided RL & Reward Modeling](#rubric-guided-rl--reward-modeling)
  - [Rubric-Based Evaluation & Judges](#rubric-based-evaluation--judges)
- [Harness Evolution: Automatic Agent Harness Engineering](#harness-evolution-automatic-agent-harness-engineering)
  - [Harness Evolution Methods](#harness-evolution-methods)
  - [Harness Engineering Foundations](#harness-engineering-foundations)
  - [Harness Surveys](#harness-surveys)
- [Contributing](#contributing)
- [License](#license)

---

## Auto-Skill: Self-Evolving Agent Strategies

Research on enabling LLM-based agents to autonomously create, evolve, and reuse skills from experience, achieving self-improvement without human intervention.

### Skill Learning & Evolution

| Name | Date | Paper | Repo | TL;DR |
|------|------|-------|------|-------|
| **Skill-Pro** | Feb 2026 | [arXiv:2602.01869](https://arxiv.org/abs/2602.01869) | - | Agents autonomously learn reusable procedural skills from interaction via Non-Parametric PPO — formalizes a Skill-MDP with activation/execution/termination conditions and a PPO Gate for robust skill verification. **ICML 2026 Spotlight.** |
| **SkillFlow (Flow-Driven)** | May 2026 | [arXiv:2605.14089](https://arxiv.org/abs/2605.14089) | [Code](https://anonymous.4open.science/r/SkillFlow-E850) | Flow-based framework using Tempered Trajectory Balance for agentic orchestration — enables recursive skill evolution with transparent per-step credit assignment, outperforming baselines on 14 datasets. |
| **Harnessing Agentic Evolution (AEvo)** | May 2026 | [arXiv:2605.13821](https://arxiv.org/abs/2605.13821) | - | Meta-editing framework where a meta-agent observes accumulated evolution context and edits the procedure/agent context that controls future evolution — 26% relative improvement over strongest baseline. |
| **Harnessing LLM Agents with Skill Programs** | May 2026 | [arXiv:2605.17734](https://arxiv.org/abs/2605.17734) | - | Encodes reusable skills as executable programs with explicit intervention mechanisms, moving beyond advisory textual guidance for more reliable agent skill reuse. |
| **MOSS** | May 2026 | [arXiv:2605.22794](https://arxiv.org/abs/2605.22794) | [Code](https://github.com/hkgai-official/Moss) | Self-evolution through source-level rewriting — autonomous agents modify their own runtime code to learn from interactions and fix recurring failures. |
| **Trace2Skill** | May 2026 | [arXiv:2605.21810](https://arxiv.org/abs/2605.21810) | - | Verifier-guided skill evolution for EDA agents — distills long verification traces into reusable skills for hardware design tasks. |
| **MUSE-AutoSkill** | May 2026 | [arXiv:2605.27366](https://arxiv.org/abs/2605.27366) | - | Skill-centric agent framework with a unified skill lifecycle (creation, memory, management, evaluation, refinement) — introduces skill-level memory that accumulates experience across tasks for better reuse and cross-agent transfer. |
| **SkillMAS** | May 2026 | [arXiv:2605.09341](https://arxiv.org/abs/2605.09341) | - | Skill co-evolution with multi-agent systems — jointly evolves skills and agent coordination strategies, coupling two adaptation targets that are typically decoupled. |
| **SkillFlow (Retrieval)** | Apr 2025 | [arXiv:2504.06188](https://arxiv.org/abs/2504.06188) | - | First multi-stage retrieval pipeline for agent skill discovery — frames skill acquisition as an information retrieval problem over ~36K community-contributed skill definitions from GitHub. |

### Benchmarks & Evaluation

| Name | Date | Paper | Repo | TL;DR |
|------|------|-------|------|-------|
| **SkillFlow (Benchmark)** | Apr 2026 | [arXiv:2604.17308](https://arxiv.org/abs/2604.17308) | - | Benchmark of 166 tasks across 20 families for lifelong skill discovery and evolution — evaluates whether agents can discover skills, repair them, and maintain coherent libraries over time. |
| **SkillEvolBench** | May 2026 | [arXiv:2605.24117](https://arxiv.org/abs/2605.24117) | - | Diagnostic benchmark for evaluating the step from experience reuse to skill formation — 180 tasks across 6 real-world domains testing whether episodic trajectories can be distilled into reusable procedural skills. |

---

## Auto-Rubric: Automated Rubric Discovery from Preferences

Research on automatically discovering and learning evaluation rubrics from preference-pair data, enabling interpretable, customizable reward signals for LLM alignment.

### Rubric Learning from Preference Data

| Name | Date | Paper | Repo | TL;DR |
|------|------|-------|------|-------|
| **Online Rubrics Elicitation** | Oct 2025 | [arXiv:2510.07284](https://arxiv.org/abs/2510.07284) | - | Online elicitation of rubrics from pairwise comparisons — iteratively discovers evaluation criteria through preference data. |
| **Auto-Rubric** | Oct 2025 | [arXiv:2510.17314](https://arxiv.org/abs/2510.17314) | - | Paradigm shift from implicit to explicit reward parameterization — iteratively induces discriminative criteria via verification-driven refinement and compresses them into hierarchical rubric structures. With only 70 preference pairs, outperforms fully trained reward models on RewardBench2. |
| **Alternating RL for Rubric-Based Reward** | Feb 2026 | [arXiv:2602.01511](https://arxiv.org/abs/2602.01511) | - | Proposes alternating reinforcement learning that generates rubric-based multi-dimensional reward signals, capturing fine-grained quality aspects beyond scalar scores in non-verifiable domains. |
| **Rethinking Rubric Generation** | Feb 2026 | [arXiv:2602.05125](https://arxiv.org/abs/2602.05125) | - | Rethinks rubric generation for improving LLM judges and reward modeling for open-ended tasks, analyzing when and how rubrics improve alignment. |
| **Learning Query-Specific Rubrics** | Feb 2026 | [arXiv:2602.03619](https://arxiv.org/abs/2602.03619) | - | Learns query-specific rubrics from human preferences for DeepResearch report generation — addresses the lack of verifiable reward signals for long-form research outputs. |
| **Open Rubric System** | Feb 2026 | [arXiv:2602.14069](https://arxiv.org/abs/2602.14069) | - | Scales reinforcement learning with pairwise adaptive rubrics — addresses the limitation of scalar reward models that compress multi-dimensional preferences. |
| **SibylSense** | Feb 2026 | [arXiv:2602.20751](https://arxiv.org/abs/2602.20751) | - | Inference-time adaptive rubric learning via memory tuning and adversarial probing — adapts a frozen rubric generator through a tunable memory bank, alternating with rubric-adversarial policy updates. |
| **CDRRM** | Mar 2026 | [arXiv:2603.08035](https://arxiv.org/abs/2603.08035) | - | Contrast-driven rubric generation for reliable and interpretable reward modeling — generates rubrics by contrasting preferred and dispreferred responses. |
| **Rationale Matters** | Mar 2026 | [arXiv:2603.16600](https://arxiv.org/abs/2603.16600) | - | Learning transferable rubrics via proxy-guided critique for VLM reward models — improves vision-language evaluation through structured rubric learning. |
| **Auto-Rubric as Reward (ARR)** | May 2026 | [arXiv:2605.08354](https://arxiv.org/abs/2605.08354) | - | Externalizes VLM's internalized preference knowledge as prompt-specific rubrics for multimodal generative models — introduces Rubric Policy Optimization (RPO) for stable alignment training. |
| **RUBRIC-ARROW** | May 2026 | [arXiv:2605.29156](https://arxiv.org/abs/2605.29156) | - | Alternating pointwise rubric reward modeling for LLM post-training in non-verifiable domains — advances rubric-based reward signals for open-ended generation. |

### Rubric-Guided RL & Reward Modeling

| Name | Date | Paper | Repo | TL;DR |
|------|------|-------|------|-------|
| **CARMO** | Oct 2024 | [arXiv:2410.21545](https://arxiv.org/abs/2410.21545) | - | Dynamic criteria generation for context-aware reward modelling — generates task-specific criteria on-the-fly rather than using fixed rubrics. |
| **AdaRubric** | Mar 2026 | [arXiv:2603.21362](https://arxiv.org/abs/2603.21362) | - | Task-adaptive rubrics for reliable LLM agent evaluation and reward learning — automatically generates domain-specific evaluation criteria. **KnowFM @ ACL 2026.** |
| **ProMedical** | Apr 2026 | [arXiv:2604.08326](https://arxiv.org/abs/2604.08326) | - | Hierarchical fine-grained criteria modeling for medical LLM alignment via explicit injection — adapts rubric learning for high-stakes medical domains. **ACL 2026.** |
| **RewardHarness** | May 2026 | [arXiv:2605.08703](https://arxiv.org/abs/2605.08703) | [Project](https://rewardharness.com/) | Self-evolving agentic reward framework that reframes reward modeling as context evolution — iteratively evolves a library of tools and skills from as few as 100 preference demos, surpassing GPT-5 by 5.3 points on image-editing evaluation using only 0.05% of preference data. |
| **RubricEM** | May 2026 | [arXiv:2605.10899](https://arxiv.org/abs/2605.10899) | - | Rubric-guided RL framework combining stagewise policy decomposition with reflection-based meta-policy evolution for deep research agents — rubrics serve as the shared interface for policy execution, judge feedback, and agent memory. |

### Rubric-Based Evaluation & Judges

| Name | Date | Paper | Repo | TL;DR |
|------|------|-------|------|-------|
| **Prometheus** | Oct 2023 | [arXiv:2310.08491](https://arxiv.org/abs/2310.08491) | - | Inducing fine-grained evaluation capability in language models using rubric-based evaluation — a foundational work for rubric-guided LLM judges. **ICLR 2024.** |

---

## Harness Evolution: Automatic Agent Harness Engineering

Research on automatically evolving agent harnesses — the runtime substrate of prompts, tools, memory, orchestration logic, and verification that surrounds a frozen LLM and determines its effectiveness. Instead of changing model weights, harness evolution optimizes everything *around* the model.

### Harness Evolution Methods

| Name | Date | Paper | Repo | TL;DR |
|------|------|-------|------|-------|
| **Meta-Harness** | Mar 2026 | [arXiv:2603.28052](https://arxiv.org/abs/2603.28052) | - | Outer-loop system that searches over harness code using an agentic proposer with access to source code, scores, and execution traces — improves over SOTA context management by 7.7 points and surpasses hand-engineered baselines on TerminalBench-2. |
| **The Last Harness You'll Ever Build** | Apr 2026 | [arXiv:2604.21003](https://arxiv.org/abs/2604.21003) | - | Two-level framework: a Harness Evolution Loop optimizes worker agent harnesses per-task, and a Meta-Evolution Loop learns a universal blueprint that enables rapid harness convergence on any new task with zero human engineering. |
| **Agentic Harness Engineering (AHE)** | Apr 2026 | [arXiv:2604.25850](https://arxiv.org/abs/2604.25850) | - | Closed-loop observability-driven harness evolution with three pillars: component, experience, and decision observability — lifts pass@1 on Terminal-Bench 2 from 69.7% to 77.0%, surpassing human-designed Codex-CLI and self-evolving baselines. |
| **DemoEvolve** | May 2026 | [arXiv:2605.24539](https://arxiv.org/abs/2605.24539) | - | Overcomes sparse feedback in agentic harness evolution by leveraging demonstrations to bootstrap the evolution process. |
| **FlashEvolve** | May 2026 | [arXiv:2605.08520](https://arxiv.org/abs/2605.08520) | - | Accelerates agent self-evolution with asynchronous stage orchestration, enabling faster harness/skill evolution through parallelized LLM-based pipelines. |
| **Harness Updating ≠ Harness Benefit** | May 2026 | [arXiv:2605.30621](https://arxiv.org/abs/2605.30621) | - | Diagnostic study disentangling evolution capabilities — shows harness updating does not always improve performance, identifying when and why self-evolution succeeds or fails. |
| **HarnessFix** | Jun 2026 | [arXiv:2606.06324](https://arxiv.org/abs/2606.06324) | - | Trace-guided framework for diagnosing agent failures and repairing harnesses — compiles traces into Harness-aware Trace IR, attributes failures to specific harness layers, and generates validated patches. Improves held-out performance by 15.2%–50.0% over initial harnesses. |

### Harness Engineering Foundations

| Name | Date | Paper | Repo | TL;DR |
|------|------|-------|------|-------|
| **AI Harness Engineering** | May 2026 | [arXiv:2605.13357](https://arxiv.org/abs/2605.13357) | - | Formalizes the agent harness as a runtime substrate with 11 component responsibilities and a four-level capability ladder (H0–H3) — reframes the question from "can the model produce a patch" to "can the system produce a verifiable change." |
| **Workspace Optimization** | May 2026 | [arXiv:2605.09650](https://arxiv.org/abs/2605.09650) | - | "How to Train Your Agent" — argues the trainable component in modern agents is not model weights but the workspace/harness around them. |

### Harness Surveys

| Name | Date | Paper | Repo | TL;DR |
|------|------|-------|------|-------|
| **Code as Agent Harness** | May 2026 | [arXiv:2605.18747](https://arxiv.org/abs/2605.18747) | [GitHub](https://github.com/YennNing/Awesome-Code-as-Agent-Harness-Papers) | Comprehensive survey on code as the operational substrate for agent reasoning, acting, and verification — covers harness interface, mechanisms (planning, memory, tools), and scaling to multi-agent systems. |
| **Externalization in LLM Agents** | Apr 2026 | [arXiv:2604.08224](https://arxiv.org/abs/2604.08224) | - | Unified review of memory, skills, protocols and harness engineering — 54-page tech report on how capabilities are externalized from model weights to runtime components. |

---

## Related Topics

### Self-Evolving Agent Systems (Broader)

| Name | Date | Paper | Repo | TL;DR |
|------|------|-------|------|-------|
| **EvoMaster** | Apr 2026 | [arXiv:2604.17406](https://arxiv.org/abs/2604.17406) | - | Foundational evolving agent framework for agentic science at scale — combines LLMs with evolutionary strategies for scientific discovery. |
| **Memory Transfer Learning** | Apr 2026 | [arXiv:2604.14004](https://arxiv.org/abs/2604.14004) | - | Studies how memories are transferred across domains in coding agents — analyzes cross-domain memory-based self-evolution. |
| **M★** | Apr 2026 | [arXiv:2604.11811](https://arxiv.org/abs/2604.11811) | [Code](https://github.com/wbopan/mstar) | Every task deserves its own memory harness — proposes task-adaptive memory systems instead of fixed memory designs, optimizing memory structure for each domain. |

---

## Contributing

Contributions are welcome! Please follow these steps:

1. Fork this repository
2. Add your paper/repo to the appropriate section in the table
3. Follow the existing format: **Name** | Date | Paper Link | Repo Link | TL;DR
4. Submit a Pull Request

### Guidelines

- Papers should be related to **Auto-Skill** (self-evolving agent skills), **Auto-Rubric** (automated rubric learning from preferences), or **Harness Evolution** (automatic agent harness engineering)
- Include the arXiv link (or conference link if published)
- Include the GitHub repo link if available (use `-` if not)
- Write a concise TL;DR (1-2 sentences)
- Sort entries chronologically within each section

---

## Star History

If you find this collection useful, please consider giving it a star!

---

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

## Citation

If you find this resource helpful, please cite:

```bibtex
@misc{awesome-autoskill-autorubric,
  title={Awesome AutoSkill \& AutoRubric \& Harness Evolution},
  author={IHChen},
  year={2026},
  url={https://github.com/IHChen/Awesome-AutoSkill-AutoRubric}
}
```
