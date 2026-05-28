---
title: "OmniCellAgent: An AI Scientist for Omic-Driven Scientific Discovery"
title_zh: OmniCellAgent：一款用于组学驱动科学发现的AI科学家
authors: "Huang, D., Li, H., Li, W., Zhang, H., Xu, T., Lu, Y., Fang, K., Xu, Z., Chen, J., Dickson, P., Sardiello, M., Buchser, W., Cooper, J. D., Cruchaga, C., Eghtesady, P., Li, G., Goedegebuure, P., DeNardo, D., Ding, L., Fields, R. C., Zhan, M., Miller, J. P., Province, M., Chen, Y., Payne, P., Li, F."
date: 2026-05-20
pdf: "https://www.biorxiv.org/content/10.1101/2025.07.31.667797v2.full.pdf"
tags: ["query:autoresearch"]
score: 9.0
evidence: 多智能体AI科学家自主检索和分析组学数据
tldr: 生物医学发现中，识别相关组学数据集并利用先验知识解释结果至关重要，但现有AI代理需用户手动预定义疾病数据集，耗时且对非计算研究者困难。OmniCellAgent多智能体AI框架基于大规模单细胞RNA测序资源，自动检索、整合并分析疾病与对照样本的多种细胞类型数据，结合先验知识代理进行靶点注释，领域专家代理进行下游解释。在多疾病评估中，它能识别相关数据集、优先排序生物学意义靶点并生成证据支持假设。该工作表明多智能体AI系统可降低组学驱动发现门槛，加速精准医学假设生成。
source: biorxiv
selection_source: fresh_fetch
motivation: 解决用户需手动预定义疾病数据集的问题，降低非计算研究人员利用组学数据进行科学发现的障碍。
method: 构建多智能体AI框架OmniCellAgent，自动检索整合scRNA-seq数据，包含先验知识代理和领域专家代理进行靶点注释与下游解释。
result: 在多疾病设置中评估，能识别相关数据集、优先排序有意义的靶点并生成全面、证据支持的假设。
conclusion: 多智能体AI系统可降低组学驱动发现障碍，加速精准医学中的假设生成。
---

## 摘要
在生物医学科学发现中，利用数据库和文献中的先验知识来识别相关组学数据集并解释分析结果，对于产生新假设至关重要。尽管最近的AI代理支持自动化的组学分析和文献检索，但它们通常需要用户预定义和整理疾病特定数据集，这一过程对于非计算研究人员而言仍然具有挑战性且耗时。在此，我们提出OmniCellAgent，一个基于大规模单细胞RNA测序（scRNA-seq）资源构建的多智能体AI框架，能够自主检索、整合和分析跨组织和条件下不同细胞类型的疾病与对照相关数据集。此外，OmniCellAgent整合了一个生物医学先验知识智能体，用于使用精选数据库和文献进行系统靶标注释，以及用于下游高优先级靶标解释的领域特定专家智能体。通过汇总各智能体的证据，该框架生成结构化的分析报告和数据驱动的假设。我们在多种疾病背景下评估OmniCellAgent，展示了其识别相关数据集、优先考虑生物学上有意义的靶标以及生成全面且证据支持的假设的能力。我们的结果表明，多智能体AI系统可以降低组学驱动发现的障碍，并加速精准医学中的假设生成。源代码公开于：https://github.com/FuhaiLiAiLab/OmniCellAgent。

## Abstract
In biomedical scientific discovery, identifying relevant omics datasets and interpreting analysis results using prior knowledge from databases and literature are essential for generating novel hypotheses. Although recent AI agents support automated omics analysis and literature retrieval, they typically require users to predefine and curate disease-specific datasets, which is a process that remains challenging and time-consuming, particularly for non-computational researchers. Herein we present OmniCellAgent, a multi-agent AI framework built on large-scale single-cell RNA sequencing (scRNA-seq) resources that autonomously retrieves, integrates and analyzes disease and control-related datasets of diverse cell types across tissues and conditions. Moreover, OmniCellAgent incorporates a biomedical prior knowledge agent for systematic target annotation using curated databases and literature, as well as domain-specific expert agents for downstream interpretation of high-priority targets. By aggregating evidence across agents, the framework generates structured analytical reports and data-driven hypotheses. We evaluate OmniCellAgent across multiple disease settings, demonstrating its ability to identify relevant datasets, prioritize biologically meaningful targets and produce comprehensive, evidence-supported hypotheses. Our results suggest that multi-agent AI systems can reduce barriers to omics-driven discovery and accelerate hypothesis generation in precision medicine. The source code is publicly available at: https://github.com/FuhaiLiAiLab/OmniCellAgent.