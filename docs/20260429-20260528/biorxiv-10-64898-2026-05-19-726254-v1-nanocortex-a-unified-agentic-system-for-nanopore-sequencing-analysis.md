---
title: "NanoCortex: A Unified Agentic System for Nanopore Sequencing Analysis"
title_zh: "NanoCortex: 一个统一的纳米孔测序分析智能体系统"
authors: "Xia, Q., Wang, Z., Shokoufandeh, M., Rouhanifard, S. H., Wanunu, M."
date: 2026-05-21
pdf: "https://www.biorxiv.org/content/10.64898/2026.05.19.726254v1.full.pdf"
tags: ["query:autoresearch"]
score: 8.0
evidence: 用于纳米孔测序分析的全自动多智能体系统
tldr: 纳米孔测序可获取DNA/RNA序列异构体及化学修饰等多层信息，但现有分析工具分散，用户使用困难。NanoCortex是一个基于Gemini API和ADK的统一自主代理框架，采用多代理架构自动进行任务解析、代码生成、迭代自我修正及科学解释。相比通用大语言模型，它在复杂分析任务上可用性显著更高。该框架无缝集成实验数据与公共数据库元分析，无需繁琐计算步骤即可提取生物学意义。
source: biorxiv
selection_source: fresh_fetch
motivation: 解决纳米孔测序分析工具分散、用户难以整合使用的痛点。
method: 基于Gemini API和ADK的多代理自主框架，涵盖从原始信号basecalling到生物学解释的端到端处理。
result: 在复杂分析任务上，NanoCortex比通用大语言模型实现了显著更高的可用性。
conclusion: 框架无缝整合实验数据与公共数据库，简化了生物学意义的提取过程。
---

## 摘要
纳米孔测序已经能够提供关于DNA和RNA序列异构体及化学修饰的多个层次信息。然而，分散的纳米孔分析工具使得用户在这些工具之间导航成为一项重大挑战。我们提出NanoCortex，一个统一的自主智能体框架，旨在通过提供从原始信号碱基识别到生物学解释的端到端数据处理来弥补这一不足。该系统基于Gemini API服务（按使用量计费）构建，并通过Gemini Agent开发工具包（ADK）进行编排，采用多智能体架构自主执行任务解析、代码生成、迭代式代码级自我修正和科学解释。代码生成后，可离线使用。基准测试显示，与通用大语言模型相比，NanoCortex在复杂分析任务上实现了显著更高的可用性。该框架将实验数据与公开生物数据库的元分析无缝集成，有助于从测序数据中提取生物学上有意义的见解，而无需繁琐的计算步骤。

## Abstract
Nanopore sequencing has enabled various layers of information about DNA and RNA sequence isoforms and chemical modifications. Yet, the archipelago of disjoint nanopore analysis tools makes navigating among these a significant challenge for the nanopore user. We present NanoCortex, a unified autonomous agentic framework designed to bridge this shortcoming by providing end-to-end data processing which ranges from raw signal basecalling to biological interpretation. Built upon Gemini API services that incur usage-based API costs and orchestrated through the Gemini Agent Development Kit (ADK), the system utilizes a multi-agent architecture to autonomously perform task parsing, code generation, iterative code-level self-correction of code, and scientific interpretation. Following code generation, the code can be used offline. Benchmarking reveals that NanoCortex achieves significantly higher usability across complex analytical tasks compared to general-purpose large language models. The framework seamlessly integrates experimental data with meta-analysis of publicly available, biological databases to facilitate the extraction of biologically meaningful insights from sequencing data without cumbersome computational steps.