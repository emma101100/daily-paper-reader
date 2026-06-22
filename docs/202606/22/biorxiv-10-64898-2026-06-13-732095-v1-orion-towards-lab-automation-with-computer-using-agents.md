---
title: "Orion: Towards Lab Automation with Computer-Using Agents"
authors: "Ma, C., Trinh, L., Bucci, M., Regev, A., Wang, H."
date: 2026-06-16
pdf: "https://www.biorxiv.org/content/10.64898/2026.06.13.732095v1.full.pdf"
tags: ["query:autoresearch"]
score: 8.0
evidence: 一种自动化生物医学图像分析与解释的AI代理，助力科学发现
tldr: Orion是一个面向生物医学图像分析与解释的计算机使用AI代理，旨在自动化实验室工作流程的计算层面。它结合了大型语言模型、终端执行、GUI控制和自适应多步推理，能够检查视觉数据、操作标准科学软件、挖掘网络资源并整合跨来源知识，从而将实验数据与分析和假设生成相连接，为实验室自动化迈出了重要一步。
source: biorxiv
selection_source: carryover_cache
motivation: 一种自动化生物医学图像分析与解释的AI代理，助力科学发现。
method: 方法与实现细节请参考摘要与正文。
result: 结果与对比结论请参考摘要与正文。
conclusion: 总体而言，该工作在所述任务上展示了有效性，并提供了可复用的思路或工具。
---

## Abstract
Laboratory discovery increasingly depends on computational workflows that connect experimental data to analysis, interpretation and follow-up hypotheses. Yet these workflows remain constrained by labor-intensive use of specialized software, visual inspection through graphical user interfaces, and integration of knowledge across multiple sources. Here, we present Orion, a computer-using AI agent for biomedical image analysis and interpretation that moves towards lab automation by automating this computational layer of laboratory work. Orion combines large language models with terminal execution, GUI control and adaptive multi-step reasoning in a shared computing environment. It can inspect visual data, operate standard scientific software, mine web resources and conduct end-to-end analysis and interpretation workflows without requiring bespoke software integrations. Across benchmarks, Orion achieved over 90% accuracy on biomedical database and literature retrieval tasks, learned to use the popular tools CellProfiler and QuPath for quantitative analysis of cellular and tissue images, respectively, and facilitated autonomous discovery in experimental imaging data. In 100 hours of autonomous exploration of a large-scale perturbation imaging dataset, Orion generated 52 research reports, of which human scientist review prioritized 22 plausible mechanistic hypotheses. These results show that computer-using AI agents can substantially expand the reach of laboratory automation, providing a scalable and auditable route from experimental imaging data to quantitative analysis, reports and biologically grounded hypotheses.



O_FIG O_LINKSMALLFIG WIDTH=200 HEIGHT=45 SRC="FIGDIR/small/732095v1_ufig1.gif" ALT="Figure 1">
View larger version (20K):
org.highwire.dtl.DTLVardef@12ac457org.highwire.dtl.DTLVardef@c03dcaorg.highwire.dtl.DTLVardef@118c023org.highwire.dtl.DTLVardef@1ee6ba2_HPS_FORMAT_FIGEXP  M_FIG Overview of Orion

Orion operates within a digital lab environment, using both graphical user interfaces and terminals just like a human scientist. This dual approach allows Orion to interact seamlessly with scientific software while also viewing figures and web databases to capture their nuanced visual information.

C_FIG