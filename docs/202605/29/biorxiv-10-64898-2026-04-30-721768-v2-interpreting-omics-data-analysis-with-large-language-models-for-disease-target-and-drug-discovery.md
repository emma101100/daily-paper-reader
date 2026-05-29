---
title: Interpreting Omics Data Analysis with Large Language Models for Disease Target and Drug Discovery
title_zh: 用大型语言模型解释组学数据分析以发现疾病靶点和药物
authors: "XU, Z., Chen, W., Ren, W., Xu, T., Amaechin, S., Khan, R., Chen, Y., Province, M., Payne, P., Li, F."
date: 2026-05-23
pdf: "https://www.biorxiv.org/content/10.64898/2026.04.30.721768v2.full.pdf"
tags: ["query:autoresearch"]
score: 6.0
evidence: 提出一个溯源感知的 Text-to-Target 框架，耦合 LLM 检索与组学数据分析
tldr: 论文提出了一种溯源感知的 Text-to-Target 框架，通过将模式约束的多模型 LLM 检索与数值组学数据分析相耦合，解决了纯文本 LLM 输出在药物靶点发现中缺乏定量证据可靠性的问题。其关键设计是模态感知融合步骤，将候选物划分为重叠支撑锚点、纯检索隐藏枢纽等，从而增强结论的证据基础。该方法为多模态 AI 驱动的生物医学发现提供了更可靠的决策支持。
source: biorxiv
selection_source: fresh_fetch
motivation: 提出一个溯源感知的 Text-to-Target 框架，耦合 LLM 检索与组学数据分析。
method: 方法与实现细节请参考摘要与正文。
result: 结果与对比结论请参考摘要与正文。
conclusion: 总体而言，该工作在所述任务上展示了有效性，并提供了可复用的思路或工具。
---

## 摘要
在生物医学科学发现中，从文献中综合先验知识是解释数值组学数据分析以识别疾病靶点和发现药物的重要组成部分。单独使用大型语言模型可以快速从生物医学文本中检索疾病机制，但仅文本输出是笼统的，并且在没有队列特异性定量证据的情况下，对于靶点和药物的优先级排序并不可靠。本文中，我们提出了一个来源感知的文本到靶点框架，该框架将模式约束的多模型 LLM 检索与数值组学数据分析相结合。其关键设计是一个模态感知融合步骤：候选物被划分为重叠支持的锚点、仅检索的隐藏枢纽和网络涌现的新颖节点，然后在拓扑约束下传播到分阶段的假设和策略生成中。我们评估了该模型在阿尔茨海默病和胰腺导管腺癌中的表现。在胰腺导管腺癌中，该工作流程产生了一个平衡的 75 基因候选集合和一个包含 23 个策略的组合，在靶点水平和策略水平上都得到了显著的 DepMap 支持。在阿尔茨海默病中，更严格的候选控制产生了一个紧凑的 34 基因集合和 14 个策略；在扩展的 CRISPRbrain 注册表下，两个靶点水平轴都显著，并且策略水平富集很强。在这两种疾病中，最终策略都保留了到候选池的完整来源闭合，从而能够实现从检索工件到验证输出的端到端可审计性。这些结果支持一种可迁移的发现架构，其中组学证据约束生物活性，LLM 检索扩展机制搜索空间，网络感知融合保持可解释性。该框架为双疾病靶点优先级排序提供了可重复的基础，并通过代理证据刷新循环激发了持续的文献-机制一致性。

## Abstract
In biomedical scientific discovery, synthesizing prior knowledge from the literature is an essential component of interpreting numerical omics data analyses for disease target identification and drug discovery. Large language models (LLMs) alone can rapidly retrieve disease mechanisms from biomedical text, but text-only outputs are general and unreliable for target and drug prioritization without cohort-specific quantitative evidence. Herein, we propose a provenance-aware Text-to-Target framework that couples schema-constrained multi-model LLM retrieval with numeric omics data analysis. The key design is a modality-aware fusion step: candidates are partitioned into overlap-supported anchors, retrieval-only hidden hubs, and network-emergent novelty nodes, then propagated into staged hypothesis and strategy generation under topology constraints. We evaluate the model in Alzheimers disease (AD) and pancreatic ductal adenocarcinoma (PDAC). In PDAC, the workflow produced a balanced 75-gene candidate universe and a 23-strategy portfolio, with significant DepMap support at both target level and strategy level. In AD, stricter candidate controls yielded a compact 34-gene universe and 14 strategies; under an expanded CRISPRbrain registry, both target-level axes were significant, with strong strategy-level enrichment. Across both diseases, final strategies preserved full provenance closure to the candidate pool, enabling end-to-end auditability from retrieval artifacts to validation outputs. These results support a transferable discovery architecture in which omics evidence constrains biological activity, LLM retrieval expands mechanistic search space, and network-aware fusion preserves interpretability. The framework provides a reproducible basis for dual-disease target prioritization and motivates continuous literature-mechanism concordance with agentic evidence-refresh loops.