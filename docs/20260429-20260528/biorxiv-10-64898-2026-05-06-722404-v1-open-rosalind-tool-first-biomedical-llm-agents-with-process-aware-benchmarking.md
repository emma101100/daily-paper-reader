---
title: "Open-Rosalind: Tool-First Biomedical LLM Agents with Process-Aware Benchmarking"
title_zh: Open-Rosalind：工具优先的生物医学大语言模型智能体与过程感知基准测试
authors: "Wang, L."
date: 2026-05-08
pdf: "https://www.biorxiv.org/content/10.64898/2026.05.06.722404v1.full.pdf"
tags: ["query:autoresearch"]
score: 9.0
evidence: 以证据接地和追踪完整性为操作原则的智能体系统
tldr: "生物医学领域需要可审计的AI代理，但通用代理的自由度与问责制冲突。提出工具优先的Open-Rosalind系统，并构建过程感知基准BioBench。实验表明，去除工具使准确率下降19.3-26.4个百分点；外部有效性审计后，准确率从17.8%提升到53.3%。该工作强调了外部有效性审计在代理研究中的关键作用。"
source: biorxiv
selection_source: fresh_fetch
motivation: 通用代理的灵活性在生物医学中缺乏问责性，需要可审计的约束来确保可靠输出。
method: 设计工具优先的Open-Rosalind系统，遵循证据输出、轨迹完整、工作流约束和工具中介原则；并构建过程感知基准BioBench。
result: "无工具使任务准确率下降19.3-26.4个百分点；经外部有效性审计修复后，准确率从17.8%提升至53.3%。"
conclusion: 工具优先执行是性能的关键贡献者，但仅靠约束不能保证优越性，外部有效性审计不可或缺。
---

## 摘要
大语言模型越来越被用作科学智能体，然而有利于通用智能体的灵活性可能与生物医学研究所要求的问责性相冲突。我们研究生物医学智能体是否可以围绕可审计的约束而非无约束的自主性来组织。我们提出了Open-Rosalind，一个工具优先的生物智能体系统，围绕四个操作原则设计：基于证据的输出、追踪完整性、工作流约束执行以及事实声明的显式工具中介。为了评估这些原则，我们引入了Open-Rosalind BioBench，一个过程感知的基准测试，它不仅衡量任务准确性，还衡量工具正确性、引文存在性、追踪完整性和失败率。在一个严格的内部基准测试上，参考流水线以完整的执行追踪实现了81.4%的准确性。在多模型消融实验和配对复制中，移除工具会使准确率下降19.3到26.4个百分点，表明工具优先执行是性能最强且最稳定的贡献因素。约束工作流也减少了那些在自由形式工具使用方面较弱的模型的低尾失败。然而，一个独立于作者的30任务保留数据集最初揭示了部署模型上的严重外部效度崩溃。在诊断了五个路由和归一化失败并应用了针对性修复后，保留数据集准确率从17.8%提高到53.3%，并且最令人担忧的与无工具基线的负面比较消失了。这些结果将Open-Rosalind定位为一项具有明确外部效度审计的生物医学智能体研究，而不是声称仅凭协议约束就能保证优越性能。

## Abstract
Large language models are increasingly used as scientific agents, yet the flexibility that benefits general-purpose agents can conflict with the accountability required in biomedical research. We study whether biomedical agents can be organized around auditable constraints rather than unconstrained autonomy. We present Open-Rosalind, a tool-first bio-agent system designed around four operational principles: evidence-grounded outputs, trace completeness, workflow-constrained execution, and explicit tool mediation for factual claims. To evaluate these principles, we introduce Open-Rosalind BioBench, a process-aware benchmark that measures not only task accuracy but also tool correctness, citation presence, trace completeness, and failure rate.

On a strict in-house benchmark, the reference pipeline achieves 81.4% accuracy with complete execution traces. In multi-model ablations and paired replications, removing tools reduces accuracy by 19.3 to 26.4 percentage points, indicating that tool-first execution is the strongest and most stable contributor to performance. Constrained workflows also reduce lower-tail failures for models that are weak at free-form tool use.

However, an author-independent 30-task hold-out initially revealed severe external-validity collapse on the deployment model. After diagnosing five routing and normalization failures and applying targeted fixes, hold-out accuracy improved from 17.8% to 53.3%, and the most concerning negative comparison against a no_tool baseline disappeared. These results position Open-Rosalind as a biomedical-agent study with an explicit external-validity audit, rather than as a claim that protocol constraints alone guarantee superior performance.