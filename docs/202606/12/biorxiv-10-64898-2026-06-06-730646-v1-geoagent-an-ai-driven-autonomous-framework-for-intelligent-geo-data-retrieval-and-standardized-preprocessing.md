---
title: "GEOAgent: An AI-driven Autonomous Framework for Intelligent GEO Data Retrieval and Standardized Preprocessing"
title_zh: GEOAgent：一种用于智能GEO数据检索和标准化预处理的AI驱动自主框架
authors: "Zhao, Y., Cai, Q., Chen, D., Chen, J."
date: 2026-06-10
pdf: "https://www.biorxiv.org/content/10.64898/2026.06.06.730646v1.full.pdf"
tags: ["query:autoresearch"]
score: 6.0
evidence: AI驱动的自主框架，用于智能GEO数据检索和标准化预处理
tldr: "针对GEO数据库样本注释异构和测序数据预处理繁琐问题，GEOAgent框架通过自主语义治理和自动化Nextflow管道，实现自然语言检索和标准化预处理，自动解析实验设计并生成容器化工作流。在基准测试中，检索精度达96%，分析分类与样本关系解析准确率100%。该框架大幅降低人工管理负担，提供公开可用的平台和源代码，加速生物信息学数据整合与重用。"
source: biorxiv
selection_source: fresh_fetch
motivation: GEO数据集因样本注释异构和测序数据需要特定预处理而难以大规模重用。
method: 构建自主语义治理框架与Nextflow管道bioStream，结合关系数据库和语义索引，实现自然语言检索，自动确定分析模式、解析实验设计并生成容器化工作流清单。
result: "专家基准测试中，检索精度96%，分析模态分类和样本关系解析准确率均为100%。"
conclusion: GEOAgent大幅减少人工管理，提供公开可用的平台和源代码，有效提升GEO数据重用效率。
---

## 摘要
基因表达综合数据库（GEO）中的数据集在规模上难以重复使用，因为样本注释是异质的，原始测序数据需要特定于分析的预处理。我们提出了GEOAgent，这是一个AI驱动的自主框架，旨在通过将自主语义治理与名为bioStream的自动化Nextflow管道相结合，实现智能数据集检索和标准化预处理。来自181,760个测序系列和84,756个相关PubMed记录的元数据被组织在一个关系数据库和语义索引中，以支持自然语言数据集检索。该框架自动确定分析模式，解析实验设计配对，并标准化样本命名，以最大限度地减少人工整理的工作量。基于这些解析的属性，该框架生成部署就绪的清单，以自动执行跨批量和单细胞组学模式的容器化工作流程。在专家整理的基准测试中，该工作流程实现了96%的检索精度，同时在分析分类和样本关系解析方面实现了100%的准确性。该网络平台可公开访问，而源代码和相关数据库可通过GitHub和Zenodo公开获取。

## Abstract
Datasets in the Gene Expression Omnibus (GEO) remain difficult to reuse at scale because sample annotations are heterogeneous and raw sequencing data require assay-specific preprocessing. We present GEOAgent, an AI-driven autonomous framework designed for intelligent dataset retrieval and standardized preprocessing by coupling autonomous semantic governance with an automated Nextflow pipeline named bioStream. Metadata from 181,760 sequencing series and 84,756 associated PubMed records were organized in a relational database and semantic index to support natural-language dataset retrieval. The framework automatically determines assay modalities, resolves experimental design pairings, and standardizes sample naming to minimize manual curation overhead. Based on these parsed attributes, the framework generates deployment-ready manifests to automatically execute containerized workflows across bulk and single-cell omics modalities. In expert-curated benchmarks, the workflow achieved 96% retrieval precision alongside 100% accuracy in assay classification and sample relationship resolution. The web platform is publicly accessible, while the source code and associated databases are openly available via GitHub and Zenodo.