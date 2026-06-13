---
title: Reconstructing living materials as a computable design space with multi-agent reasoning
title_zh: 利用多智能体推理将活体材料重构为可计算的设计空间
authors: "Xiao, Y., Zeng, X., Yang, Z., Gu, J., Lu, Y., Wang, Y., Wen, H., Chen, M., Huang, Z., Hu, J., Liu, J., Sha, C., Xie, J., Li, H., Zhu, X., Zheng, S., Zhang, J., Zong, W., He, Z., Xu, Y., Zhou, X., Li, F., Liu, H., He, Q., Liu, L., Yu, Z."
date: 2026-06-09
pdf: "https://www.biorxiv.org/content/10.64898/2026.02.15.705954v2.full.pdf"
tags: ["query:autoresearch"]
score: 9.0
evidence: LiveMat利用多智能体推理将非结构化文献转化为活体材料的可计算设计空间，支持自动化科学发现。
tldr: "人工智能正加速科学发现，但现有框架多局限于分子或蛋白质等明确空间，活体材料因其功能源自细胞、基质及制造条件间的上下文耦合而极难建模。为此，研究者提出LiveMat，一个多智能体推理框架，它从非结构化文献中标准化34,215条记录，整合微生物和聚合物数据，构建连接活体组分、非生物基质与性能指标的知识图谱。基准测试显示，活体材料推理主要受限于跨域特征集成而非粗分类；LiveMat通过约束分解、一致性检查和专家锚定排序克服此问题，并在伤口愈合任务中优先推荐顶尖体内性能的四组分设计。这为可解释、证据驱动的活体材料发现奠定了可扩展基础设施，有望加速生物医学材料创新。"
source: biorxiv
selection_source: fresh_fetch
motivation: 活体材料的功能实现依赖多因素上下文耦合，计算建模极具挑战，缺乏从文献中系统整合知识的框架。
method: "提出LiveMat多智能体框架，标准化34,215条文献记录，构建包含微生物-聚合物关联的知识图谱，用约束分解和溯源提取保障质量。"
result: 基准测试表明跨域特征集成是主要瓶颈，LiveMat在伤口愈合任务中优先筛选出具有顶尖体内性能的四组分设计。
conclusion: 该工作证明了多智能体推理可将非结构化文献转化为可操作设计空间，为活体材料理性发现提供新范式。
---

## 摘要
人工智能正日益用于加速科学发现，但最成功的框架通常在明确定义的分子、蛋白质或材料空间内运行。活体材料提出了更艰巨的计算挑战，因为功能涌现于细胞、基质、制造工艺和评估条件之间依赖于情境的耦合。在此，我们介绍LiveMat，一个多智能体推理框架，将非结构化文献转化为活体材料的可计算设计空间。LiveMat标准化了34,215条活体材料记录，将16,769个微生物条目和17,446个聚合物条目整合成一个知识图谱，连接活体成分、非生物基质、功能输出、评估情境和性能指标。在五个大型语言模型上的基准测试表明，活体材料推理的主要限制在于跨领域特征整合，而非粗略分类。LiveMat通过约束分解、溯源感知提取、一致性检查和专家锚定排名克服了这一限制。在一项前瞻性伤口愈合任务中，它优先考虑了一种四组分设计，并展示了先进的体内性能，从而为可解释、基于证据的活体材料发现建立了可扩展的基础设施。

## Abstract
Artificial intelligence is increasingly used to accelerate scientific discovery, but most successful frameworks operate within well-defined molecular, protein or materials spaces. Living materials present a more formidable computational problem because functions emerge from context dependent coupling among cells, matrices, fabrication processes and evaluation conditions. Here we introduce LiveMat, a multi-agent reasoning framework that transforms unstructured literature into a computable design space for living materials. LiveMat standardizes 34,215 living material records, integrating 16,769 microorganism and 17,446 polymer entries into a knowledge graph linking living components, abiotic matrices, functional outputs, evaluation contexts and performance metrics. Benchmarking across five large language models shows that living material reasoning is limited mainly by cross-domain feature integration rather than coarse classification. LiveMat overcomes this limitation through constraint decomposition, provenance-aware extraction, consistency checking and expert-anchored ranking. In a prospective wound-healing task, it prioritizes a four-component design with state-of-the-art in vivo performance, establishing a scalable infrastructure for interpretable, evidence-grounded living material discovery.

---

## 论文详细总结（自动生成）

# 1. 论文的核心问题与整体含义（研究动机和背景）

- **研究动机**：人工智能正加速科学发现，但现有成功框架多局限于分子、蛋白质或材料等结构明确的设计空间。活体材料（living materials）的功能源于活细胞、非生物基质、制造工艺与评估条件之间极其复杂的上下文耦合，这使得其设计空间极难建模和计算探索。
- **核心挑战**：活体材料的知识分布在大量非结构化文献中，缺乏系统整合与可计算表示的方法，导致跨领域特征难以被有效集成和推理。
- **整体含义**：作者提出，如果能将碎片化的文献知识重构为可计算、可推理的设计空间，便有望实现可解释且证据驱动的活体材料理性发现，从而加速该领域的创新。

# 2. 论文提出的方法论

- **核心思想**：设计一个多智能体推理框架 LiveMat，将非结构化科学文献自动转化为结构化的知识图谱，并在此基础上进行活体材料的跨域推理与设计排序。
- **关键技术细节**：
  - **文献标准化与知识图谱构建**：从大量文献中标准化提取 34,215 条活体材料记录，整合 16,769 个微生物条目和 17,446 个聚合物条目，构建连接“活体成分—非生物基质—功能输出—评估情境—性能指标”的知识图谱。
  - **约束分解**：将复杂的活体材料设计问题分解为可独立处理的子约束，以便多智能体分工协作。
  - **溯源感知提取（provenance‑aware extraction）**：在信息抽取时保留文献来源与上下文证据，保证信息的可追溯性。
  - **一致性检查**：对多源抽取的信息进行逻辑与实验条件的交叉核验，滤除矛盾记录。
  - **专家锚定排名（expert‑anchored ranking）**：利用已有专家知识作为锚点，对候选设计进行排序，从而在伤口愈合等前瞻性任务中突出最优组合。
  - **流程形式**：整体流程为“文献输入 → 多智能体协同信息提取与校验 → 知识图谱集成 → 跨域特征融合与推理 → 设计优先级排序”，未披露严格数学公式。

# 3. 实验设计

- **数据集/场景**：
  - **核心数据集**：从非结构化文献中标准化得到的 34,215 条活体材料记录，及其衍生的知识图谱。
  - **应用场景**：活体材料设计空间的基准推理能力测试，以及前瞻性伤口愈合任务的实际筛选。
- **基准测试（Benchmark）**：
  - 针对活体材料推理任务，在**五个大型语言模型（LLM）**上进行基准评测。
  - 评测重点并非简单的粗略分类，而是衡量模型在**跨域特征整合**（将微生物、聚合物、工艺、性能等异质信息关联推理）上的表现。
- **对比方法**：
  - 与五个 LLM 的基线推理结果直接对比，以证明 LiveMat 在克服跨域集成瓶颈方面的优势。
  - 在前瞻性伤口愈合任务中，将 LiveMat 优先选出的四组分设计与文献中已知的体内性能数据进行对比验证。

# 4. 资源与算力

- 论文摘要及提供的元数据中**未明确提及**所使用的 GPU 型号、数量、训练时长等算力资源信息。由于 LiveMat 框架的核心在于知识图谱构建与多智能体协调推理，而非大模型的大规模预训练，其算力消耗可能更多依赖于文献处理和模型调用，但具体数字无从得知。

# 5. 实验数量与充分性

- **实验组数概览**：
  - 构建并标准化了 34,215 条记录的知识图谱，本身即涉及大规模数据处理与质量验证。
  - 在五个 LLM 上进行了基准测试（至少覆盖 5 种模型对比）。
  - 完成了一项前瞻性体内伤口愈合任务，筛选出四组分设计并验证其顶尖性能。
- **充分性与公平性**：
  - 从摘要看，实验覆盖了数据构建、基准对比和真实案例验证多个层面，设计较为立体。
  - 五个 LLM 的对比为客观评估提供了基础；前瞻性任务采用体内实际性能作为金标准，增强了可信度。
  - 然而，是否包含消融实验（例如移除约束分解或一致性检查模块后的性能变化）、不同超参数敏感性分析，以及是否在更多疾病或材料类型上验证等，均未在摘要中体现，其充分性需待全文才能准确评估。

# 6. 论文的主要结论与发现

- **活体材料推理的瓶颈**：基准测试表明，当前 AI 在活体材料上的主要限制不是粗略分类能力，而是**跨领域特征的深度融合与推理**。
- **LiveMat 的有效性**：通过约束分解、溯源感知提取和一致性检查，LiveMat 成功克服了这一瓶颈，并实现了基于证据的设计优先级排序。
- **前瞻性验证**：在伤口愈合任务中，LiveMat 优先推荐的一种**四组分活体材料设计**展现出了**顶尖的体内性能**，证明了该框架能将文献知识转化为实际可用的创新方案。
- **范式意义**：工作为解释性强、可追溯的活体材料发现建立了可扩展的基础设施，开启了从非结构化文献到自动化科学发现的新范式。

# 7. 优点（方法与实验设计的亮点）

- **知识整合的系统性**：首次将零散的非结构化文献大规模重构为活体材料的可计算知识图谱，打通了从文献到设计的壁垒。
- **跨域推理的针对性**：抓住了活体材料最棘手的“上下文耦合”问题，通过约束分解和专家锚定等手段，直接针对跨域特征集成这一核心挑战。
- **证据链的完整性与可解释性**：溯源感知提取和一致性检查保证了每条推理都有文献证据支持，避免了黑箱式预测，增强了结果的可信度和可审核性。
- **实验从基准到应用闭环**：结合多模型基准测试与真实体内伤口愈合验证，展示了框架的通用推理能力和实际转化潜力，实验设计完整。

# 8. 不足与局限

- **覆盖范围的潜在偏差**：知识图谱完全基于已发表文献，可能受限于文献本身的发表偏倚（如阳性结果更易发表），导致设计空间中被忽视的失败案例未能充分体现。
- **任务泛化性未充分验证**：前瞻性验证目前仅展示在伤口愈合任务上，其在其他活体材料应用场景（如自修复、环境修复、生物传感等）中的表现尚不明确。
- **算力与成本未评估**：摘要未提及构建知识图谱和运行多智能体系统的实际计算成本，其可扩展至百万级文献的可行性有待探讨。
- **方法细节透明度不足**：因仅有摘要，多智能体协作机制、约束分解的策略、专家锚点如何自动获取等关键技术细节未展开，暂时难以评估其复现难度和潜在局限性。

（完）
