---
title: AI-Discovered Cognitive Models Reveal Novel Insights into Human and Animal Learning
title_zh: 人工智能发现的认知模型揭示人类与动物学习的新洞察
authors: "Kasenberg, D., Castro, P. S., Eckstein, M. K., Elteto, N., Dabney, W., Wang, C. L., Engelcke, M., Mohanta, R., Dev, A., Botvinick, M. M., Tomasev, N., Turner, G. C., Costa, V. D., Daw, N. D., Stachenfeld, K. L., Miller, K. J."
date: 2026-05-21
pdf: "https://www.biorxiv.org/content/10.64898/2026.05.18.725921v1.full.pdf"
tags: ["query:autoresearch"]
score: 6.0
evidence: 使用AI自动发现认知模型
tldr: 传统认知模型需专家手工设计，耗时且可能遗漏重要模式。本文提出AI驱动的模型发现方法，从行为数据中自动拟合灵活模型并解释，在被试行为数据集上发现了优于手工模型的新认知机制。该方法推动了自动化科学发现中模型生成的实践，尽管未完整包含实验循环，却是AI for Science的重要一步。
source: biorxiv
selection_source: fresh_fetch
motivation: 使用AI自动发现认知模型。
method: 方法与实现细节请参考摘要与正文。
result: 结果与对比结论请参考摘要与正文。
conclusion: 总体而言，该工作在所述任务上展示了有效性，并提供了可复用的思路或工具。
---

## 摘要
科学模型作为科学理论与经验数据之间的接口，在自然科学中得到了广泛应用[1]。例如，这些模型在人类与动物学习研究中扮演着关键角色，它们表达算法假设并将其与心理学和神经科学数据联系起来[2, 3]。传统上，这些模型由专家研究者根据现有理论或新见解手工构建。然而，现在已知这类手工模型即使在狭窄领域内也难以捕捉行为的全部丰富性[4-7]。一种替代的数据驱动方法应运而生，旨在通过拟合和解释灵活的模型来发现新见解[8-11]。但是，这些工具需要大量的人力才能从数据中获取见解，而且如何高效地从数据中发现新思路一直不清楚。在此，我们提出DataDIVER，一种从数据中自动发现计算模型的通用方法，并证明这些模型能浮现出关于人类与动物学习的新颖机制性见解。我们的方法提供的模型采用简短计算机程序的形式，这些程序经过优化以既良好拟合数据又保持简洁。这些程序与现有理论框架明确联系，且易于被人类科学家理解。它们还可用于做出新颖预测，其中一些预测在对现有数据的重新分析中得到了验证。从数据中浮现新想法的通用工具，尤其是与众多领域日益丰富的大数据集相结合，有望极大地加速科学发现。

## Abstract
Scientific models are widely used across the natural sciences as an interface between scientific theories and empirical data [1]. Such models play a key role, for example, in the study of human and animal learning, where they express algorithmic hypotheses and relate them to psychology and neuroscience data [2, 3]. These models are traditionally handcrafted by expert researchers based on existing theory or new insights. Such handcrafted models, however, are now known to fall short of capturing the full richness of behavior, even in their narrow domains [4-7]. An alternative data-driven approach has emerged, seeking to discover new insights by fitting and interpreting flexible models [8-11]. However, these tools require substantial human effort to derive insight from data, and it has been unclear how to discover new ideas from data efficiently. Here, we present DataDIVER, a general approach for automatically discovering computational models from data, and demonstrate that these models surface novel mechanistic insights into human and animal learning. Our approach delivers models that take the form of short computer programs, which are optimized both to fit data well and to be simple. These programs explicitly connect with existing theoretical frameworks and are readily understandable by human scientists. They can also be used to make novel predictions, some of which we show are borne out in re-analysis of existing data. General-purpose tools for surfacing new ideas from data, especially in combination with the large datasets that are increasingly available in many fields, stand to dramatically accelerate scientific discovery.