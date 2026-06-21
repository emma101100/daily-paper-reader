---
title: "FlowBench: separating planning, fault recovery and interpretation in agentic bioinformatics"
authors: "Kurjan, A., Cribbs, A. P."
date: 2026-06-16
pdf: "https://www.biorxiv.org/content/10.64898/2026.06.12.731844v1.full.pdf"
tags: ["query:autoresearch"]
score: 9.0
evidence: 提出FlowBench，用于评估生物信息学中智能体LLM系统的规划、故障恢复和解释能力，与自主科研智能体直接相关
tldr: 为区分智能体LLM系统在生物信息学中的不同能力维度，FlowBench将端到端性能分解为规划、故障恢复、生物学解释和输出保真度，并提供模块化FlowAgent框架支持骨架与模型分离评估，揭示了现有系统规划完整性高但故障恢复和解释能力不足的问题，为自主科研智能体的精细诊断打下了基准基础。
source: biorxiv
selection_source: fresh_fetch
motivation: 提出FlowBench，用于评估生物信息学中智能体LLM系统的规划、故障恢复和解释能力，与自主科研智能体直接相关。
method: 方法与实现细节请参考摘要与正文。
result: 结果与对比结论请参考摘要与正文。
conclusion: 总体而言，该工作在所述任务上展示了有效性，并提供了可复用的思路或工具。
---

## Abstract
AO_SCPLOWBSTRACTC_SCPLOWAgentic large language model (LLM) systems are being deployed in bioinformatics faster than they are understood, and single-metric evaluations conflate capabilities that fail independently. We introduce FlowBench, a benchmark that decomposes agentic bioinformatics performance into planning, fault recovery, biological interpretation, and end-to-end output-fidelity. Existing systems achieve high plan completeness, but their closed, single-provider designs prevent attribution of performance to scaffolding versus the underlying model. We therefore built FlowAgent, a modular, provider-agnostic framework whose components can be selectively disabled and whose backbone model can be swapped across providers on a shared harness, and used it to evaluate 23 models from three main providers. Three findings emerge. First, generating a valid workflow plan from a named toolchain is largely solved, whereas inferring an appropriate toolchain from biological intent alone is uniformly difficult regardless of model tier, compressing all models into a narrow 44-57% pass-rate band. Second, ablation shows that the dependency-structured plan and a completeness-reflection step drive performance, while adding a same-context validator-driven retry makes structural quality worse. Third, fault recovery and data-grounded interpretation remain unsolved. Models frequently propose fixes that force a clean exit while leaving the underlying data invalid, and data-grounded interpretation lags internal-knowledge recall by a consistent margin. Safety does not emerge from capability, and reasoning-tier models were among the least reliable at recognising unrecoverable faults. Once planning saturates, agent architecture and refusal calibration, not model scale, are the productive frontier.

Availability and implementationFlowAgent and FlowBench are available under a GPLv3 licence at https://github.com/EnteloBio/flowagent

Contactadam@entelo.bio