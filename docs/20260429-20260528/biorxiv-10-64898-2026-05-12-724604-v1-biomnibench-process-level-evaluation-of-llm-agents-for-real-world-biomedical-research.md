---
title: "BiomniBench: Process-level Evaluation of LLM Agents for Real-world Biomedical Research"
title_zh: "BiomniBench: 用于真实世界生物医学研究的LLM智能体过程级评估"
authors: "Qu, Y., Lu, Y., Tu, X., Zhang, S., She, T., Shaw, A. G., Shih, J.-H., Zhao, B., Shen, M., Yang, H., Yan, J., Zhang, R., Wu, X., Li, T., Cong, L., Hu, X., Jiang, Y., Dong, J., Peng, T., Leskovec, J., Huang, K."
date: 2026-05-14
pdf: "https://www.biorxiv.org/content/10.64898/2026.05.12.724604v1.full.pdf"
tags: ["query:autoresearch"]
score: 9.0
evidence: 针对生物医学研究智能体的过程级基准，解决评估局限性
tldr: 现有LLM代理评估仅依赖最终结果，易受记忆或偶然正确性误导，也误判合理替代分析。为此提出BiomniBench，首个生物医学研究过程级基准，基于专家设计的评分标准对代理完整轨迹进行维度诊断。BiomniBench-DA包含100个源自Nature/Cell/Science论文的数据分析任务。测试发现前沿与开源模型得分相近且提升空间大，代理工具影响超过模型换代，代理在方法选择和科学推理上持续短板。该基准提供了结果评分无法揭示的细粒度诊断能力。
source: biorxiv
selection_source: fresh_fetch
motivation: 仅基于结果的基准无法区分真实推理与偶然正确，且误判合理替代分析，需过程级评估。
method: 构建BiomniBench-DA，包含100个源自顶刊的数据分析任务，由专家设计评分标准对代理完整轨迹逐维度评分。
result: 前沿与开源基础模型得分相近，代理工具影响大于模型换代，代理在方法选择与科学推理上持续不足。
conclusion: BiomniBench是首个生物医学研究LLM代理过程级基准，提供结果评分无法实现的诊断，指明模型关键短板。
---

## 摘要
LLM智能体现已能够执行真实的生物医学研究，但对其进行严格评估相当困难。仅关注结果的基准测试存在两个问题。首先，正确的最终答案可能源于记忆、奖励破解或偶然产生正确数字的错误推理。其次，有效的替代分析仅仅因为与参考答案不同而被判定为错误。我们提出了BiomniBench，一个过程级评估框架，根据专家设计的、针对具体任务的评分标准对整个智能体轨迹进行评分。我们的首次发布BiomniBench-DA包含100个数据分析任务，涵盖17种任务类型、5个疾病领域以及一个普通生物学类别，每个任务基于来自《自然》、《细胞》、《科学》等期刊的一篇论文，并与原始作者或领域专家共同开发。对前沿模型和开放权重模型在四个智能体框架上的基准测试揭示了三个发现：前沿模型和开放权重模型之间的得分差距很小，所有模型都有显著的提升空间；智能体框架对得分的影响超过连续模型代际之间的差距；智能体能够可靠地将结论与真实来源联系起来，但在方法选择、生物学解释和科学推理方面始终存在不足。BiomniBench是生物医学研究中LLM智能体的首个过程级基准，提供了结果评分无法实现的维度级诊断。数据集：huggingface.co/datasets/phylobio/BiomniBench-DA

## Abstract
LLM agents now perform real biomedical research, but evaluating them rigorously is hard. Outcome-only benchmarks fail in two ways. First, a correct final answer can come from memorization, reward hacking, or wrong reasoning that produces the right number by chance. Second, valid alternative analyses are marked wrong simply because they differ from the reference. We introduce BiomniBench, a process-level evaluation framework that scores the full agent trajectory against expert-designed, task-specific rubrics. Our first release, BiomniBench-DA, contains 100 data-analysis tasks across 17 task types, 5 disease areas, and a general-biology category, each based on a paper from journals such as Nature, Cell, and Science and co-developed with an original author or a domain expert. Benchmarking frontier and open-weight models across four agent harnesses reveals three findings. Frontier and open-weight bases cluster within a few points of each other, with substantial headroom for all models. The agent harness shifts scores by more than the gap between successive model generations. Agents reliably ground claims in real sources yet consistently fall short on method selection, biological interpretation, and scientific reasoning. BiomniBench is the first process-level benchmark for LLM agents in biomedical research, providing the dimension-level diagnostics that outcome scoring cannot.

Datasethuggingface.co/datasets/phylobio/BiomniBench-DA