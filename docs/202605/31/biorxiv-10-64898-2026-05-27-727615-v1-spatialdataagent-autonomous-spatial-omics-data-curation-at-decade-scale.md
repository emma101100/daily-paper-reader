---
title: "SpatialDataAgent: Autonomous Spatial Omics Data Curation at Decade Scale"
title_zh: SpatialDataAgent：十年尺度的自主空间组学数据整理
authors: "Ji, J.-H., Zou, Q., Cheng, J., She, Z., Hao, Y., Liu, W., Zhang, D., Wang, Z., Yu, J.-T., Yuan, Z."
date: 2026-05-30
pdf: "https://www.biorxiv.org/content/10.64898/2026.05.27.727615v1.full.pdf"
tags: ["query:autoresearch"]
score: 7.0
evidence: 自主空间组学数据整理的智能体工作流，含自我优化标准化与证据评估
tldr: "为解决空间组学数据元数据碎片化导致的大量‘暗数据’不可用问题，提出SpatialDataAgent自主整理流程。该智能体通过模式约束证据评估与自我优化标准化，从十年GEO记录中识别出769个配对H&E-空间转录组数据集，规模扩大6.4倍，并建立HESRT数据湖。该工作展示了智能体在生命科学数据整理中的规模化能力，为多模态数据自主发现提供了蓝图。"
source: biorxiv
selection_source: fresh_fetch
motivation: 自主空间组学数据整理的智能体工作流，含自我优化标准化与证据评估。
method: 方法与实现细节请参考摘要与正文。
result: 结果与对比结论请参考摘要与正文。
conclusion: 总体而言，该工作在所述任务上展示了有效性，并提供了可复用的思路或工具。
---

## 摘要
空间组学档案中碎片化的元数据已导致大量多模态分子-组织学数据沦为“暗数据”，难以获取。在此，我们引入SpatialDataAgent，这是一种用于自主空间组学数据整理的代理工作流，它将模式约束的证据评估与自我精炼的标准化代理相结合。应用于长达十年的GEO记录，SpatialDataAgent识别出769个配对的H&E-空间转录组学（ST）数据集，相对于现有手动整理的基线，规模扩大了6.4倍。在基准测试窗口内，该框架使高置信度（A类）配对数据集实现了141%的增长，这些数据集经自动过滤与组装，建成了HESRT（一个包含2920万个点/细胞的数据湖），为多模态生物医学档案的循证自主整理树立了蓝图。

## Abstract
Fragmented metadata in spatial omics archives has rendered large volumes of multimodal molecular-histological data inaccessible as 'dark data'. Here, we introduce SpatialDataAgent, an agentic workflow for autonomous spatial omics data curation, combining schema-constrained evidence evaluation with a self-refining standardization agent. Applied to a decade of GEO records, SpatialDataAgent identified 769 paired H&E-spatial transcriptomics (ST) datasets, representing a 6.4-fold scale expansion over existing manually curated baselines. Within the benchmarking window, the framework achieved a 141% increase in high-confidence (Class A) paired datasets, which were automatically filtered and assembled to establish HESRT (a datalake containing 29.2 million spots/cells), establishing a blueprint for evidence-grounded autonomous curation of multimodal biomedical archives.