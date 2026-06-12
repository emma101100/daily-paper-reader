---
title: Evaluating agentic AI for biological discovery in autonomous and copilot settings
title_zh: 评估自主与协作设定下面向生物发现的智能体人工智能
authors: "Johri, S., Pimenta, E. M., Yates, J., Fu, J., Bao, E. L., Jun, H., Reardon, B., Bacot, S., Shady, M., Fu, D., Mei, W., Camp, S. Y., Park, J., Van Allen, E."
date: 2026-06-09
pdf: "https://www.biorxiv.org/content/10.64898/2026.06.04.729919v1.full.pdf"
tags: ["query:autoresearch"]
score: 10.0
evidence: 评估用于生物发现的智能体 AI，重点关注开放式假设生成和对多模态证据的迭代推理。
tldr: 基于大语言模型的AI代理在生物发现中面临多模态异质数据挑战，其能力未知。本研究开发M3A框架，利用11种癌症多组学数据评估自主与协作设置下的代理表现。结果显示AI能有效系统性探索复杂数据，但领域专家在方法论指导和生物学综合上仍不可替代。该工作界定了当前AI代理的潜力与边界，为计算生物学中AI评估提供了框架。
source: biorxiv
selection_source: fresh_fetch
motivation: 评估基于大语言模型的AI代理在多组学单细胞数据生物发现中的能力，明确其在自主与协作模式下的局限性。
method: 开发M3A框架，利用11种癌症多组学单细胞数据，在自主和copilot设置下评估AI代理。
result: AI代理能有效系统性探索复杂多组学数据，但领域专家的方法论指导和生物学综合仍不可或缺。
conclusion: 研究界定了agentic AI在计算生物学中的潜力与局限，为评估生物学发现AI系统提供了框架。
---

## 摘要
基于大语言模型（LLM）的人工智能（AI）智能体的进展提高了它们执行结构化分析工作流程的能力，包括用于生物发现的标准生物信息学流程。然而，计算生物学很少仅由确定性的流程执行组成。生物数据集具有异质性和噪声，而有意义的发现通常需要开放式的假设生成和对多模态证据的迭代推理。这些挑战在多组学研究中尤为突出，其中配对的分子模态和异质的临床背景为发现创造了机遇与障碍。新兴的智能体AI系统在多大程度上能够支持或自动化这种科学发现模式，目前仍知之甚少。在此，我们利用涵盖11种癌症类型的多组学单细胞数据集，系统评估了智能体AI用于生物发现的能力与局限性。我们开发了多步骤多模态多组学智能体（M3A）框架，以支持在持久的多模态数据状态上进行LLM驱动的推理，并捕捉在自主和人类-AI协作设定下的智能体推理行为。通过该框架，我们在互补任务中评估了AI智能体，包括自主细胞类型注释、从基因程序中生成可证伪的生物学假设，以及测试人类参与和领域专业知识影响的协作实验。我们发现，当前的AI智能体擅长对复杂数据进行广泛、系统性的探索，而领域专家对于方法学指导和分析中的生物学综合仍然至关重要。总之，我们的结果界定了智能体AI在计算生物学中的当前潜力与边界，并为评估旨在支持生物发现的AI系统建立了一个框架。

## Abstract
Advances in large language models (LLMs)-based artificial intelligence (AI) agents have improved their ability to execute structured analytical workflows, including standard bioinformatic pipelines for biological discovery. However, computational biology rarely consists of deterministic pipeline execution alone. Biological datasets are heterogeneous and noisy, and meaningful discovery often requires open-ended hypothesis generation and iterative reasoning over multimodal evidence. These challenges are particularly evident in multi-omic studies, where paired molecular modalities and heterogeneous clinical contexts create both opportunities and obstacles for discovery. The extent to which emerging agentic AI systems can support or automate this mode of scientific discovery remains poorly understood. Here, we systematically evaluated the capabilities and limitations of agentic AI for biological discovery using multi-omic single cell datasets spanning 11 cancer types. We developed the Multistep Multimodal Multiomic Agentic (M3A) Framework to support LLM-driven reasoning over persistent multimodal data states and to capture agentic reasoning behavior in autonomous and human-AI copilot settings. Using this framework, we assessed AI agents across complementary tasks, including autonomous cell-type annotation, generation of falsifiable biological hypotheses from gene programs, and copilot experiments testing the effect of human involvement and domain expertise. We found that current AI agents are effective at broad, systemic exploration of complex data, whereas domain experts remain critical for methodological guidance and biological synthesis across analyses. Together, our results delineate the current potential and boundaries of agentic AI in computational biology, and establish a framework for evaluating AI systems designed to support biological discovery.

---

## 论文详细总结（自动生成）

### 1. 论文的核心问题与整体含义（研究动机和背景）

- **核心问题**：基于大语言模型（LLM）的智能体在自动化生物信息流程上已有进展，但生物发现并非仅仅是确定性流程执行，它需要开放式假设生成、对异质多模态数据的迭代推理。尤其在多组学单细胞数据中，配对分子模态与复杂临床背景使得AI支持或自动化这类科学发现的能力未被充分理解。论文旨在系统评估智能体AI在真实癌症多组学数据中的自主发现与人类协作能力，明确其潜力与局限。

- **整体含义**：为AI在计算生物学中的“发现导向”任务提供了基准框架，揭示当前智能体在广泛系统性探索上的优势，以及在方法指导和生物综合上对领域专家的依赖，提出人机混合架构是未来方向。

### 2. 论文提出的方法论

- **核心思想**：建立一个统一评估框架（M3A: Multistep Multimodal Multiomic Agentic），通过标准化执行环境、统一工具集、持久数据状态、递归多模态上下文整合和步骤级遥测，可控地捕捉LLM智能体在多步、多组学推理中的完整行为轨迹，实现对自主与协作模式的定量与机理性分析。

- **关键技术细节**：
  - **标准化执行环境**：基于Docker镜像，每次运行重置环境保证可重复性。
  - **专用工具集**：Python程序分析、终端访问、单细胞组学领域特定工具、文献检索（Google Search/PubMed等，屏蔽已发表研究链接防泄露）。
  - **递归多模态上下文整合**：将模型生成的文本、代码、图表等迭代纳入上下文窗口。
  - **持久数据状态**：AnnData等结构化对象跨步骤保持，支持中间结果复用。
  - **步骤级遥测**：记录每一步的意图、工具选择、输出及token用量等，支持决策轨迹分析。
  - **评估策略**：设计自主细胞类型注释（与专家标签对比）、可证伪假设验证（cNMF程序排序与TCGA独立队列统计排名对比）、人机协作实验（HITL/HOTL/全自主）并捕获用户行为与智能体动作分类，最后进行盲审专家评估。

- **算法/流程（文字说明）**：
  - **细胞注释评分**：基于构建的层次化本体树，将AI标签与GT标签映射至本体节点，按六个互斥等级（精确匹配、谱系正确、比GT更细、兄弟错误、可具体错误、谱系错误）计分。
  - **验证任务**：对HTAN单细胞cNMF程序进行无标注排名，同一程序在TCGA bulk RNA-seq中计算ssGSEA分数并与临床/分子终点关联，产生统计基准排序，计算Spearman秩相关及Top-1准确率。
  - **协作实验**：参与者分为领域专家、单细胞经验者、单细胞新手，在HOTL(仅干预重大错误)和HITL(主动干预)模式下完成四项生物推理任务，智能体动作和用户干预被分类统计，最终由原始研究第一作者盲审评分（质量、可信度、新颖性等）。

### 3. 实验设计

- **数据集/场景**：
  - **细胞注释任务**：来自HTAN的9个癌种（BRCA、CESC、CRC、GBM、HNSCC、OV、PDAC、SKCM、UCEC）的多患者snMultiome数据（146样本，646,057细胞），GT标签由各癌种工作组共识生成。
  - **验证任务**：HTAN 8个癌种的cNMF程序，TCGA独立队列（分子、病理、临床终点）作为外部验证；涵盖64个任务（分子、病理、生存三大类）。
  - **协作实验**：3个已发表研究数据集（LPS脂肪肉瘤、EAC食管腺癌、BRCA乳腺癌），snMultiome或snRNA/scATAC数据，由22名参与者（领域专家4名、单细胞经验者13名、单细胞新手5名，以及全自主运行3次）完成4项生物推理任务。

- **Benchmark对比**：
  - **指标**：细胞注释的灵敏度和特异性、细粒度正确率（6级评分）；程序排名Top-1准确率、Spearman秩相关、Top-3交换；盲审中质量/可信度/新颖性评分及排名。
  - **消融/比较**：主要对比不同交互模式（全自主 vs. HOTL vs. HITL）、不同用户经验水平（领域专家/有经验/新手）；替代动作分析（智能体考虑了但未实际执行的工具类别）。

- **公平性措施**：验证任务使用外部独立队列，终点数据与转录组数据来源正交；盲审时去除交互模式与背景标签，专家无法区分，确保客观性；文献检索屏蔽源研究链接防止数据泄露。

### 4. 资源与算力

- 论文未明确说明使用的GPU型号、数量或训练时长。其主要计算在于LLM推理（Claude Opus 4.6）和传统生物信息分析（cNMF、ssGSEA等），未涉及大规模模型训练，因此未提供相关算力详情。

### 5. 实验数量与充分性

- **主要实验组数**：
  - 细胞注释：9个癌种共约64万细胞，细粒度分析按类别流行度分层。
  - 验证任务：64个独立任务（8癌种 × 多类终点）。
  - 协作实验：27次运行（3数据集 × 3种模式：全自主1次/数据集 + HITL和HOTL各若干用户），用户动作分类上千步，盲审21组输出（HOTL/HITL/自主），对每项任务评估多个维度。

- **充分性与公平性**：实验覆盖多种癌症类型、多层次任务（从流程化注释到开放式发现），并通过独立验证、盲审和细致的混淆矩阵拆解减少主观偏差。协作实验的参与者数量和数据集较少，主要提供定性趋势，但结论按描述性呈现，未过度声称统计显著性。整体设计严谨，客观性较强，但协作组样本量小限制了普遍性结论。

### 6. 论文的主要结论与发现

- **细胞注释**：AI在常见细胞类型上特异性和灵敏度高，但稀有细胞类型易出现谱系错误，准确率随细胞流行度锐降。深度的推理步骤不代表更高的准确性，智能体倾向于使用scATAC做确认而非独立聚类，且不自动迭代质控。
- **生物程序排序**：AI在全64个任务中Top-1准确率30%（基线~11%），在信号强且区分度高的任务上表现更好，但存在系统性偏好：过度排名EMT/基质和免疫程序，低估代谢和神经程序，错误可解释且与训练文献偏差相关。
- **协作模式**：全自主运行步数更多，减少cNMF注释，增加调控分析；人机协作时用户干预集中在早期任务；领域专家在HITL中提前引导假设生成，把后期分析交予智能体；新手更多依赖文件管理和进度检查。
- **盲审**：全自主输出在某些任务中新颖性评分更高，HITL倾向复述已知生物学；随着任务复杂性增加，完全自主和缺乏单细胞经验的组合质量有所下降，领域专家对复杂综合任务依旧关键。多处协作产生的输出被原作者评为等同于或优于原发现。

### 7. 优点

- **真实多组学评估**：使用多个真实癌症snMultiome数据，突破许多研究仅用scRNA的局限。
- **多层次系统基准**：包括确定性注释、可证伪的假设验证、人机交互实验和盲审，覆盖发现全周期。
- **框架的精细遥测**：捕捉决策轨迹、替代行动考虑，可分析智能体推理机制。
- **消融分析深入**：分析流行度、信号强度、任务主题等对性能的影响，揭示结构化盲点。
- **创新性的验证方法**：将程序排序视为可证伪预测，通过独立队列统计验证，避免主观评判。
- **人机协作的量化**：按经验水平和交互模式分类用户干预与智能体行为，为未来架构设计提供依据。

### 8. 不足与局限

- **模型与工具单一**：仅评估Claude Opus 4.6，未比较其他LLM或开源模型，结论可能不普适于所有智能体。
- **协作实验样本小**：总参与者22人，每个数据集自主运行仅1次，统计效力有限，结果带描述性趋势。
- **顺序效应**：参与者先执行HOTL再HITL，可能带来学习效应，影响行为指标。
- **高度预配置环境**：协作为专家策划的预处理数据集和精心设计的提示，全自主运行本身即嵌入了大量领域知识，可能高估自主表现。
- **程序排序验证局限**：cNMF跨模态（单细胞→ bulk RNA-seq）转移可能引入模式差异，混杂程序稳健性。
- **稀有细胞与主题偏差**：稀有细胞和冷门生物学主题的泛化能力未经测试；主题排序偏差可能反映训练语料而非实际生物学。
- **缺乏长期发现迭代**：未评估智能体在多轮假设-验证-修订闭环中的能力，单次任务设计简化了真实发现过程。
- **未明确算力**：未提供推理成本或时延数据，难以评估实际效率和可扩展性。

（完）
