---
title: Reproducible and shareable bioinformatics pipelines from natural-language prompts
title_zh: 基于自然语言提示的可重现和可共享生物信息学流程
authors: "Kim, H.-M., Jeong, H., Mekonnen, A. M., Kim, Y., Oh, Y., Lee, H., Jung, C., Park, J."
date: 2026-06-01
pdf: "https://www.biorxiv.org/content/10.64898/2026.05.28.719125v1.full.pdf"
tags: ["query:autoresearch"]
score: 8.0
evidence: 生成保留源代码且可重新执行的容器化流水线，确保可复现性和溯源
tldr: 大型语言模型从自然语言生成的生物信息学分析流程难以跨会话复现和共享，且无法在远程高性能计算环境运行。为此开发了Autopipe平台，引导兼容MCP的LLM产生可重新执行的容器化流水线。该平台支持在任意本地远程服务器上执行分析并可视化结果，将对话式分析转变为可复用工作流。Autopipe显著提升了LLM驱动生物信息学研究的可重复性和协作效率。
source: biorxiv
selection_source: fresh_fetch
motivation: LLM生成的生物信息学分析因会话非确定性及环境异构性难以重现，无法远程执行或共享。
method: 提出Autopipe平台，通过MCP兼容的LLM生成容器化流程，包含桌面应用、在线注册表、结果查看器和CLI工具。
result: Autopipe将会话分析转化为可重新执行、可共享的工作流，支持远程执行和基于Web的结果可视化。
conclusion: Autopipe解决了LLM驱动生物信息学分析的可重复性问题，提供免费平台，推动研究协作与复用。
---

## 摘要
大型语言模型（LLMs）越来越多地被用于从自然语言提示生成生物信息学流程并进行分析。然而，由于LLM驱动的对话的非确定性以及本地执行环境的异质性，所得到的分析往往难以在不同会话间重现，并且无法在远程高性能计算（HPC）服务器上运行，也无法被共享和重用。我们推出了Autopipe，一个引导任何与模型上下文协议（MCP）兼容的LLM生成、执行和发布保留源代码、可重新执行的容器化流程的平台。Autopipe使用户能够在任何用户自有的远程服务器上执行生物信息学流程——并配有全面的设置文档，旨在帮助没有服务器管理经验的研究人员——并通过可扩展的基于Web的查看器可视化结果。Autopipe平台包含四个组件：一个集成了MCP服务器的桌面应用程序，用于流程管理和远程执行；一个用于流程和插件发现的在线注册表；一个基于Web的结果查看器；以及一个用于自定义查看器插件的CLI工具。Autopipe将对话式分析转变为可重新执行且可共享的工作流。Autopipe可在 https://autopipe.org/ 免费获取。

## Abstract
Large language models (LLMs) are increasingly used to generate bioinformatics pipelines and to carry out analyses from natural-language prompts. However, the resulting analyses are often difficult to reproduce across sessions, owing to the non-deterministic nature of LLM-driven conversations and heterogeneity of local execution environments, and cannot run on remote high-performance computing (HPC) servers or be shared and reused. We present Autopipe, a platform that guides any Model Context Protocol (MCP) - compatible LLM to produce, execute, and publish source-preserved, re-executable containerized pipelines. Autopipe enables users to execute bioinformatics pipelines on any on-premises remote servers - supported by comprehensive setup documentation aimed at researchers without prior server-administration experience - and to visualize results through an extensible web-based viewer. The Autopipe platform comprises four components: a desktop application with an embedded MCP server for pipeline management and remote execution, an online registry for pipeline and plugin discovery, a web-based result viewer, and a CLI tool for customizing viewer plugins. Autopipe turns conversational analysis into re-executable and shareable workflows. Autopipe is freely available at https://autopipe.org/.