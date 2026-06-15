---
title: "APOSM: Pairwise preference learning improves generative small-molecule design"
title_zh: APOSM：成对偏好学习改进生成式小分子设计
authors: "Dreisler, M. W., Michael, R., Hatzakis, N. S., Boomsma, W."
date: 2026-06-10
pdf: "https://www.biorxiv.org/content/10.64898/2026.06.06.730554v1.full.pdf"
tags: ["query:autoresearch"]
score: 7.0
evidence: 成对偏好学习用于生成式分子设计，自动筛选候选化合物，推动AI for Science
tldr: 小分子先导优化受限于合成与测试成本，基于稀疏噪声数据的替代模型可靠性不足。本文提出利用候选分子的成对比较训练替代模型，并开发主动学习算法APOSM，结合片段生成器、成对图神经网络与概率排序。在Practical Molecular Optimization等任务上，APOSM较无引导优化、Graph-GA及逐点回归显著提升目标达成与采样效率，尤其当绝对分数难以校准时优势明显，为小分子智能设计提供可靠方案。
source: biorxiv
selection_source: fresh_fetch
motivation: 稀疏噪声的筛选数据导致绝对分数替代模型不可靠，需要更鲁棒的优先筛选策略。
method: 提出APOSM算法，基于成对偏好学习训练图神经网络替代模型，结合片段生成器与概率排序进行主动学习批量获取。
result: 在PMO基准和GPCR任务上，APOSM在目标达成和采样效率上超越无引导优化、Graph-GA和逐点回归，绝对分数难校准任务上增益最大。
conclusion: 成对偏好学习能有效处理稀疏噪声数据，提升小分子优化替代模型可靠性，APOSM为生成式分子设计提供了高效主动学习新范式。
---

## 摘要
小分子先导化合物优化受限于合成和测定候选物的成本，这使得优先选择化合物进行实验测试的替代模型成为设计过程的核心。此类替代模型的可靠性受到筛选测量的噪声和稀疏性的限制。我们表明，在这种情形下，基于候选分子之间的成对比较训练替代模型，而非基于绝对预测分数，能够为活性候选物选择提供显著更可靠的信号。我们开发了APOSM，这是一种主动学习算法，在批量采集循环中结合了基于片段的生成器、成对消息传递图神经网络替代模型以及概率排序。在实用分子优化基准测试和GPCR配体再发现任务中，APOSM 在目标达成度和采样效率上均优于无引导的基于片段的优化、Graph-GA 遗传算法和逐点回归消融模型，其中在绝对分数最难校准的任务上提升最大。

## Abstract
Small-molecule lead refinement is constrained by the cost of synthesizing and assaying candidates, making the surrogate models that prioritize compounds for experimental testing central to the design process. The reliability of such surrogates is limited by the noise and sparsity of screening measurements. We show that training the surrogate on pairwise comparisons between candidate molecules, rather than on absolute predicted scores, yields a substantially more reliable signal for active candidate selection in this regime. We develop APOSM, an active-learning algorithm that combines a fragment-based generator, a pairwise message-passing graph neural network surrogate, and probabilistic ranking inside a batched acquisition loop. On the Practical Molecular Optimization benchmark and a GPCR ligand rediscovery task, APOSM improves target attainment and sampling efficiency over unguided fragment-based optimization, the Graph-GA genetic algorithm, and a pointwise-regression ablation, with the largest gains on tasks where absolute scores are hardest to calibrate.