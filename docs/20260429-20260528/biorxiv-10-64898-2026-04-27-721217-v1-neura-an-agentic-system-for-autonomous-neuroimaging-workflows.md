---
title: "NEURA: An agentic system for autonomous neuroimaging workflows"
title_zh: NEURA：用于自主神经影像工作流的智能体系统
authors: "Xie, J., Wang, J., Wu, X., Liu, X., Mi, Y., Liu, Q., Xu, T., Liu, C., Chen, H., Guo, J."
date: 2026-04-30
pdf: "https://www.biorxiv.org/content/10.64898/2026.04.27.721217v1.full.pdf"
tags: ["query:autoresearch"]
score: 8.0
evidence: 用于自主科学工作流的代理系统，具备声明验证
tldr: "现有LLM代理在神经影像分析中易产生幻觉，缺少可信度。NEURA通过集成形式化证明风格的验证层，将自然语言研究问题转换为可执行计划，在110个任务上达到89.5%规划准确率，比直接LLM查询提升30.5%。实验表明验证层能检测所有注入错误且无假阳性。案例研究再现了小脑萎缩等已知病理模式。"
source: biorxiv
selection_source: fresh_fetch
motivation: LLM代理在自动化神经影像工作流时易产生幻觉，缺乏可信和可审计的计算。
method: 提出NEURA框架，结合领域感知规划与基于形式化证明的确定性验证层，确保结果经过工具证据和领域公理检查。
result: "在NeuroEval基准上规划准确率89.5%，提升30.5%；验证层在注入实验中100%检测错误且无假阳性。"
conclusion: 耦合领域代理与证明承载验证可将LLM驱动的自动化转化为可审计的科学计算，提升可信度。
---

## 摘要
神经影像学研究依赖于异构软件、多模态数据和多阶段统计工作流。基于大语言模型（LLM）的智能体提供了一条自动化这些工作流的途径，但其容易产生幻觉的倾向限制了其在科学使用中的可信度。在此，我们介绍NEURA，一个用于抗幻觉神经影像自动化的证明携带框架。NEURA将自由文本研究问题和神经影像数据集转换为可执行的分析计划、验证输出和结构化报告。该系统结合了疾病和工具感知的规划以及受形式化证明启发的确定性验证层：在将任何主张保留用于报告之前，必须对照工具衍生的证据和领域公理进行检查。在NeuroEval（一个由专家策划的110个神经影像任务基准）上，NEURA达到了89.5%的规划准确率，比直接LLM查询提高了30.5%。在一个受控的幻觉注入实验中，验证层在指定的公理库和信任假设下检测到了所有注入的错误类别，且没有误报。在3型脊髓小脑性共济失调的案例研究中，NEURA重现了与已建立的病理学和独立专家分析一致的小脑萎缩和异常扩散模式。这些发现共同表明，将领域驱动的智能体与证明携带验证相结合，可以将LLM驱动的工作流自动化从概率性自我检查转变为可审计的科学计算。

## Abstract
Neuroimaging research depends on heterogeneous software, multimodal data and multistage statistical workflows. Large language model (LLM)-based agents offer a route to automate these workflows, but their susceptibility to hallucination limits their credibility in scientific use. Here we introduce NEURA, a proof-carrying framework for hallucination-resistant neuroimaging automation. NEURA converts free-text research questions and neuroimaging datasets into executable analysis plans, validated outputs and structured reports. The system combines disease- and tool-aware planning with a deterministic verification layer inspired by formal proof: before any claim is retained for reporting, it must be checked against tool-derived evidence and domain axioms. On NeuroEval, an expert-curated benchmark of 110 neuroimaging tasks, NEURA achieved 89.5% planning accuracy, a 30.5% improvement over direct LLM queries. In a controlled hallucination-injection experiment, the verification layer detected all the injected error classes under the specified axiom bank and trust assumptions, with no false positives. In case studies of spinocerebellar ataxia type 3, NEURA reproduced cerebellar atrophy and abnormal diffusion patterns consistent with established pathology and independent expert analyses. Together, these findings show that coupling domain-grounded agency with proof-carrying verification can turn LLM-driven workflow automation from probabilistic self-checking into auditable scientific computation.