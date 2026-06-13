---
title: Do Larger Models Really Win in Drug Discovery?A Benchmark Assessment of Model Scaling in AI-Driven Molecular Property and Activity Prediction
title_zh: 更大模型是否真的在药物发现中胜出？人工智能驱动的分子性质与活性预测中模型规模化的基准评估
authors: "Guo, J., Ding, S."
date: 2026-06-08
pdf: "https://www.biorxiv.org/content/10.64898/2026.04.29.721568v3.full.pdf"
tags: ["query:autoresearch"]
score: 9.0
evidence: 评估分子性质预测中模型缩放的基准，直接关联AI用于科学自动发现。
tldr: 随着大模型兴起，药物发现中倾向使用超大预训练模型，但缺乏公平比较。本研究在26个ADME/毒性/生物活性端点、三种难度递增的数据分割下，系统对比经典ML、GNN、分子序列模型和LLM。经典ML在随机分割中表现最佳且总体胜率最高；大模型仅在难分割下部分任务中优于经典方法，且优势依赖训练设置；模型间微小差异不显著。强调预测性能取决于模型与任务、验证场景的匹配，而非单纯规模，紧凑专用模型仍具高度实用性。
source: biorxiv
selection_source: fresh_fetch
motivation: 随着分子基础模型和大语言模型流行，业界普遍认为模型越大预测性能越好，但缺乏系统性基准评估。
method: 构建26个ADME/毒性/生物活性端点、16万+标签的基准，在随机、骨架和结构分离三种5折CV下对比经典ML、GNN、序列模型与LLM。
result: "经典ML整体胜率47.4%居首，GNN和序列模型在难分割下部分任务更优，但依赖训练设置；模型间差异多不显著。"
conclusion: 预测性能不取决于模型规模，而在于模型-任务-验证场景的匹配；紧凑专用模型仍高度实用，大模型在低数据SAR推理中增值。
---

## 摘要
分子基础模型和大语言模型的快速发展，促使人们以规模为中心看待人工智能在药物发现中的应用，期望更大的预训练模型能够取代基于经典机器学习和针对单任务训练的图神经网络等紧凑型化学信息学模型。我们在涵盖ADME、毒性和生物活性三类共26个终点上检验这一假设，涉及165541条终点级别的化合物标注记录。基准测试包含78个终点和划分条目，对应26个终点在三种划分方案下的评估：随机划分、Murcko骨架划分和结构分离的五折交叉验证。按从易到难的顺序，这些划分分别近似于封闭库上的回顾性评估、从苗头化合物到先导化合物阶段的骨架扩展，以及新化学型上的库扩展。每个条目包含两项任务和指标比较，共计156组对比。在所有对比中，经典机器学习提供了最大比例的最优条目（47.4%），其次是预训练的分子序列模型（28.8%）、图神经网络（21.8%）和基于大语言模型的构效关系基线（1.9%）。经典机器学习在随机划分的内插任务中占主导地位，并且整体上仍是最大的赢家类别。图神经网络和序列模型在主最优留出验证的一些较难划分方案中具有竞争力，但在固定的最终窗口验证下，它们的严格获胜比例下降，表明其中部分收益依赖于训练设置和模型选择。成对自助法分析表明，不应将单个模型间的微小数值差异视为决定性胜利。来自训练折的构效关系知识改善了许多GPT5.5-SAR和Opus4.7-SAR的指标，但并未使基于规则的推理成为监督预测器的通用替代品。紧凑的专业化模型在分子性质和活性预测中仍然非常有效。更大的模型在数据有限情况下的构效关系解读和推理中能增加价值，但预测性能取决于模型、任务和验证场景之间的匹配，而不仅仅取决于规模。

## Abstract
The rapid growth of molecular foundation models and large language models (LLMs) has encouraged a scale centred view of AI in drug discovery, in which larger pretrained models are expected to supersede compact cheminformatics models based on classical machine learning (classical ML) and graph neural networks (GNNs) trained for individual tasks. We test this assumption across 26 endpoints grouped into ADME, toxicity and bioactivity classes, covering 165,541 endpoint level compound label records. The benchmark contains 78 endpoint and split entries, corresponding to 26 endpoints evaluated under three split protocols: random, Murcko scaffold and structure separated 5-fold cross validation (CV). Ordered from easiest to hardest, these splits approximate retrospective evaluation on a closed library, scaffold expansion in hit to lead, and library expansion on novel chemotypes. Each entry contributes two task and metric comparisons, giving 156 comparisons in total. Across these comparisons, classical ML provides the largest share of best performing entries (47.4%), followed by pretrained molecular sequence models (28.8%), GNNs (21.8%) and LLM based SAR baselines (1.9%). Classical ML dominates random split interpolation and remains the largest winner family overall. GNN and sequence models are competitive in selected harder split protocols under the primary optimal held-out readout, but their strict winner shares decrease under a fixed final-window readout, indicating that some of these gains depend on training settings and model selection. Paired bootstrap analyses indicate that small numerical differences between individual models should not be read as decisive victories. SAR knowledge from training folds improves many GPT5.5-SAR and Opus4.7-SAR metrics but does not make rule based reasoning a universal substitute for supervised predictors. Compact specialized models remain highly effective for molecular property and activity prediction. Larger models add value for SAR interpretation and reasoning in low data settings, but predictive performance depends on the fit among model, task and validation scenario, not on scale alone.

---

## 论文详细总结（自动生成）

## 1. 论文的核心问题与整体含义

- **研究动机**：近年来分子基础模型和大语言模型（LLM）快速发展，药物发现领域逐渐形成“规模至上”的观念，即模型参数量越大，分子性质与活性预测性能越强，有望取代传统的紧凑型模型（如经典机器学习、图神经网络）。但这种假设缺乏系统、公平的基准评估。
- **核心问题**：更大的预训练模型在分子性质与活性预测任务中是否确实优于经典的、面向单任务训练的紧凑模型？性能增益究竟来自模型规模，还是来自任务特性、训练设置和验证场景的匹配？
- **整体含义**：论文通过构建覆盖 ADME、毒性、生物活性三大类共 26 个终点的基准，在三种难度递增的数据分割下进行系统对比，挑战“大即好”的流行观念，强调预测性能的根本在于模型、任务与验证场景的适配，而非单纯的参数规模。

## 2. 论文提出的方法论

- **整体框架**：采用多模型、多终点、多分割方案的系统性基准测试，定量比较经典机器学习（经典 ML）、图神经网络（GNN）、预训练分子序列模型以及基于大语言模型的构效关系（SAR）推理基线在分子性质与活性预测上的表现。
- **数据分割策略**：为模拟药物发现中从简单到困难的评价场景，设计三种五折交叉验证（5‑fold CV）方案：
  - **随机分割（Random Split）**：近似封闭化合物库上的回顾性评估（最易，内插为主）。
  - **Murcko 骨架分割（Scaffold Split）**：按 Murcko 骨架划分，模拟从苗头化合物到先导化合物阶段的骨架扩展（中难度）。
  - **结构分离分割（Structure‑Separated Split）**：类似新化学型上的库扩展（最难，外推性强）。
- **任务与指标**：每个终点在每种分割下包含两项任务和指标对比（可能涉及分类和回归的多种评价指标），共计 156 组模型×任务×指标组合。使用“胜率”统计各类模型在组间表现最优的比例。
- **显著性检验**：利用成对自助法（Paired Bootstrap）评估单个模型间数值差异是否具有统计显著性，避免将微小波动解读为决定性胜利。
- **LLM‑SAR 基线的知识注入**：从训练折提取构效关系知识用于指导 GPT5.5‑SAR 和 Opus4.7‑SAR 的推理，考察基于规则的推理能否替代监督预测模型。

## 3. 实验设计

- **数据集**：共包含 26 个终点，涵盖 ADME（吸收、分布、代谢、排泄）、毒性和生物活性三类性质，总记录数约 165,541 条终点级别的化合物标注。具体终点名称未在元数据中列出，但范围覆盖药物发现中常见的分子属性预测任务。
- **基准构成**：26 个终点 × 3 种分割方案 = 78 个“终点‑分割”条目。每个条目进行两项任务与指标对比，最终形成 156 组模型性能比较。
- **对比方法**：
  - **经典机器学习**（Classical ML）：基于固定分子指纹（如 ECFP、MACCS 等）的传统算法（如随机森林、XGBoost 等）。
  - **图神经网络**（GNN）：面向单任务训练的分子图表示模型。
  - **预训练分子序列模型**（Pretrained Molecular Sequence Models）：如基于 SMILES 序列的大规模预训练模型，在目标任务上微调。
  - **LLM 基线**：利用大语言模型直接进行构效关系推理的方法，包括 GPT5.5‑SAR、Opus4.7‑SAR，并对比是否注入训练折 SAR 知识的效果。
- **评估层面**：
  - 主最优留出验证（primary optimal held‑out readout）：从训练设置（如超参数）中选取在验证集上最优的模型进行评估。
  - 固定最终窗口验证（fixed final‑window readout）：采用统一固定的训练配置和最终模型检查点进行评估，以消除训练过程差异带来的“择优”偏袒。

## 4. 资源与算力

- **说明**：从提供的论文摘要和元数据中，**未明确提及**所使用 GPU 的型号、数量、单次训练时长或总计算开销。文中仅指出进行了大规模系统性比较，可能涉及对经典 ML、GNN 和预训练序列模型的训练与验证，以及 LLM 的推理调用，但未能获知具体算力细节。

## 5. 实验数量与充分性

- **实验规模**：
  - 总计 78 个“终点‑分割”条目，每个条目对应两组任务与指标对比，总计 **156 组模型性能比较**。
  - 对 LLM‑SAR 基线还进行了**是否注入训练折 SAR 知识**的消融式对比。
  - 除了主最优留出验证，还引入了**固定窗口验证**以检验训练设置依赖对排名的影响。
  - 使用**成对自助法**检验单个模型比较的显著性，排除随机波动误导。
- **充分性与公平性**：
  - 从覆盖的终点类型（ADME/毒性/生物活性）、分割方案（三种难度）、模型类别（经典 ML、GNN、序列模型、LLM）以及评价维度（多指标、双验证设置）来看，实验设计**系统而全面**，**公平性较高**。
  - 通过固定窗口验证消除了可能存在“择优”带来的偏差，增强了结论的可靠性。
  - 不足之处在于：未提供超参数搜索空间、训练重复次数、指标种类（AUC、RMSE 等）的具体细节，因此部分实验公平性细节无法完全判断。

## 6. 论文的主要结论与发现

- **整体胜率**：在所有 156 组比较中，**经典机器学习**提供了最大比例的最优条目（**47.4%**），大幅领先其他模型类，是总体表现最强的“家族”。
- **模型类别排名**：其余依次为预训练分子序列模型（28.8%）、图神经网络（21.8%）和 LLM‑SAR 基线（1.9%）。
- **任务难度影响**：经典 ML 在随机分割（内插）任务中占据绝对主导地位；GNN 和序列模型在骨架分割、结构分离等较难的外推任务中表现出一定竞争力，但这种优势**依赖于训练设置和模型选择**（在固定窗口验证下严格获胜比例下降）。
- **差异不显著**：通过成对自助法分析发现，单个模型之间的微小数值差异往往**不构成统计上的决定性胜利**，不能据此轻易断言某个模型“胜出”。
- **LLM 推理局限**：注入训练折 SAR 知识能提升 LLM 部分指标，但基于规则的推理**并不能成为监督预测模型的通用替代方案**。
- **核心论断**：预测性能的差异**并非取决于模型规模**，而是要依赖于模型架构、具体任务和验证场景之间的匹配；紧凑的专用模型在分子性质与活性预测中仍然高度有效。大模型的价值更多体现在数据有限时的构效关系解读与推理，而非普适的预测精度提升。

## 7. 优点

- **系统性基准**：首次在同一框架下同时比较经典 ML、GNN、序列预训练模型和 LLM，覆盖 26 个药物发现相关终点和三种不同难度的分割，填补了相关系统性评估的空白。
- **实验设计严谨**：引入三种难度递增的验证场景（内插、骨架扩展、新型库扩展），贴近真实药物研发流程；采用主最优留出和固定窗口两种验证方式从而识别训练设置带来的虚假性能增益；用成对自助法控制比较的统计显著性。
- **结论客观务实**：用数据打破了“越大越好”的迷思，强调了模型‑任务‑场景适配的重要性，对工业界和学术界药物发现 AI 方法选择具有实际指导意义。
- **对 LLM 的清晰定位**：明确指出大模型在 SAR 推理中的辅助价值，同时划清了其与监督预测模型的边界，避免了盲目追捧。

## 8. 不足与局限

- **数据集范围有限**：仅包含 26 个 ADME/毒性/生物活性终点，可能未涵盖某些特殊的性质预测任务（如晶型预测、合成可及性等），泛化结论需谨慎。
- **大模型代表性不足**：LLM 基线仅使用 GPT5.5‑SAR 和 Opus4.7‑SAR，未纳入当前更前沿的大规模分子基础模型（如 GIMLET、MolFM 等），也未尝试参数规模更大的通用 LLM 的微调变体。
- **训练与评估细节缺失**：未公布具体超参数搜索策略、训练重复次数、评价指标名称及计算方式，使得部分实验的可复现性和公平性难以完整评估。
- **无算力与成本分析**：论文未涉及不同模型的训练/推理计算开销和时间成本的对比，然而在工业落地中，紧凑模型的经济性往往是大模型难以匹敌的。
- **缺乏化学机制的可解释性**：虽然使用了骨架分割等提高评价可信度，但未进一步分析模型在不同化学空间或作用机制下的表现模式，难以提供化学层面的洞察。

（完）
