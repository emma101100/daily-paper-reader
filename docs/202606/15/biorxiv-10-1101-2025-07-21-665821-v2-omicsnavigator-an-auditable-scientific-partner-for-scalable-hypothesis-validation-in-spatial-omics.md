---
title: "OmicsNavigator: An auditable scientific partner for scalable hypothesis validation in spatial omics"
title_zh: OmicsNavigator：用于空间组学可扩展假设验证的可审计科学伙伴
authors: "Li, Y., Vakharia, N., Liang, W., Mayer, A. T., Luo, R., Trevino, A. E., Wu, Z."
date: 2026-06-14
pdf: "https://www.biorxiv.org/content/10.1101/2025.07.21.665821v2.full.pdf"
tags: ["query:autoresearch"]
score: 9.0
evidence: 自主LLM系统，用于空间组学的端到端假设验证
tldr: 空间组学分析因高维、多模态数据难以转化为生物学假设而存在瓶颈。OmicsNavigator是一个基于大语言模型的自主系统，通过融合视觉和分子特征进行知识引导注释，将高维数据转换为文本解释，实现零样本生物标志物检索和疾病谱重建，并内置可审计的假设验证引擎。在糖尿病肾病、肾移植排斥和COVID-19肺病理等多病种数据集上验证，系统能产出基于证据的人类可读见解。该工作为空间组学提供可扩展、可解释的模态无关解决方案，有望加速空间生物学发现。
source: biorxiv
selection_source: fresh_fetch
motivation: 空间组学分析的主要瓶颈在于如何将高维多模态数据转化为可验证的生物学假设。
method: OmicsNavigator利用大语言模型对空间组学多模态输入进行推理，通过知识引导注释生成文本解释，并采用预注册蓝图进行假设验证。
result: 在糖尿病肾病、肾移植排斥和COVID-19肺部病理等数据集上，系统成功生成了基于证据的人类可读见解。
conclusion: 该系统为空间组学提供了一种可扩展、可解释且模态无关的分析方案，有望加速生物学发现。
---

## 摘要
将高维、空间解析的分子数据集转化为可检验的生物学发现仍然是一个主要的研究瓶颈。在这里，我们提出了OmicsNavigator，一个自主的大型语言模型驱动系统，用于在空间组学数据上进行端到端数据探索和假设验证。OmicsNavigator直接在空间组学数据的多模态输入（包括视觉和分子特征）上进行推理，执行知识引导的空间结构注释。我们表明，通过将高维数据转化为文本解释，OmicsNavigator能够实现组织生物标志物的零样本语义检索，并从原始组学观测中重建患者水平的疾病档案。此外，OmicsNavigator具有一个客观的假设验证引擎，该引擎由预先注册、经人类审计的蓝图控制。通过在不同病理条件（包括糖尿病肾病、肾移植排斥反应和COVID-19肺部病理）的数据集上验证系统，我们证明OmicsNavigator从空间组学数据中生成基于证据、人类可读的见解，有潜力加速空间生物学发现。OmicsNavigator为空间组学分析提供了一种可扩展、可解释且模态无关的解决方案。

## Abstract
Translating high-dimensional, spatially resolved molecular datasets into testable biological findings remains a major research bottleneck. Here, we present OmicsNavigator, an autonomous large language model-powered system for end-to-end data exploration and hypothesis validation on spatial omics data. OmicsNavigator reasons directly over the multi-modal inputs of spatial omics data, including visual and molecular signatures, to perform knowledge-guided annotation of spatial structures. We show that by transforming high-dimensional data into textual interpretations, OmicsNavigator enables zero-shot semantic retrieval of tissue biomarkers and the reconstruction of patient-level disease profiles from raw omics observations. Furthermore, OmicsNavigator features an objective hypothesis validation engine governed by pre-registered, human-audited blueprints. By validating the system across datasets spanning diverse pathological conditions including diabetic kidney disease, kidney transplant rejection, and COVID-19 pulmonary pathology, we demonstrate that OmicsNavigator generates evidence-based, human-readable insights from spatial omics data, with potential to accelerate spatial biology discoveries.OmicsNavigator offers a scalable, interpretable, and modality-agnostic solution for spatial omics analysis.

---

## 论文详细总结（自动生成）

# 论文深度总结：《OmicsNavigator: 用于空间组学可扩展假设验证的可审计科学伙伴》

## 1. 核心问题与整体含义
- **研究动机**：空间组学（spatial omics）能够同时测量组织中数千个分子特征的空间分布，产生高维、多模态的复杂数据。然而，如何将这类数据高效转化为可检验的生物学假设，仍是限制领域发展的主要瓶颈。传统分析依赖人工解释，效率低、可重复性差，难以规模化。
- **整体含义**：本文提出 OmicsNavigator，通过构建一个由大语言模型（LLM）驱动的自主系统，将空间组学数据自动转化为人类可读的、可验证的生物学见解，旨在打通从原始数据到科学假设的端到端路径，加速空间生物学发现。

## 2. 方法论
- **核心思想**：让 LLM 直接对空间组学的**多模态输入**（包括形态学视觉特征与分子表达谱）进行推理，执行知识引导的空间结构注释，将高维数据转化为文本解释，从而支持下游检索与假设验证。
- **关键技术细节**：
  - **知识引导的空间注释**：系统对组织区域进行语义标注，融合视觉与分子特征，结合生物学先验知识（可能通过 prompt 或知识库嵌入）识别出有生物学意义的结构（如特定细胞区室、病理区域）。
  - **文本化表示**：将高维组学数据转化为自然语言描述，使得组织中的生物标志物和疾病特征可被零样本（zero-shot）语义检索——用户可用自然语言查询（如“显示纤维化区域”）直接定位相关组织区域。
  - **假设验证引擎**：内置客观的假设验证机制，由**预先注册、经人类审计的蓝图**控制，确保验证过程的透明性和可审计性。这意味着系统会按事先制定的分析计划执行统计检验，防止数据探索中的多重检验陷阱和 p-hacking。
  - **模态无关性**：系统设计不依赖于特定的空间组学技术（如 10x Visium、MERFISH、CODEX 等），可适配不同分子模态和成像平台。
- **公式/流程**：摘要未给出具体数学公式，可推断其流程为：多模态数据输入 → LLM 引导的空间结构语义解析 → 生成组织/疾病文本档案 → 零样本语义查询/假设蓝图驱动的验证 → 输出证据支撑的人类可读报告。

## 3. 实验设计
- **使用数据集**：
  - 糖尿病肾病（diabetic kidney disease）空间组学数据
  - 肾移植排斥（kidney transplant rejection）空间组学数据
  - COVID-19 肺部病理（COVID-19 pulmonary pathology）空间组学数据
- **评估场景与 benchmark**：论文摘要未明确说明对比了哪些基线方法或具体的定量 benchmark。从描述推测，验证可能侧重于：
  - 零样本生物标志物检索的准确性或与专家注释的一致性
  - 患者疾病谱重建的合理性与临床相关性
  - 假设验证引擎产出的证据是否支持已知生物学知识
- **对比方法**：原文未提及与其他计算工具（如 Giotto、Squidpy、DeepST 等）的对比，可能需要阅读全文获取具体对比实验信息。

## 4. 资源与算力
- 提供的摘要及元数据中**没有说明** GPU 型号、数量或训练时长。
- 系统采用 LLM 驱动，很可能调用预训练大模型（如 GPT-4 系列或开源模型），但具体模型名称、是否需要微调、推理阶段的算力消耗均未在现有信息中披露。此为待补充项。

## 5. 实验数量与充分性
- **实验数量**：从摘要可知，至少在三种不同病理条件下进行了验证（糖尿病肾病、移植排斥、COVID-19 肺病理）。每个条件下可能包含多组实验（如生物标志物检索、疾病档案重建、假设验证），但具体实验组数、消融实验、敏感性分析等信息未提供。
- **充分性/客观性**：覆盖了肾脏和肺脏两种组织，三种具有不同免疫和基质特征的病理状态，显示了跨疾病、跨器官的通用性。然而，摘要未给出定量指标或统计比较结果，难以评估实验的统计学严格程度。假设验证引擎的“预注册蓝图”设计增强了客观性，但实际执行细节未知。

## 6. 主要结论与发现
- OmicsNavigator 能够直接消化多模态空间组学数据，通过文本化表示实现**零样本语义检索**，无需训练特定分类器即可定位感兴趣的区域和生物标志物。
- 系统可以从原始观测中重建**患者水平的疾病档案**，生成基于证据的、人类可读的见解。
- 在多病种数据集上，系统产出的结论**与现有病理学知识相符**，证明其有潜力加速空间生物学发现的转化过程。
- 其框架具有**可扩展性、可解释性和模态无关性**，为空间组学分析提供了新一代解决方案。

## 7. 优点（亮点）
- **端到端自主性**：从数据探索到假设验证全自动化，减少了人工干预和分析偏见。
- **可审计的验证设计**：预注册蓝图和人类审计机制保证了假设检验的科学严谨性，类似临床试验中的预注册理念，这在计算生物学工具中较为少见。
- **零样本能力**：利用 LLM 的世界知识，避免了对每个新标志物或任务收集标注数据的繁琐过程，大幅提升分析效率。
- **多模态原生推理**：直接在视觉和分子特征联合空间中推理，保持了组织原位信息的完整性。
- **产出人类可读报告**：降低了空间组学结果的理解门槛，有利于跨学科团队协作和临床转化。

## 8. 不足与局限
- **技术细节缺失**：摘要未提供 LLM 的选择、提示策略、幻觉控制机制、验证引擎的具体统计框架等，限制了对方法可信度的独立评估。
- **定量评估不足**：未报告任何数值指标（如检索精确率、临床一致性 kappa 系数等），难以客观衡量系统相比现有方法的提升程度。
- **数据多样性有限**：仅验证了肾脏和肺的三种疾病，在更广泛的组织类型（如肿瘤、脑组织）、技术平台和样本规模上的表现未知。
- **潜在偏差**：LLM 可能引入训练数据中的生物学偏见（如过度代表西方人群、特定文献结论），影响注释和假设生成的公正性。
- **计算资源与时效性**：若依赖大型商业模型，可能带来推理成本高、响应延迟和数据隐私问题；若使用开源模型，性能可能打折。
- **实用性障碍**：系统需要通过人类审计，能否真正替代专家判断或仅作为增强工具，还需前瞻性研究证明。

（完）
