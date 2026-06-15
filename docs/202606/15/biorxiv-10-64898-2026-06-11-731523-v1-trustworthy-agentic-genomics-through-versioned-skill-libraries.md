---
title: Trustworthy agentic genomics through versioned skill libraries
title_zh: 通过版本化技能库实现可信的自主智能基因组学
authors: "Corpas, M., Iacoangeli, A., Bourdenx, M., Aldraimli, M., Skene, N., Fatumo, S., Guio, H."
date: 2026-06-15
pdf: "https://www.biorxiv.org/content/10.64898/2026.06.11.731523v1.full.pdf"
tags: ["query:autoresearch"]
score: 9.0
evidence: 利用版本化技能库确保可信的智能体基因组学，提供溯源和结构化工件。
tldr: 基因学领域正采用AI代理从自然语言指令解读基因组，但信任问题突出。本研究提出将验证决策逻辑编码为版本化技能并作为代码执行，而非依赖模型推理。实验表明，架构决定可信赖性：模型直接推理或检索增强均不安全，而执行代码实现精确、可审计且跨模型一致的药物基因组映射，消除了解读中的祖先梯度。该通用架构为大规模可信赖的代理基因解读奠定基础。
source: biorxiv
selection_source: fresh_fetch
motivation: 基因组学采用自主AI代理进行解释，但信任构建滞后，在错误可测量且致命的药物基因组学中尤为关键。
method: "在110个药物基因案例上对9个前沿LLM进行44,550次评分评估，并测试对7,000多例不同祖先个体的真实星等位基因双倍型的解读，比较推理、检索与编码执行三种架构。"
result: 可信赖性取决于架构而非模型；模型推理不安全且检索反而增加致命错误；将决策逻辑编码为代码执行生成了精确、一致且可审计的映射，消除了祖先梯度差异。
conclusion: 本研究建立了一种通用、可审计的架构，通过版本化技能编码并执行，实现大规模可信赖的代理基因解读。
---

## 摘要
基因组学正在采用自主人工智能代理，它们根据自然语言指令解读基因组的速度，快于建立信任它们的手段。我们首次报告了大规模受控评估，以确定在自主基因组分析流程中，正确性必须位于何处，才能使系统在临床规模上可信。利用药物基因组学这一错误可衡量且有时致命的领域，我们在110个药物基因组学案例中对九个前沿大语言模型进行了44,550次评分评估，并测试了模型对来自三个不同祖先背景的7000多名个体的真实星号等位基因双倍型的解读。事实证明，可信性是流程架构的属性，而非模型的属性。让模型推理是随机的且不安全，通过检索将其锚定在正确指南上反而增加了致死类错误。将经过验证的决策逻辑编码为版本化技能，并以代码形式执行，使药物基因组学映射变得精确、可审计且在不同模型中保持一致，将所有残留错误限制在单一的输入解读步骤中。在个体基因组上，未经防护的模型解读会沿着祖先梯度下降；执行则从临床映射中消除了这一梯度，并将其转移到输入调用器的可审计完整性上。这为大规模可信的自主智能基因组解读建立了一种可推广、可审计的架构。

## Abstract
Genomics is adopting autonomous AI agents that interpret genomes from natural-language instructions faster than it is building the means to trust them. We report the first large-scale controlled evaluation of where, in an agentic genomic pipeline, correctness must reside for the system to be trustworthy at clinical scale. Using pharmacogenomics, a domain where errors are measurable and sometimes lethal, we benchmarked nine frontier large language models across 44,550 scored evaluations on 110 pharmacogenomic cases, and tested model interpretation of real star-allele diplotypes from more than 7,000 individuals in three ancestrally diverse populations. Trustworthiness proved to be a property of pipeline architecture, not of the model. Letting the model reason was stochastic and unsafe, and grounding it in the correct guidelines by retrieval paradoxically increased lethal-class errors. Encoding the validated decision logic as a versioned skill and executing it as code made the pharmacogenomic mapping exact, auditable and identical across models, confining all residual error to a single input-interpretation step. On individual genomes, unguarded model interpretation degraded along an ancestry gradient; execution removes this gradient from the clinical mapping, relocating it to the auditable completeness of the input caller. This establishes a generalisable, auditable architecture for trustworthy agentic genome interpretation at scale.

---

## 论文详细总结（自动生成）

### 1. 论文的核心问题与整体含义（研究动机和背景）
- **核心问题**：基因组学领域正在快速部署能够根据自然语言指令解读基因组的自主 AI 代理，但构建对它们的信任手段（即验证其输出正确性）严重滞后。在药物基因组学（pharmacogenomics）这一可直接衡量错误、且错误可能致命的场景中，这种信任危机尤为突出。
- **整体含义**：研究旨在系统性地回答：在一个自主基因组分析流程中，为使其在临床规模上可信，正确性必须处在流程的哪个环节？换言之，是模型本身的推理能力，还是工作流的架构设计决定了最终的可信赖性。

### 2. 论文提出的方法论
- **核心思想**：将经过验证的决策逻辑**打包为版本化技能（versioned skills）**，并以**代码形式执行**，而不是依赖大语言模型（LLM）的自由推理或检索增强。
- **关键技术细节与流程**：
  - 设计了三种基因组解读架构进行对比：
    1. **模型直接推理**：让 LLM 根据自然语言指令和输入数据自行推断药物基因组映射。
    2. **检索增强生成（RAG）**：在推理前通过检索将模型锚定在正确的指南上。
    3. **代码执行架构（版本化技能）**：将已由专家验证的决策规则编码为可执行代码，以确定性的方式映射输入，不依赖模型生成答案。
  - 流程中将误差源头限制在单一的**输入解读步骤（input-interpretation step）**，该步骤由**输入调用器（input caller）**完成（如将原始星号等位基因双倍型转化为规范输入），后续映射完全由可审计的代码保证。
  - 技能被**版本化**，以保证可追溯性和可审计性。

### 3. 实验设计
- **数据集/场景**：
  - **药物基因组案例**：110 个经过精心构建的药物基因组学案例，用于对 LLM 的输出进行评分。
  - **真实个体数据**：来自三个祖先差异较大人群的 7,000 多名个体的真实星号等位基因双倍型（star-allele diplotypes），用于测试模型对真实基因组的解读。
- **基准（Benchmark）**：
  - 以准确的药物基因组临床映射为金标准，评估不同流程架构下错误的数量与严重性（特别是致死类错误）。
- **对比方法**：
  - 九种前沿大语言模型（未在摘要中具体列出名称，但提及了 nine frontier large language models）。
  - 三种流程架构之间的横向对比：纯模型推理、检索增强推理、版本化技能代码执行。

### 4. 资源与算力
- 论文摘要及提供的元数据中**未明确说明使用的 GPU 型号、数量或训练时长**。仅在方法中提及进行了 44,550 次评分评估，涉及 9 个前沿 LLM，但计算资源细节缺失。

### 5. 实验数量与充分性
- **实验数量**：
  - 对 9 个 LLM 在 110 个药物基因组案例上进行 44,550 次评分评估（应为系统性组合不同模型、案例和架构的试验）。
  - 对来自三个祖先背景的 7,000 余名个体的真实双倍型进行了实际解读测试。
  - 对比了三种根本不同的架构设计，构成完整的消融对比。
- **充分性与公平性**：
  - 实验规模大（数万次评估，数千份真实个体数据），覆盖多个前沿模型和多种祖先背景，具有统计学说服力。
  - 对比设计公平：对同一组案例和同一批模型，仅改变流程架构，排除了模型本身能力差异的干扰，直接回答了“架构决定可信赖性”这一核心命题。

### 6. 论文的主要结论与发现
- **可信赖性是流程架构的属性，而非模型的属性**。无论模型多强，若将其推理直接用于临床映射，结果既随机又不安全。
- **检索增强反而可能增加致命错误**：将模型通过检索锚定到正确指南上并未消除错误，反而引入了致死类错误（lethal-class errors）的风险。
- **代码执行架构能实现精确、可审计且跨模型一致的映射**：将经验证的决策逻辑编码为版本化技能并执行，能够消除模型之间的映射差异，并将所有残留误差局限在可审计的输入解读步骤中。
- **消除祖先梯度差异**：未加防护的模型解释在个体基因组上会沿着祖先梯度（ancestry gradient）退化；而使用代码执行架构可将这一退化效应从临床映射中移除，使其只出现在输入调用器的可审计完整性上，从而保障了下游映射的公平性。

### 7. 优点（方法或实验设计的亮点）
- **首创性**：首次在临床规模上对自主基因组代理的信任根基进行大规模受控评估。
- **架构驱动的洞见**：通过直接比较三种基础性架构（推理、检索、执行），清晰地将可信性归因于流程设计，而非模型能力，对负责任 AI 的实践具有指导意义。
- **现实世界验证**：使用来自三个不同祖先背景的 7,000 余份真实个体基因组数据，验证了方法在多样人群上的稳健性，并揭示了祖先偏差的来源。
- **可审计性与可推广性**：提出的版本化技能执行架构天然支持版本控制与审计，为今后在更广泛的基因组解读任务中构建可信代理提供了可重复的范式。

### 8. 不足与局限
- **研究范围局限于药物基因组学**：虽然架构声称可推广，但实验验证仅在一类临床解读任务（药物基因映射）中进行，对其他基因组分析子领域（如罕见病变异解读、多基因风险评分）的有效性尚需证明。
- **输入调用器仍是单点依赖**：整个系统的可信度最终取决于输入解读步骤（星号等位基因双倍型的调用）的完整性，若该环节本身存在系统偏差或更新延迟，仍可能影响下游结果，文中未详细讨论如何确保这一前序环节的可靠性。
- **计算资源与执行细节未披露**：缺少对所用模型版本、推理硬件等信息，这限制了外部对其评估成本及可复现性的判断。
- **生态依赖性**：可执行技能的正确性依赖于专家预先验证和版本管理流程，若维护不当，代码本身的错误可能被固化，论文未详细探讨长期维护机制。

（完）
