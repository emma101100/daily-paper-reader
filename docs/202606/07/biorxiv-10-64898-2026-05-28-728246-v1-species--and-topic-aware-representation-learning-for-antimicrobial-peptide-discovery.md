---
title: Species- and Topic-aware Representation Learning for Antimicrobial Peptide Discovery
title_zh: 面向抗菌肽发现的物种与主题感知表征学习
authors: "Padi, S., Mondal, K., Kaur, N., Hoogerheide, D. P., Heinrich, F., Mihailescu, E., Klauda, J. B., Cardone, A., Keyrouz, W."
date: 2026-06-01
pdf: "https://www.biorxiv.org/content/10.64898/2026.05.28.728246v1.full.pdf"
tags: ["query:autoresearch"]
score: 6.0
evidence: STAMP框架利用机器学习进行跨物种抗菌肽活性预测，实现自动化抗菌肽发现。
tldr: 抗生素耐药性构成全球健康挑战，高效发现抗菌肽(AMPs)的需求迫切。生成模型能产生大量候选序列，但湿实验验证成本高昂，精准预测最低抑菌浓度(MIC)至关重要。我们提出STAMP框架，融合蛋白质语言模型嵌入、物种条件与主题感知表征，实现跨物种预测。该框架在三个基准数据集上取得PCC=0.837、R2=0.70的优异性能，超越基线模型，并通过针对大肠杆菌和表皮葡萄球菌的实验验证与残基重要性分析，证实了其实用性并揭示了序列活性决定因素，为加速AMP发现与优化提供了可扩展的计算工具。
source: biorxiv
selection_source: fresh_fetch
motivation: 抗生素耐药性驱使高效抗菌肽发现，但生成候选肽的实验验证成本高，亟需精准的跨物种MIC预测方法。
method: 提出STAMP框架，融合蛋白语言模型嵌入、物种条件与主题感知表征，实现跨物种抗菌活性预测。
result: 在三个数据集上取得PCC=0.837和R2=0.70，优于基线，经实验验证并揭示残基重要性。
conclusion: STAMP为MIC预测提供了可扩展框架，加速抗菌肽发现与优化，是有效的计算工具。
---

## 摘要
抗菌素耐药性构成了重大的全球健康挑战，亟需高效策略来发现强效抗菌肽。尽管近期生成模型能够产生大量候选序列，但由于湿实验验证成本高、时间长，对所有生成的肽进行实验测试并不现实。因此，对肽类药效（通常以最低抑菌浓度衡量）的准确预测存在强烈需求。我们提出了 STAMP，一个面向抗菌肽发现的物种与主题感知表征学习框架。该统一机器学习框架可实现跨物种的抗菌肽活性预测。STAMP 将蛋白质语言模型嵌入与物种条件以及捕获序列水平模式的主题感知表征相结合，从而在单一模型内实现对多种细菌物种的泛化预测。我们在三个基准数据集上评估了 STAMP，其中包括两个先前发布的数据集和一个新整理的来自 DBAASP 的数据集，系统性地处理了重复和不一致问题。STAMP 在这些数据集上表现出强劲的预测性能，皮尔逊相关系数达到 0.837，R² 达到 0.70，优于多个基线模型。重要的是，我们进一步使用经实验测试对大肠杆菌和表皮葡萄球菌具有抗菌活性的肽验证了预测模型，展示了其实际应用能力。此外，残基级重要性分析揭示了决定抗菌活性的序列因素。综上，这些结果确立了 STAMP 作为最低抑菌浓度预测的可扩展框架，以及加速抗菌肽发现与优化的有效计算工具。

## Abstract
Antimicrobial resistance poses a major global health challenge, necessitating efficient strategies to discover potent antimicrobial peptides (AMPs). While recent generative models can produce many candidate sequences, experimentally validating all generated peptides in wet labs is impractical due to the high costs and time involved in such measurements. As a result, there is a strong demand for accurate predictions of peptide efficacy, typically measured as the minimum inhibitory concentration (MIC). We introduce STAMP, a framework for Species- and Topic-aware Representation Learning in AMP Discovery. This unified machine learning framework allows for cross-species predictions of AMP activity. STAMP integrates protein language model embeddings with species conditioning and topic-aware representations that capture sequence-level patterns, enabling generalizable predictions across multiple bacterial species within a single model. We evaluated STAMP on three benchmark datasets, which include two previously published datasets and a newly curated dataset derived from DBAASP, addressing duplicates and inconsistencies systematically. STAMP achieved strong predictive performance across these datasets, demonstrating a Pearson correlation coefficient (PCC) of 0.837 and an R2 of 0.70, outperforming several baseline models. Importantly, we further validated our prediction model using peptides that were experimentally tested for their antimicrobial activity against E.coli. and S.epidermidis bacteria, demonstrating its real-world applicability. Furthermore, residue-level importance analyses provide insights into the sequence determinants governing antimicrobial activity. Together, these results establish STAMP as a scalable framework for MIC prediction and an effective computational tool for accelerating AMP discovery and optimization.