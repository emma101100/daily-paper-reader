---
title: "ClaroAI-Bench: Evaluating Agentic Scientific Reproducibility on Real Biomedical Papers"
title_zh: ClaroAI-Bench：评估真实生物医学论文上的智能体科学可复现性
authors: "O'Connell, K. A."
date: 2026-05-12
pdf: "https://www.biorxiv.org/content/10.64898/2026.05.08.723611v1.full.pdf"
tags: ["query:autoresearch"]
score: 9.0
evidence: 评估代理科研可重现性的基准
tldr: "现有AI评估基准缺乏对真实科学复现全流程的测试。ClaroAI-Bench包含35篇NIH资助的真实生物医学论文，从数据可查找性、可访问性、代码可用性、环境可重建性和结果可复现性五维度评分。全能力AI代理成功复现60.6%的论文，而基线为零。数据代码可访问性显著影响复现率，环境重建是评估者分歧最大的维度。该基准填补了代码生成与端到端科学AI评估之间的空白。"
source: biorxiv
selection_source: fresh_fetch
motivation: 现有基准未能测试AI代理在真实科研复现中的完整能力，尤其缺乏对数据、代码、环境等真实约束的评估。
method: 构建包含35篇NIH论文的五维评分基准，并设计审计基线、bash-only代理和全能力代理三种条件进行消融实验。
result: "全能力代理复现20/33论文（60.6%），D1-D4评分与D5高度相关（r=0.68），数据代码可访问的论文复现率高出2.9倍。"
conclusion: ClaroAI-Bench为评估AI代理的科研复现能力提供了标准化基准，揭示了当前AI在真实场景中的局限。
---

## 摘要
我们介绍了ClaroAI-Bench，一个用于衡量AI智能体复现已发表生物医学研究计算结果能力的评估套件。该基准包含35篇真实的美国国立卫生研究院（NIH）资助论文，涵盖五种模态（基因组学、影像学、临床/电子健康记录、流行病学、湿实验），并按五个维度评分：数据可发现性（D1）、数据可访问性（D2）、代码可用性（D3）、环境可重建性（D4）和结果可复现性（D5）。每个任务要求智能体定位数据、获取代码、重建计算环境、执行分析并验证结果与已发表声明的一致性——模拟完整的科学复现流程。在三条件消融实验中，仅审计基线（D1-D4元数据评分）和仅bash智能体（API + bash工具）均达到0%的D5复现率，而全功能智能体（Claude Code，所有工具）复现了33篇计算论文中的20篇（60.6%；95% CI [42.4, 75.8]）。D1-D4元数据评分强烈预测D5结果（Spearman r=0.68，p<0.0001），且数据与代码可访问的论文的D5得分比受限论文高2.9倍（p=0.0013）。使用三个前沿模型（Claude Opus 4.6、GPT-5.4、Gemini 2.5 Pro）的多模型评分在D3上产生r=0.85-0.97的模型间一致性，但在D4上仅为r=0.51-0.81，将环境重建确定为评估者分歧最大的维度。ClaroAI-Bench通过测试具有脆弱环境、缺失元数据和访问限制的长期真实世界复现任务，填补了代码生成基准（SWE-bench）与端到端科学AI评估之间的空白。该基准、评分规则、智能体日志和可通过pip安装的审计器存档于https://doi.org/10.5281/zenodo.20071236和HuggingFace Datasets上的https://huggingface.co/datasets/kyleaoconnell22/claroai-bench。

## Abstract
We introduce ClaroAI-Bench, an evaluation suite for measuring AI agents ability to reproduce computational findings from published biomedical research. The benchmark comprises 35 real NIH-funded papers spanning five modalities (genomics, imaging, clinical/EHR, epidemiology, wet-lab) scored on a five-dimension rubric: data findability (D1), data accessibility (D2), code availability (D3), environment reconstructability (D4), and results reproducibility (D5). Each task requires an agent to locate data, obtain code, reconstruct the compute environment, execute the analysis, and verify results against published claims--mirroring the full scientific reproduction pipeline. In a three-condition ablation, an audit-only baseline (D1-D4 metadata scoring) and a bash-only agent (API + bash tool) both achieve 0% D5 reproduction, while a full-capability agent (Claude Code, all tools) reproduces 20 of 33 computational papers (60.6%; 95% CI [42.4, 75.8]). D1-D4 metadata scores strongly predict D5 outcomes (Spearman r=0.68, p<0.0001), and papers with accessible data and code achieve 2.9x higher D5 scores than restricted papers (p=0.0013). Multi-model scoring with three frontier models (Claude Opus 4.6, GPT-5.4, Gemini 2.5 Pro) yields inter-model agreement of r=0.85-0.97 on D3 but only r=0.51-0.81 on D4, identifying environment reconstruction as the dimension with highest evaluator disagreement. ClaroAI-Bench fills a gap between code-generation benchmarks (SWE-bench) and end-to-end scientific AI evaluations by testing long-horizon, real-world reproduction tasks with brittle environments, missing meta-data, and access constraints. The benchmark, scoring rubric, agent logs, and pip-installable auditor are archived at https://doi.org/10.5281/zenodo.20071236 and on HuggingFace Datasets at https://huggingface.co/datasets/kyleaoconnell22/claroai-bench.