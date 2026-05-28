---
title: "NEURA: A proof-carrying framework for hallucination-resistant neuroimaging automation"
title_zh: NEURA：一种抗幻觉神经影像自动化的证明承载框架
authors: "Xie, J., Wang, J., Wu, X., Liu, X., Mi, Y., Liu, Q., Xu, T., Liu, C., Chen, H., Guo, J."
date: 2026-05-21
pdf: "https://www.biorxiv.org/content/10.64898/2026.04.27.721217v2.full.pdf"
tags: ["query:autoresearch"]
score: 8.0
evidence: 证明承载框架确保声明经过工具证据验证
tldr: "神经影像研究依赖异构软件和多模态数据，LLM代理自动化工作流面临幻觉风险。NEURA框架将自由文本研究问题与数据集转化为可执行分析计划，并通过基于形式化证明的验证层确保输出可靠性。在NeuroEval基准上规划准确率达89.5%，较直接LLM查询提升30.5%；幻觉注入实验中验证层检测所有错误类别无假阳性。该工作将LLM驱动的自动化从概率自检转变为可审计的科学计算，提升了神经影像分析的可信度。"
source: biorxiv
selection_source: fresh_fetch
motivation: LLM代理自动化神经影像多阶段统计工作流时易产生幻觉，缺乏可验证性，限制了其在科学研究中的可信度。
method: 结合疾病和工具感知规划与基于形式化证明的验证层，任何声明需通过工具证据和领域公理检查。
result: "在NeuroEval基准(110任务)上规划准确率89.5%，提高30.5%；验证层检测所有注入错误，无假阳性。"
conclusion: 领域接地代理与证明携带验证将LLM自动化从概率自检转变为可审计的科学计算，提升可靠性。
---

## 摘要
神经影像研究依赖于异构软件、多模态数据和多阶段统计工作流。基于大语言模型（LLM）的智能体为自动化这些工作流提供了途径，但其易产生幻觉的特性限制了其在科学应用中的可信度。本文介绍NEURA，一种抗幻觉神经影像自动化的证明承载框架。NEURA将自由文本的研究问题和神经影像数据集转化为可执行的分析计划、验证后的输出和结构化报告。该系统结合了疾病和工具感知的规划以及受形式化证明启发的确定性验证层：在保留任何声明用于报告之前，必须对照工具衍生证据和领域公理进行检查。在NeuroEval（一个由专家整理的包含110项神经影像任务的基准测试）上，NEURA实现了89.5%的规划准确率，比直接LLM查询提升了30.5%。在受控的幻觉注入实验中，验证层在指定的公理库和信任假设下检测到了所有注入的错误类别，且无假阳性。在3型脊髓小脑性共济失调的案例研究中，NEURA重现了与既定病理学和独立专家分析一致的小脑萎缩和异常扩散模式。这些发现共同表明，将领域基础智能体与证明承载验证相结合，可以将LLM驱动的工作流自动化从概率性自我检查转变为可审计的科学计算。

## Abstract
Neuroimaging research depends on heterogeneous software, multimodal data and multistage statistical workflows. Large language model (LLM)-based agents offer a route to automate these workflows, but their susceptibility to hallucination limits their credibility in scientific use. Here we introduce NEURA, a proof-carrying framework for hallucination-resistant neuroimaging automation. NEURA converts free-text research questions and neuroimaging datasets into executable analysis plans, validated outputs and structured reports. The system combines disease- and tool-aware planning with a deterministic verification layer inspired by formal proof: before any claim is retained for reporting, it must be checked against tool-derived evidence and domain axioms. On NeuroEval, an expert-curated benchmark of 110 neuroimaging tasks, NEURA achieved 89.5% planning accuracy, a 30.5% improvement over direct LLM queries. In a controlled hallucination-injection experiment, the verification layer detected all the injected error classes under the specified axiom bank and trust assumptions, with no false positives. In case studies of spinocerebellar ataxia type 3, NEURA reproduced cerebellar atrophy and abnormal diffusion patterns consistent with established pathology and independent expert analyses. Together, these findings show that coupling domain-grounded agency with proof-carrying verification can turn LLM-driven workflow automation from probabilistic self-checking into auditable scientific computation.