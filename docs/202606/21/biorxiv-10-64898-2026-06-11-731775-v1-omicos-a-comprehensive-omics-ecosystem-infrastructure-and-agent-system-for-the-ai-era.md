---
title: "OmicOS: A Comprehensive Omics Ecosystem Infrastructure and Agent System for the AI Era"
authors: "Zeng, Z., Meng, X., Hu, L., Li, C., Liu, P., Shi, Y., Ma, X., Gao, L., Wang, X., Luo, Z., Zheng, Y., Xian, J., Lin, Z., Zhu, H., Jiang, Z., Mao, S., Lu, Y., Tang, W., Peng, Q., Ma, Y., Zhou, L., Xing, C., Zhang, X., Xiong, Y., Du, H."
date: 2026-06-16
pdf: "https://www.biorxiv.org/content/10.64898/2026.06.11.731775v1.full.pdf"
tags: ["query:autoresearch"]
score: 9.0
evidence: 将组学社区转化为可执行基础的代理系统，使能自主科学发现。
tldr: 生物学积累了庞大的组学方法生态系统，但这些工具分散于各种语言和容器，难以被AI代理直接调用。OmicOS将开放组学社区OmicVerse V2转化为可执行的基础设施，提供兼容AnnDataOOM的Rust后端和代理友好的算法，使AI系统能够可靠地选择、执行和验证组学分析。这为构建可自主进行科学研究的代理系统奠定了实用基础。
source: biorxiv
selection_source: fresh_fetch
motivation: 将组学社区转化为可执行基础的代理系统，使能自主科学发现。
method: 方法与实现细节请参考摘要与正文。
result: 结果与对比结论请参考摘要与正文。
conclusion: 总体而言，该工作在所述任务上展示了有效性，并提供了可复用的思路或工具。
---

## Abstract
Biology has accumulated a vast ecosystem of omics methods, but much of this ecosystem remains built for expert humans rather than scientific agents. Methods are scattered across Python packages, R/Bioconductor and CRAN workflows, command-line tools, incompatible data containers and implicit object states, making even routine analyses difficult for an AI system to choose, execute and verify reliably. Here we introduce OmicOS, a comprehensive omics ecosystem infrastructure and agent system that turns OmicVerse V2, an open-source omics community, into an executable foundation for agentic biology. OmicVerse V2 provides the community substrate: scalable AnnDataOOM-compatible rust backends, agent-friendly Python algorithms for single-cell, spatial, bulk and multi-omics analysis, interfaces to single-cell foundation models, and Python-native reconstructions of historically R-centred Bioconductor/CRAN-style workflows. OmicOS makes this substrate actionable by registering analytical functions as state-aware capability contracts, allowing agents to inspect live data objects, select valid methods, execute controlled workflows and record provenance. The result is not a fixed pipeline, but a programmable omics environment in which agents compose real analyses from verified community methods rather than inventing tools. Across external and purpose-built benchmarks, OmicOS ranked first among the evaluated systems, reaching 81.2% on BiomniBench. Adding OmicVerse to a minimal agent improved task completion by up to 34.2 percentage points with qwen-3.6-35b, and controlled ablations showed that the gains came from registry-grounded execution rather than from larger models, documentation retrieval or unrestricted tool exposure. The same infrastructure scaled to atlas-sized data, reproduced R-centred workflows in Python and converted external pathology software into agent-usable skills. In a discovery task starting from a whole-body spatial map and the term "Alzheimers disease", OmicOS composed a non-canonical workflow that integrated spatial expression, genetic association, eQTL and colocalization evidence to nominate a colon epithelial risk axis centred on PICALM, CD2AP and CR1. Together, OmicVerse and OmicOS define an open foundation for AI-era omics, showing how a community of biological methods can be transformed into a reliable, extensible and agent-operable system for discovery.

HighlightO_LIOmicVerse 2.0 consolidates 694 methods spanning 11 omics domains into agent-callable high-level APIs.
C_LIO_LIRebuildR automatically reconstructs and evolves R/Bioconductor methods as Python-native implementations under output-equivalence gates.
C_LIO_LIOmicOS establishes a state-of-the-art omics agent harness, ranking first on general omics benchmarks across models and substantially improving the analytical capability of local open-source models.
C_LIO_LICompositional use of ecosystem modules nominates a colon epithelial axis associated with Alzheimers disease risk.
C_LIO_LIExternal algorithm packages supporting automatic iterative evolution can be integrated into the OmicOS ecosystem.
C_LI