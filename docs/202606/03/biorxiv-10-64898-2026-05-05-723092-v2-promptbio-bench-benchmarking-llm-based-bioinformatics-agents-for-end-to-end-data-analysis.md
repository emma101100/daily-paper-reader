---
title: "PromptBio-Bench: Benchmarking LLM-based Bioinformatics Agents for End-to-End Data Analysis"
title_zh: PromptBio-Bench：面向端到端数据分析的基于大语言模型的生物信息学代理基准测试
authors: "Guo, W., Zhang, M., Han, B., Ma, Y., Leng, Y., Hebbar, S., Zhou, X., Gu, W., Yang, X., Dhar, S."
date: 2026-06-01
pdf: "https://www.biorxiv.org/content/10.64898/2026.05.05.723092v2.full.pdf"
tags: ["query:autoresearch"]
score: 7.0
evidence: 评测基于大语言模型的智能体在自动化生物信息学数据分析这种科学工作流中的能力
tldr: 基于大语言模型的生物信息学智能体有望自动化工作流，但系统评估不足，阻碍技术落地。为此，我们构建了PromptBio-Bench基准，包含244个覆盖生物信息与数据科学的多难度专家任务及结构化评分框架。评测三个前沿智能体显示，Biomni与ToolsGenie性能相当，但所有智能体在面对困难任务时准确率显著下降。该基准为自动化生物信息智能体的持续进步提供了标准化评估基础设施。
source: biorxiv
selection_source: fresh_fetch
motivation: LLM驱动的生物信息学智能体缺乏系统评估，阻碍了其实际应用准备度的判断。
method: 提出PromptBio-Bench，包含244个专家策划的多难度任务和结构化文件比较评分框架。
result: 评估显示Biomni和ToolsGenie性能相当，但所有智能体在面对困难任务时准确率显著下降。
conclusion: PromptBio-Bench为评估并推动自动化生物信息智能体发展提供了系统基准。
---

## 摘要
基于大语言模型（LLM）的代理在自动化生物信息学工作流程方面具有变革潜力；然而，对其能力的系统评估仍然有限，妨碍了对其实际应用准备程度的清晰评估。我们推出了 PromptBio-Bench，这是一个包含 244 项专家策划任务的综合评估套件，涵盖不同难度级别的生物信息学和数据科学，并提供了一个用于结构化文件比对和参照专家参考答案文件进行评分的评估框架。对三种最先进的生物信息学代理的评估显示，Biomni 和 ToolsGenie 的性能相当，所有代理的准确率都随着任务难度的增加而显著下降。随着基础模型和代理框架的不断发展，PromptBio-Bench 为系统性地跟踪代理化生物信息学的进展提供了一个有价值的基准基础设施。

## Abstract
Large language model (LLM)-based agents hold transformative potential for automating bioinformatics workflows; however, systematic evaluations of their capabilities remain limited, hindering a clear assessment of their readiness for real-world application. We introduce PromptBio-Bench, a comprehensive evaluation suite of 244 expert-curated tasks spanning bioinformatics and data science at varied difficulty levels, and an evaluation framework for structured file comparison and scoring against expert reference answer files. Evaluation of three state-of-the-art bioinformatics agents revealed comparable performance between Biomni and ToolsGenie, with all agents showing a marked decline in accuracy as task difficulty increased. As foundation models and agent frameworks continue to evolve, PromptBio-Bench provides a valuable benchmark infrastructure for systematically tracking progress in agentic bioinformatics.