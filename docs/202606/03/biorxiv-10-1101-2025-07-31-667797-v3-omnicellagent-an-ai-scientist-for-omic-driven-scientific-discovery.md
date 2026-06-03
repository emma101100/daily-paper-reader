---
title: "OmniCellAgent: An AI Scientist for Omic-Driven Scientific Discovery"
title_zh: OmniCellAgent：面向组学驱动科学发现的人工智能科学家
authors: "Huang, D., Li, H., Li, W., Zhang, H., Xu, T., Lu, Y., Fang, K., Xu, Z., Chen, J., Dickson, P., Sardiello, M., Buchser, W., Cooper, J. D., Cruchaga, C., Eghtesady, P., Li, G., Goedegebuure, P., DeNardo, D., Ding, L., Fields, R. C., Zhan, M., Miller, J. P., Province, M., Chen, Y., Payne, P., Li, F."
date: 2026-06-02
pdf: "https://www.biorxiv.org/content/10.1101/2025.07.31.667797v3.full.pdf"
tags: ["query:autoresearch"]
score: 9.0
evidence: 多智能体AI框架，用于自主组学驱动的科学发现，整合数据检索、分析和假设生成。
tldr: 在生物医学科学发现中，非计算研究人员难以高效识别和整合组学数据集并解释分析结果。OmniCellAgent 是一个多智能体 AI 框架，基于大规模单细胞转录组资源，自动检索、整合疾病与对照数据，并通过先验知识和领域专家代理进行靶标解释。评估表明，它可识别相关数据集，优先排序有意义的靶点，生成证据支持的结构化报告。该框架降低了组学驱动发现的门槛，加速了精准医学假设生成。
source: biorxiv
selection_source: fresh_fetch
motivation: 非计算研究人员在组学驱动的科学发现中，难以高效检索、整合数据并解释分析结果。
method: OmniCellAgent 多智能体框架基于大规模单细胞RNA测序，自动检索整合疾病对照数据，并利用先验知识与专家代理进行靶标注释和解释。
result: 在多个疾病场景中，该框架成功识别相关数据集，优先排序生物学有意义的靶点，并生成证据支持的假设与报告。
conclusion: OmniCellAgent 降低了组学驱动科学发现的门槛，可加速精准医学的假设生成。
---

## 摘要
在生物医学科学发现中，识别相关的组学数据集并利用数据库和文献中的先验知识解释分析结果，对于产生新假设至关重要。尽管近期的人工智能代理支持自动化组学分析和文献检索，但它们通常要求用户预定义和筛选特定疾病的数据集，这一过程对非计算研究人员而言尤其耗时且具有挑战性。本文介绍 OmniCellAgent，一个基于大规模单细胞 RNA 测序（scRNA-seq）资源构建的多代理人工智能框架，可自主检索、整合并分析不同组织与条件下多种细胞类型的疾病及对照相关数据集。此外，OmniCellAgent 整合了一个生物医学先验知识代理，利用精选数据库和文献进行系统化靶点注释，以及领域特定的专家代理用于高优先级靶点的下游解读。通过聚合各代理的证据，该框架生成结构化的分析报告和数据驱动的假设。我们在多种疾病场景下评估了 OmniCellAgent，证明其能够识别相关数据集、优先排序具有生物学意义的靶点，并生成全面的、有证据支持的假设。结果表明，多代理人工智能系统可以降低组学驱动发现的障碍，加速精准医学中的假设生成。

## Abstract
In biomedical scientific discovery, identifying relevant omics datasets and interpreting analysis results using prior knowledge from databases and literature are essential for generating novel hypotheses. Although recent AI agents support automated omics analysis and literature retrieval, they typically require users to predefine and curate disease-specific datasets, which is a process that remains challenging and time-consuming, particularly for non-computational researchers. Herein we present OmniCellAgent, a multi-agent AI framework built on large-scale single-cell RNA sequencing (scRNA-seq) resources that autonomously retrieves, integrates and analyzes disease and control-related datasets of diverse cell types across tissues and conditions. Moreover, OmniCellAgent incorporates a biomedical prior knowledge agent for systematic target annotation using curated databases and literature, as well as domain-specific expert agents for downstream interpretation of high-priority targets. By aggregating evidence across agents, the framework generates structured analytical reports and data-driven hypotheses. We evaluate OmniCellAgent across multiple disease settings, demonstrating its ability to identify relevant datasets, prioritize biologically meaningful targets and produce comprehensive, evidence-supported hypotheses. Our results suggest that multi-agent AI systems can reduce barriers to omics-driven discovery and accelerate hypothesis generation in precision medicine.

---

## 论文详细总结（自动生成）

## 1. 研究动机与核心问题

- **领域痛点**：在生物医学科学发现中，非计算背景的研究人员往往难以高效地检索、筛选和整合来自不同组织、不同条件下的组学数据（尤其是单细胞转录组数据），也难以利用数据库与文献中的先验知识对分析结果进行解释，从而阻碍了新假设的快速生成。
- **现有局限**：近期出现的一些人工智能代理虽可支持自动化组学分析与文献检索，但仍要求用户预先定义并人工整理特定疾病的数据集，这一工作繁琐、耗时，对非计算人员极不友好。
- **论文目标**：提出一种能够**自主完成组学数据检索、整合、分析与解释**的多智能体框架，以降低组学驱动科学发现的门槛，加速精准医学领域的假设生成。

## 2. 方法论

- **整体框架**：OmniCellAgent 是一个基于大规模单细胞 RNA 测序（scRNA-seq）资源的**多智能体 AI 系统**，通过多个专业化代理协作完成从数据获取到假设生成的全流程。
- **关键代理与流程**：
  - **自主数据检索与整合代理**：负责根据疾病与对照条件，自动检索不同组织、不同细胞类型的相关 scRNA-seq 数据集，并进行整合与分析，无需用户手动筛选。
  - **生物医学先验知识代理**：利用人工整理的数据库和科学文献，对分析得到的候选靶点进行**系统化的功能注释和证据提取**。
  - **领域专家代理**：针对被优先排序的高价值靶点，进行下游的深度解释与机制推理。
  - **证据聚合与报告生成**：各代理的证据最终被汇总，自动生成结构化的分析报告和**数据驱动的假设**。
- **技术特点**：框架将数据集检索、整合、注释和解读这些原本依赖领域专家和计算技能的步骤，封装为多个可协同的 AI 代理，实现高度自动化。

## 3. 实验设计

- **评估场景**：论文在**多种疾病设置**下对 OmniCellAgent 进行了验证（具体疾病类型在所提供的元数据中未展开，原文应包含病例研究）。
- **能力证明**：
  - 能否成功识别并整合与疾病相关的单细胞数据集；
  - 能否从海量基因或细胞靶点中**优先筛选出具有生物学意义的候选靶点**；
  - 能否生成涵盖证据来源、推理路径的**综合性假设和报告**。
- **对比方法**：元数据中未提及具体的基线方法或对比实验（如与传统人工流程、其他单体 AI 代理的横向比较），但指出过往的 AI 代理需要用户预定义数据集，OmniCellAgent 在此基础上实现了更高程度的自动化。

## 4. 资源与算力

- 所提供的信息（含论文元数据与摘要）**未明确说明** OmniCellAgent 的训练、运行所使用的 GPU 型号、数量、显存规模或总训练时长。从框架描述看，可能更多依赖对已有数据库、文献的检索和现成模型（如大语言模型）的调度，算力需求需查看原文详细技术路线才能确定。

## 5. 实验数量与充分性

- **实验丰富度**：文中提到“在多种疾病设置下”进行评估，但未给出疾病场景的具体个数、数据集规模、消融实验设计（如移除某一代理后的性能变化）等细节。
- **充分性判断**：仅依据现有摘要和元数据，无法定量评估实验是否充分、能否消除偶然性。若原文详细展示了多病种、多指标、与人工及现有工具的客观对比，则实验说服力会较强；此处仅能指出需阅读全文进一步确认。

## 6. 主要结论与发现

- OmniCellAgent 在多疾病场景中**成功自主识别并整合了相关单细胞数据集**，无需用户预先整理。
- 框架能够**有效优先排序具有生物学意义和转化潜力的靶点**，并生成证据充分、逻辑链清晰的假设。
- 多智能体协作模式可以**显著降低非计算专业研究者利用组学数据进行发现的门槛**，有助于加速精准医学从数据到假设的转化。

## 7. 优点

- **高度自动化**：打通了从数据检索到假设生成的全流程，大幅减少人工干预。
- **多代理协作设计**：将数据工程、先验知识查阅和领域推理分配给专门代理，架构清晰且可扩展。
- **面向非计算用户**：直击生物医学研究人员在计算与数据整合上的薄弱环节，提升研究效率。
- **证据集成**：生成报告附有支持性证据，有助于后续实验验证和科学传播。

## 8. 不足与局限

- **信息受限**：当前总结基于论文元数据与摘要，缺乏对具体数据集、病种、对比基准、失败案例及代理间通信机制的深入洞察。
- **潜在偏差**：自动检索可能会受限于所接数据库的覆盖面，导致某些疾病或数据稀少的领域表现不佳；先验知识代理依赖既有文献与数据库，可能存在发表偏倚或知识陈旧的问题。
- **可解释性**：多代理推理过程的透明度与可追溯性需要进一步论证，尤其当多个代理的证据出现冲突时如何协调未在摘要中提及。
- **应用限制**：框架主要基于 scRNA-seq 资源，对于其他组学（如蛋白组、代谢组）的普适性尚未验证。

（完）
