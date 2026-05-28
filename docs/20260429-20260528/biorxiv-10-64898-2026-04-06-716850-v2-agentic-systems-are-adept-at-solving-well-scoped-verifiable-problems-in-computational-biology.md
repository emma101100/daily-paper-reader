---
title: "Agentic systems are adept at solving well-scoped, verifiable problems in computational biology"
title_zh: 智能体系统擅长解决计算生物学中范围明确、可验证的问题
authors: "Nair, S., Gunsalus, L., Orcutt-Jahns, B., Rossen, J., Lal, A., Donno, C. D., Celik, M. H., Fletez-Brant, K., Xie, X., Bravo, H. C., Eraslan, G."
date: 2026-05-03
pdf: "https://www.biorxiv.org/content/10.64898/2026.04.06.716850v2.full.pdf"
tags: ["query:autoresearch"]
score: 8.0
evidence: 用于评估计算生物学中智能体系统的基准
tldr: "计算生物学任务因数据噪声大、主观性强而难以客观评估。为此，我们提出CompBioBench，包含100个多样化任务，通过合成数据和元数据扰乱构造具有唯一正确答案的问题，涵盖基因组学、转录组学等六大领域。评估表明，Codex CLI (GPT 5.4)达到83%准确率，Claude Code (Opus 4.6)在难题上达69%。该基准为智能体系统在计算生物学中的进展提供了实用测试平台，并指导未来基准设计。"
source: biorxiv
selection_source: fresh_fetch
motivation: 计算生物学任务缺乏客观可验证的评估基准，现有方法多依赖预设检查清单，无法反映真实问题解决能力。
method: 基于合成/增强数据及元数据扰乱构造真实数据集，生成100个需多步推理、工具使用和代码编写的可验证问题，涵盖六个领域。
result: "Codex CLI (GPT 5.4) 准确率83%，Gemini CLI (3.1 Pro) 82%，Claude Code (Opus 4.6) 81%；最难题上Claude Code达69%，Codex CLI 59%。"
conclusion: CompBioBench为计算生物学智能体系统提供了实用测试平台，揭示通用模型强劲性能，并推动未来基准设计。
---

## 摘要
我们介绍了CompBioBench，这是一个包含100个不同任务的基准测试，用于评估计算生物学中的智能体系统。与数学和编程不同，它们更容易进行系统验证，而生物数据本质上是嘈杂的，并且解释空间很大。为了在不将任务简化为规定性检查表的情况下实现客观评估，我们提出了一种新的基准构建策略，基于合成/增强数据以及对真实数据集的元数据打乱/清洗，创建具有单一真实答案且需要多步推理、工具使用、定制代码以及与真实世界外部资源交互的具有挑战性的问题。该基准涵盖了基因组学、转录组学、表观基因组学、单细胞分析、人类遗传学和机器学习工作流。问题由领域专家策划，涵盖各种技能和不同难度。我们从最简约的环境开始评估领先的通用智能体系统，要求它们根据需要获取数据和工具来解决每个问题。我们发现强大的端到端性能，Codex CLI (GPT 5.4)达到83%的准确率，Gemini CLI (3.1 Pro)达到82%，Claude Code (Opus 4.6)达到81%，Claude Code (Opus 4.7)达到78%。在最难的问题上，Claude Code (Opus 4.6)达到69%，Codex CLI (GPT 5.4)达到59%，Gemini CLI (3.1 Pro)达到49%。CompBioBench为衡量智能体系统在计算生物学中的进展以及指导未来基准设计提供了一个实用的测试平台。数据和公开排行榜可在 https://huggingface.co/collections/Genentech/compbiobench-v1 获取。

## Abstract
We introduce CompBioBench, a benchmark of 100 diverse tasks for evaluating agentic systems in computational biology. Unlike mathematics and programming, which more readily admit systematic verification, biological data are inherently noisy and open to interpretation. To enable objective evaluation without reducing tasks to prescriptive checklists, we propose a new benchmark construction strategy based on synthetic/augmented data and metadata scrambling/scrubbing of real datasets to create challenging problems that have a single ground-truth answer and require multi-step reasoning, tool use, bespoke code, and interaction with real-world external resources. The benchmark spans genomics, transcriptomics, epigenomics, single-cell analysis, human genetics, and machine learning workflows. Questions are curated by domain experts to cover a broad range of skills with varying difficulty. We evaluate leading general-purpose agentic systems starting from a bare-minimum environment, requiring them to fetch data and tools as needed to solve each problem. We find strong end-to-end performance, with Codex CLI (GPT 5.4) reaching 83% accuracy, Gemini CLI (3.1 Pro) reaching 82%, Claude Code (Opus 4.6) reaching 81%, and Claude Code (Opus 4.7) reaching 78%. On the hardest questions, Claude Code (Opus 4.6) reaches 69%, Codex CLI (GPT 5.4) reaches 59%, and Gemini CLI (3.1 Pro) reaches 49%. CompBioBench provides a practical testbed for measuring the progress of agentic systems in computational biology and for guiding future benchmark design. Data and a public leaderboard are available at https://huggingface.co/collections/Genentech/compbiobench-v1.