---
title: "CodeCytos: AI-assisted spatial molecular imaging analysis via code-augmented agent action space"
title_zh: CodeCytos：通过代码增强的智能体行动空间实现AI辅助空间分子成像分析
authors: "Vo, H. Q., Ly, S. T., Wan, Z., Nguyen, A.-V., Zhao, H., Sheng, J., Wong, S. T. C., Nguyen, H. V."
date: 2026-06-03
pdf: "https://www.biorxiv.org/content/10.64898/2026.05.30.728935v1.full.pdf"
tags: ["query:autoresearch"]
score: 6.0
evidence: 用于空间分子成像分析的基于代码的推理代理
tldr: 传统组织图像分析软件依赖手动干预，缺乏自动化与自定义分析能力。CodeCytos框架通过编码增强的代理行动空间，实现与空间分子成像数据的动态交互和自定义细胞特征探索。在四个组织类型基准测试中，采用最小提示且融合域外少量编码示例，CodeCytos超越基线方法。该工作展示了代码驱动推理代理在加速生物标志物发现中的潜力。
source: biorxiv
selection_source: fresh_fetch
motivation: 传统组织图像分析依赖手动操作，缺乏自动化和自定义分析能力，限制空间细胞特征探索效率。
method: 提出CodeCytos编码推理代理框架，支持动态可编程空间分子成像数据交互，并融入域外少量编码示例提升推理。
result: 在四种组织类型数据集上，采用最小提示域外示例，CodeCytos性能超越现有基线方法。
conclusion: 代码驱动推理代理为空间分子成像自定义特征探索提供高效途径，有助于加速生物标志物发现。
---

## 摘要
传统的组织图像分析软件为细胞分析提供了基础功能，包括分割、形态特征提取和空间组织分析；然而，这些工具通常需要人工干预，缺乏与代码驱动自动化的无缝集成，限制了复杂空间组织研究的效率和可扩展性，同时由于其仅支持一组固定的预定义空间细胞特征，为自定义分析提供的灵活性有限。为了解决这些限制，我们提出了CodeCytos，一个基于编码的推理智能体框架，能够实现与空间分子成像数据的动态、可编程交互，并简化针对不同研究需求的自定义空间细胞特征探索。我们通过在四个专家策划的数据集上的案例研究展示了其实用性，这些数据集涵盖不同的组织类型，包括额叶皮层、非小细胞肺癌、胰腺和扁桃体，并在一个现实的最小提示设置下对其进行评估，在该设置中，生物科学家提出简单的问题，没有任务特定指令或先验上下文知识，对多个具有强编码能力的大语言模型骨干进行了基准测试。我们进一步表明，纳入领域无关的少样本上下文编码推理示例（从空间分析领域之外随机抽样），大大提高了性能，而不需要昂贵的专家制作的领域内演示；总体而言，CodeCytos优于基线方法，突显了代码驱动的推理智能体在支持空间分子成像中的自定义特征探索和加速生物标志物发现方面的潜力。

## Abstract
Conventional tissue image analysis software provides foundational capabilities for cellular analysis, including segmentation, morphological feature extraction, and spatial organization analysis; however, these tools often require manual intervention and lack seamless integration with code-driven automation, limiting efficiency and scalability for complex spatial tissue studies, while also offering limited flexibility for custom analyses by supporting only a fixed set of predefined spatial cellular features. To address these limitations, we propose CodeCytos, a coding-based reasoning agent framework that enables dynamic, programmable interaction with spatial molecular imaging data and streamlines the exploration of custom spatial cellular features across diverse research needs. We demonstrate its utility through case studies on four expert-curated datasets spanning distinct tissue types, including frontal cortex, non-small-cell lung cancer, pancreas, and tonsil, and evaluate it under a realistic minimal prompt setting in which bioscientists pose simple questions without task-specific instructions or prior contextual knowledge, benchmarking multiple large language model backbones with strong coding capabilities. We further show that incorporating domain-agnostic few-shot in-context coding-reasoning examples, randomly sampled from outside the spatial analysis domain, substantially improves performance without requiring costly expert-crafted in-domain demonstrations; overall, CodeCytos outperforms baseline approaches, highlighting the potential of code-driven reasoning agents to support custom feature exploration in spatial molecular imaging and accelerate biomarker discovery.