---
title: Mechanistic Identifiability Preservation for Hybrid Neural Differential Equations
title_zh: 混合神经常微分方程的机理可辨识性保持
authors: "Whipple, B., Hernandez-Vargas, E. A."
date: 2026-05-23
pdf: "https://www.biorxiv.org/content/10.1101/2024.12.08.627408v2.full.pdf"
tags: ["query:autoresearch"]
score: 6.0
evidence: 为科学建模中使用的混合神经常微分方程提供可识别性的理论保证，支持严格的 AI for Science。
tldr: 混合神经微分方程（HNDE）嵌入神经网络提升建模表达力，但神经增强可能损害机理可辨识性，影响科学可解释性。本文构建保持可辨识性的理论框架，通过有界神经校正类和Gronwall型界限量化神经扰动对参数恢复的影响。实验表明，神经增强系统性削弱但未消除辨识性，存在表达力-辨识性根本权衡。该工作为科学智能计算中HNDE的可信部署提供理论基础与实践指导。
source: biorxiv
selection_source: fresh_fetch
motivation: 神经增强可能引入观测退化，损害HNDE的机理可辨识性和科学可解释性，亟需理论分析与权衡调控。
method: 形式化有界神经校正类，推导轨迹与观测差异的Gronwall型界限，建立保证近似参数恢复的充分条件。
result: 神经增强系统性削弱但未消除机理可辨识性，揭示出模型表达力与参数辨识性之间的根本权衡。
conclusion: 为HNDE在科学智能计算中的部署提供可辨识性保持的理论基础与明确指导，平衡表达力与可解释性。
---

## 摘要
混合神经常微分方程（HNDEs）将神经网络组件嵌入到机理框架中，结合了领域驱动模型的结构可解释性与神经动力学的逼近能力。尽管它们在生物学与工程学中的应用日益增多，但神经增强可能引入观测退化，从而损害机理可辨识性与科学可解释性。

在本文中，我们为HNDEs中机理可辨识性的实用保持构建了一个理论框架。我们形式化了有界神经校正类，并推导出Gronwall型轨迹与观测差异界，将神经扰动与机理参数模糊性联系起来。我们还进一步建立了充分条件，在此条件下，混合神经校正可保持近似的机理参数可恢复性，直至显式可量化的容差。

在基准系统上进行的经验似然剖面分析证实，神经增强系统性地削弱——但不消除——机理可辨识性，揭示了表达力与可辨识性之间的基本权衡。这些结果为在科学智能计算中部署HNDEs提供了理论基础与可操作的指导。

## Abstract
Hybrid neural differential equations (HNDEs) embed neural network components within mechanistic scaffolds, combining the structural interpretability of domain-derived models with the approximation power of neural dynamics. Despite their growing adoption in biology and engineering, neural augmentation can introduce observational degeneracies that compromise mechanistic identifiability and scientific interpretability.

In this paper, we develop a theoretical framework for practical preservation of mechanistic identifiability in HNDEs. We formalize bounded neural correction classes and derive Gronwall-type trajectory and observational discrepancy bounds linking neural perturbations to mechanistic parameter ambiguity. We further establish sufficient conditions under which hybrid neural corrections preserve approximate mechanistic parameter recoverability up to explicitly quantifiable tolerances.

Empirical likelihood profile analyses on benchmark systems confirm that neural augmentation systematically weakens--but does not eliminate--mechanistic identifiability, revealing a fundamental expressiveness-identifiability trade-off. These results provide theoretical foundations and actionable guidance for deploying HNDEs in scientific intelligent computing.