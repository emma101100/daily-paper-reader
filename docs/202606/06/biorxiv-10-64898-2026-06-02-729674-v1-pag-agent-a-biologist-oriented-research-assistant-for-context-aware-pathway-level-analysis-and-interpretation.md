---
title: "PAG-Agent: a biologist-oriented research assistant for context-aware pathway-level analysis and interpretation"
title_zh: PAG-Agent：面向生物学家的情境感知通路级分析与解读研究助手
authors: "Nguyen, Q.-H., Zhang, Z., Le, D.-H., Chen, J. Y., Ku, W.-S., Chen, H., Yue, Z."
date: 2026-06-06
pdf: "https://www.biorxiv.org/content/10.64898/2026.06.02.729674v1.full.pdf"
tags: ["query:autoresearch"]
score: 9.0
evidence: 整合通路分析、文献推理和科学写作的研究助理代理
tldr: PAG-Agent是一个面向生物学家的虚拟研究助手，整合通路水平统计分析、上下文感知生物学解读、文献支持推理和科学写作支持于统一工作流。它支持批量与单细胞转录组数据，用户可通过点击与对话进行数据预处理、差异表达、通路分析、共识分析和meta分析，并能结合实验条件与目标优先排序通路。在阿尔茨海默病案例中，跨三个数据集和多种方法一致发现神经退行相关通路；在文献引用基准中，PAG-Agent在五个场景下优于六款竞品LLM。该工具降低了通路分析技术门槛，帮助研究者从转录组数据走向生物学解释、假设生成和科学传播。
source: biorxiv
selection_source: fresh_fetch
motivation: 现有通路分析工具生成大量统计显著通路，但难以结合实验背景和生物学意义进行解读、验证和优先排序。
method: PAG-Agent集成通路水平统计分析、上下文感知解读与文献支持，提供点击和对话交互界面，支持数据预处理、差异表达、通路及共识分析，并关联实验条件。
result: 在阿尔茨海默病转录组分析中，跨三个数据集和多种方法一致检测到神经退行通路；引用检索测试中，PAG-Agent在五个文献支持场景下表现优于六款LLM。
conclusion: PAG-Agent降低了通路分析的技术门槛，实现从组学数据到生物学机制解释、假设生成和科学写作的辅助，能有效提升研究效率和解释深度。
---

## 摘要
通路分析是将基因水平的组学结果转化为生物学机制的关键步骤，但现有工作流程往往使研究者面对一长串难以解读、验证并与实验情境关联的统计显著通路。我们开发了PAG-Agent，一个面向生物学家的虚拟研究助手，将通路级统计分析、情境感知生物学解读、文献支持的推理以及科学写作辅助整合到统一的工作流中。PAG-Agent支持批量及单细胞转录组数据，用户可通过点击和对话式交互进行数据预处理、差异表达分析、通路分析、通路级共识分析和通路级荟萃分析。与大多孤立分析基因集的传统通路分析工具不同，PAG-Agent结合实验条件和研究目标，优先考虑生物学相关通路并生成可解释的假设。系统还提供基因与通路注释、引文检索、可视化和写作润色功能。在利用三个转录组数据集进行的阿尔茨海默病案例研究中，PAG-Agent跨多种分析方法和数据集一致识别出神经退行性相关通路。在引文检索基准测试中，PAG-Agent在五种常见文献支持场景下均优于六种竞品大语言模型，展现了其在提供情境相关且有效参考文献方面的增强能力。总体而言，PAG-Agent降低了通路级分析的技术门槛，帮助研究者从转录组数据走向基于生物学的解读、假设生成和科学交流。

## Abstract
Pathway analysis is a critical step for translating gene-level omics results into biological mechanisms, yet existing workflows often leave researchers with long lists of statistically significant pathways that are difficult to interpret, validate, and connect to experimental context. We developed PAG-Agent, a biologist-oriented virtual research assistant that integrates pathway-level statistical analysis, context-aware biological interpretation, literature-supported reasoning, and scientific writing support within a unified workflow. PAG-Agent supports bulk and single-cell transcriptomic data and enables users to perform data preprocessing, differential expression analysis, pathway analysis, pathway-level consensus analysis, and pathway-level meta-analysis through click-based and chat-based interactions. Unlike conventional pathway-analysis tools that analyze gene sets largely in isolation, PAG-Agent incorporates experimental conditions and research objectives to prioritize biologically relevant pathways and generate interpretable hypotheses. The system also provides gene and pathway annotation, citation retrieval, visualization, and writing refinement functions. In Alzheimer's disease case studies using three transcriptomic datasets, PAG-Agent consistently identified neurodegeneration-related pathways across multiple analysis methods and datasets. In citation-retrieval benchmarking, PAG-Agent outperformed six competing LLMs across five common literature-support scenarios, demonstrating improved ability to provide contextually relevant and valid references. Overall, PAG-Agent lowers technical barriers for pathway-level analysis and helps researchers move from transcriptomic data to biologically grounded interpretation, hypothesis generation, and scientific communication.

---

## 论文详细总结（自动生成）

### 1. 论文的核心问题与整体含义

- **研究动机**：转录组学分析中，差异表达基因的列表往往难以直接转化为生物学机制。通路分析是衔接基因水平结果与生物学意义的关键步骤，但现有工具通常只是输出一长串统计显著的通路，缺乏结合实验背景、研究目标和文献证据进行情境化解读的能力。
- **整体含义**：作者提出 PAG-Agent，一个面向生物学家的虚拟研究助手，旨在将通路级统计分析、情境感知解读、文献支持推理和科学写作辅助整合到一个统一的工作流中，降低技术门槛，帮助研究者从数据走向机制解释、假设生成和科学交流。

### 2. 论文提出的方法论

- **核心思想**：将通路分析从孤立的“基因集统计检验”升级为“情境感知的生物学推理与文献辅助工作流”。PAG-Agent 不仅计算通路显著性，还会结合实验条件、研究目的以及外部文献证据来优先排序通路，并生成可解释的假设。
- **关键技术细节与流程**：
  - **多模态交互**：提供点击式操作和对话式聊天界面，用户可进行数据预处理、差异表达分析、通路分析、通路级共识分析（consensus analysis）和通路级荟萃分析（meta-analysis）。
  - **情境感知通路优先排序**：将实验条件（如疾病 vs 对照、处理 vs 未处理）和研究目标纳入分析，识别在特定生物学背景下真正相关的通路，而非仅依赖统计显著性。
  - **文献支持推理**：内置引文检索模块，能够在用户需要文献支撑解读时，自动提供相关参考文献，并在基准测试中验证其提供有效引用文献的能力。
  - **辅助功能**：提供基因与通路注释、可视化、写作润色等功能，覆盖从分析到成文的整个过程。
  - **数据支持**：兼容批量转录组（bulk RNA-seq）和单细胞转录组（scRNA-seq）数据。

### 3. 实验设计

- **数据集与场景**：
  - **阿尔茨海默病案例研究**：使用三个转录组数据集，跨多个分析方法和数据集一致识别神经退行性相关通路，验证 PAG-Agent 在真实生物学问题中的发现能力和跨数据集一致性。
  - **引文检索基准测试**：设计了五种常见的文献支持场景，评估系统提供情境相关且有效参考文献的能力。
- **对比方法**：在引文检索基准测试中，PAG-Agent 与六种竞品大语言模型（LLMs）进行比较（论文未具体列出模型名，但提及“six competing LLMs”）。

### 4. 资源与算力

- 文中未明确提及使用的 GPU 型号、数量、训练时长等算力细节。PAG-Agent 可能基于 API 调用的 LLM 或本地部署，但具体计算资源消耗信息未被提供。

### 5. 实验数量与充分性

- **案例研究**：在阿尔茨海默病领域使用了三个转录组数据集，跨多种分析方法（差异表达、通路分析、共识分析、meta-analysis）进行内部验证，显示了工具跨数据集和跨方法的一致性。
- **引文检索基准**：设计五种场景，与六个竞品 LLM 对比，从数量上看，场景较为细分，对比对象较丰富。
- **充分性与客观性**：
  - 案例研究虽集中于阿尔茨海默病，但通过多数据集和多方法交叉验证，增强了结论的可靠性。
  - 引文检索基准测试以“提供有效参考文献”为评价指标，对比了多个主流 LLM，结果直接且客观。
  - 然而，未见到消融实验（如去掉文献模块或情境感知模块后性能变化），也未覆盖其他疾病领域或其他组学数据类型，实验广度和内部模块验证稍显不足。

### 6. 论文的主要结论与发现

- PAG-Agent 在阿尔茨海默病案例中跨数据集和多种分析方法一致识别出神经退行性相关通路，表明其生物学发现能力可靠且稳定。
- 在引文检索基准测试中，PAG-Agent 在五种文献支持场景下均优于六种竞品大语言模型，证明其能够更好地提供情境相关且有效的参考文献。
- 整体上，PAG-Agent 降低了通路分析的技术门槛，使生物学家能够从转录组数据高效过渡到有生物学依据的解释、假设生成和科学写作。

### 7. 优点

- **工作流整合**：将统计分析、情境解读、文献引证和写作辅助无缝衔接，避免研究者在不同工具间切换。
- **情境感知设计**：不再是“纯粹统计显著通路列表”，而是结合实验条件和研究目标进行生物学解读，更贴近研究者实际思维过程。
- **多模态交互**：点击操作与对话式交互结合，降低了非生物信息学背景研究者的使用门槛。
- **强大的文献支持**：引文检索能力显著优于直接使用通用 LLM，增强了结论的可信度和可追溯性。
- **跨数据类型与跨方法验证**：支持 bulk 和 scRNA-seq，且用共识分析和荟萃分析增强结果稳健性。

### 8. 不足与局限

- **实验覆盖面较窄**：仅使用阿尔茨海默病相关数据集进行案例验证，未在其他疾病模型、不同物种或更复杂实验设计（如多因素、时间序列）中测试。
- **缺少消融实验**：未明确报告去除情境感知模块、文献支持模块或改变底层 LLM 后系统性能的变化，难以评估各组件贡献度。
- **算力和部署细节缺失**：没有提供系统在本地部署时的硬件需求、推理延迟或基于 API 的成本信息，实用性评估受限。
- **依赖外部文献数据库**：引文检索虽优于通用 LLM，但准确性仍受限于底层数据库覆盖范围和更新及时性，部分领域可能缺乏高质量文献支持。
- **通用性风险**：“情境感知”的具体实现方式未详细披露，可能依赖于对输入实验条件和目标的自然语言理解，存在提示敏感或误解风险。

（完）
