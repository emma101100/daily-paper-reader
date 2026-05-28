---
title: "Talk2QSP: Deriving Executable Scenarios from Unstructured Literature via Human-in-the-Loop Agents"
title_zh: Talk2QSP：通过人在回路代理从非结构化文献中推导可执行场景
authors: "Kazemeini, A., Prieto, J., Balaji Kuttae, S., Siokis, A., Singh, G., Passban, P., Andreani, T."
date: 2026-05-15
pdf: "https://www.biorxiv.org/content/10.64898/2026.05.06.723244v2.full.pdf"
tags: ["query:autoresearch"]
score: 8.0
evidence: 从文献提取可执行场景的代理框架
tldr: 制药研发中，QSP模型需将非结构化文献中的临床/临床前情景转化为可执行干预，但现有单次推理不可靠。本文提出基于代理的框架，结合语义基础、LLM驱动的Scenario Extractor和双代理Scenario Mapper，并通过人机交互处理歧义。在四个ODE/QSP模型和七个专家情景上，所有情景均被正确解析为参数变化，包括多剂量干预、单位转换等案例。该方法验证了结构化人机协作能可靠解决原始SBML推理无法处理的情景。
source: biorxiv
selection_source: fresh_fetch
motivation: 非结构化文献中的临床情景难以自动转化为可执行的QSP模型干预，现有单次推理LLM调用不可靠。
method: 提出基于代理的框架，包含语义基础、LLM驱动的Scenario Extractor和双代理Scenario Mapper，并采用动态人机交互策略解决歧义。
result: 在四个ODE/QSP模型和七个专家情景上，所有情景被正确解析为参数变化，包括多剂量、单位转换、无操作和歧义触发人机交互案例。
conclusion: 结构化人机协作代理系统能可靠解决原始SBML推理无法处理的情景，提升QSP模型作为实验规划引擎的实用性。
---

## 摘要
定量系统药理学（QSP）模型在药物研发中扮演着固有的干预角色，作为可执行的因果系统用于设计、评估和替代临床试验。然而，将QSP用作实验规划引擎仍受到限制，因为将临床或临床前场景的非结构化文献描述转化为可复现的、适合模拟的模型干预措施存在困难。受此问题启发，我们提出了一种基于代理的框架，通过自动提取和执行文献推导的场景，将QSP模型操作化为可干预的实验系统。该框架将模型实体的语义基础与大型语言模型（LLM）驱动的场景提取器和双代理场景映射器相结合。我们的流程不依赖于不透明的单次推理，而是通过离散、可验证的工作单将自由文本干预转化为精确的参数配置。此外，我们的动态人在回路（HITL）策略使建模者能够交互式地解决生物学歧义。在四种不同的动力学常微分方程（ODE）/ QSP模型和七个主题专家（SME）策划的文献场景中，我们的模型将所有选定场景解析为正确的可执行参数变化，包括多剂量干预、单位转换、无操作场景以及歧义触发的HITL案例，证明了专家与代理系统之间的结构化协作可以解决独立的原始系统生物学标记语言（SBML）推理LLM调用不可靠处理的场景。

## Abstract
Quantitative Systems Pharmacology (QSP) models play an inherently interventional role in pharmaceutical research and development, functioning as executable causal systems for designing, evaluating, and replacing clinical trials. However, deploying QSP as an experimental planning engine remains constrained by the difficulty of translating unstructured literature descriptions of clinical or preclinical scenarios into reproducible, simulation-ready model interventions. Motivated by this issue, we propose an agent-based framework that operationalizes QSP models as intervention-ready experimental systems by automatically extracting and executing literature-derived scenarios. The framework combines semantic grounding of model entities with a large language model (LLM)-driven Scenario Extractor and a dual-agent Scenario Mapper. Rather than relying on opaque, single-shot reasoning, our pipeline converts free-text interventions into precise parameter configurations through discrete, verifiable work orders. Moreover, our dynamic Human-in-the-Loop (HITL) strategy empowers modelers to resolve biological ambiguities interactively. Across four diverse kinetic ordinary differential equation (ODE)/QSP models and seven Subject Matter Expert (SME)-curated literature scenarios, our model resolved all selected scenarios into correct executable parameter changes, including multi-dose interventions, unit conversions, no-op scenarios, and ambiguity-triggered HITL cases, demonstrating that structured collaboration between experts and agentic systems can resolve scenarios that standalone raw Systems Biology Markup Language (SBML) reasoning LLM calls handle unreliably.