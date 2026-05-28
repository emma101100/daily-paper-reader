---
title: "Towards autonomous biology: Compiler-Verified Protocols as a Foundation for Real World AI Execution"
title_zh: 迈向自主生物学：编译器验证的协议作为现实世界AI执行的基础
authors: "Song, R., Fu, Y., Zhao, Z., Yu, J., Yuan, Q., Chen, C.-T."
date: 2026-05-07
pdf: "https://www.biorxiv.org/content/10.64898/2026.05.05.720956v1.full.pdf"
tags: ["query:autoresearch"]
score: 9.0
evidence: 提出用于自主生物学的编译器验证协议，实现闭环发现
tldr: "实验协议依赖自然语言描述导致歧义和不可重复。本文提出生物学协议语言BPL及BPL-COGEN管道，结合30B大语言模型与编译器，在生成-验证-修复循环中自动将自然语言SOP转为编译器验证协议。在300篇Nature Protocols上达到95.1% fidelity，湿实验验证跨平台可重复性。该工作为物理世界AI执行奠定基础。"
source: biorxiv
selection_source: fresh_fetch
motivation: 自然语言实验协议缺乏精确性和可验证性，成为AI从计算到物理执行的瓶颈。
method: 提出BPL领域特定语言与BPL-COGEN管道，以编译器反馈驱动LLM迭代修复，生成物理约束满足的协议。
result: "在300篇Nature Protocols上达95.1% fidelity，湿实验验证跨平台可重复执行。"
conclusion: 编译器验证协议是物理世界AI执行的关键前提，推动自主生物学发展。
---

## 摘要
人工智能已从分析实验数据发展到自主生成假设、设计实验和协调闭环发现。然而，从计算推理到物理执行的转化仍然受限于实验协议——在生物学中，实验协议仍依赖于模糊的自然语言描述：这种媒介在其他工程学科数十年前就已放弃，转而采用编译器验证的规范语言。这一缺陷在三个维度上割裂了可重复性：协议准确性、执行前验证和跨平台可移植性。现有的形式化方法仅解决这些挑战的子集，以表达力换取严谨性，以可移植性换取标准化，或以可用性换取溯源。在此，我们引入生物学协议语言（BPL），一种具有生物学原生类型系统的领域特定语言，其中每个量都带有物理单位，每个试剂声明其物理形式，每个容器保持编译器跟踪的状态，从而隐含假设必须明确陈述，物理上不可能的操作在编译时被拒绝。我们进一步开发了BPL-COGEN，一个将微调的300亿参数语言模型与确定性编译器耦合的流程，形成闭环的生成-验证-修复循环，通过编译器诊断迭代地纠正从自然语言SOP到BPL的翻译，直到所有物理、量纲和状态约束得到满足。在300篇已发表的《自然· protocols》论文基准测试中，BPL-COGEN相对于源协议作为真实值达到了95.1的总体保真度分数。在GFP表达文库构建和HPLC到UHPLC方法转换中的湿实验室实验和跨平台验证证实，单个BPL源能够在手动和液体处理器辅助环境下产生可重复的执行。这些结果建立了一种新的流程，生成编译器验证的协议，这是生物学中物理实现AI的必要先决条件。

## Abstract
Artificial intelligence has advanced from analyzing experimental data to autonomously generating hypotheses, designing experiments, and coordinating closed loop discovery. Yet the translation from computational reasoning to physical execution remains bottlenecked by the experimental protocol, which in biology still relies on ambiguous natural-language descriptions: a medium other engineering disciplines abandoned decades ago in favor of compiler verified specification languages. This deficit fragments reproducibility along three axes: protocol accuracy, pre execution verification, and cross platform portability. Existing formalisms address only subsets of these challenges, trading expressiveness for rigor, portability for standardization, or usability for provenance. Here we introduce the Biology Protocol Language (BPL), a domain specific language with a biology-native type system in which every quantity carries physical units, every reagent declares its physical form, and every container maintains compiler-tracked state, so that implicit assumptions must be stated explicitly and physically impossible operations are rejected at compile time. We further develop BPL-COGEN, a pipeline that couples a fine tuned 30 billion parameter language model with the deterministic compiler in a closed generate validate repair loop, iteratively correcting the translation from natural language SOPs to BPL through compiler diagnostics until all physical, dimensional, and state constraints are satisfied. On a benchmark of 300 published Nature Protocols papers, BPL COGEN achieved an overall fidelity score of 95.1 against the source protocols as ground truth. Wet-lab experiment and cross-platform validation in GFP expression library construction and HPLC to UHPLC method translation confirmed that a single BPL source yielded reproducible execution across manual and liquid handler assisted contexts. The results established a novel pipeline that generates compiler-verified protocols, which is an essential prerequisite for physically embodied AI in biology.