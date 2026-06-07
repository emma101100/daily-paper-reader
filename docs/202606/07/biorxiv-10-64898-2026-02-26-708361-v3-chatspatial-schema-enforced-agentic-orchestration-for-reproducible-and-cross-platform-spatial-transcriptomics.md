---
title: "ChatSpatial: Schema-Enforced Agentic Orchestration for Reproducible and Cross-Platform Spatial Transcriptomics"
title_zh: ChatSpatial：面向可重复且跨平台空间转录组学的模式强制智能体编排
authors: "Yang, C., Zhang, X., Chen, J."
date: 2026-06-04
pdf: "https://www.biorxiv.org/content/10.64898/2026.02.26.708361v3.full.pdf"
tags: ["query:autoresearch"]
score: 7.0
evidence: 基于LLM的平台强制使用预验证工具模式，构建跨Python和R的可重复分析工作流，确保溯源。
tldr: 空间转录组学分析因Python与R工具生态割裂，迫使研究者疲于适配而非探索生物学问题。ChatSpatial平台让LLM根据领域知识嵌入的模式描述，从60余种预验证工具中智能选择，而非自由生成代码，基于模型上下文协议提供跨生态统一对话式工作流。复现卵巢癌与口腔鳞癌两项已发表研究，展示工作流级近乎确定性可重复性，并经7种LLM验证。该系统通过模式强制编排保障分析可重复性，支持跨方法三角验证，为空间组学研究提供可靠基础。
source: biorxiv
selection_source: fresh_fetch
motivation: 空间转录组学分析因Python与R工具不兼容，迫使研究者侧重工具适配而非生物学洞察。
method: ChatSpatial通过LLM选择预验证工具模式，而非自由生成代码，基于MCP统一60+方法为跨平台对话式工作流。
result: 在复现卵巢癌与口腔鳞癌研究中，工作流结果近乎确定性可重复，并在7个LLM上验证，支持跨方法三角测量。
conclusion: ChatSpatial通过模式强制编排，为空间转录组学提供可重复、跨平台的智能分析方案，促进方法交叉验证。
---

## 摘要
空间转录组学改变了我们在分子分辨率下研究组织架构的能力，但分析这些数据需要在互不兼容的Python和R生态系统中驾驭数十种计算方法，迫使研究人员在让工具正常运行上投入的精力比追求生物学问题还多。我们提出了ChatSpatial，一个由大语言模型从预验证的工具模式中进行选择而非生成自由形式代码的平台，并将领域专业知识嵌入模式描述中，以实现上下文感知的参数推断。基于模型上下文协议（MCP）构建，ChatSpatial将15个分析类别下的60多种方法统一到跨越Python和R生态系统的单一对话式工作流程中。通过对两项已发表研究的复现——揭示卵巢癌中的亚克隆异质性和口腔鳞状细胞癌中的肿瘤微环境组织——以及在七个大语言模型平台上的验证，表明对于多步骤空间分析，模式强制的编排能在工作流程层面实现近乎确定性的可重复性。除复现外，探索性的跨方法分析展示了跨独立分析框架的实际三角验证。

## Abstract
Spatial transcriptomics has transformed our ability to study tissue architecture at molecular resolution, yet analyzing these data demands navigating dozens of computational methods across incompatible Python and R ecosystems---forcing researchers to devote more effort to making tools function than to pursuing biological questions. We present ChatSpatial, a platform in which the LLM selects from pre-validated tool schemas rather than generating free-form code, with domain expertise embedded in schema descriptions for context-aware parameter inference. Built on the Model Context Protocol (MCP), ChatSpatial unifies 60+ methods across 15 analytical categories into a single conversational workflow spanning Python and R ecosystems. Replication of two published studies---recovering subclonal heterogeneity in ovarian cancer and tumor microenvironment organization in oral squamous cell carcinoma---and validation across seven LLM platforms demonstrate that schema-enforced orchestration yields near-deterministic reproducibility at the workflow level for multi-step spatial analyses. Beyond replication, exploratory cross-method analyses illustrate practical triangulation across independent analytical frameworks.