---
title: "BioRAG-DRAG: A Multimodal Biological Retrieval Layer for Local-First Biomedical Agents"
title_zh: BioRAG-DRAG：面向本地优先生物医学代理的多模态生物检索层
authors: "Wang, L."
date: 2026-05-21
pdf: "https://www.biorxiv.org/content/10.64898/2026.05.19.726174v1.full.pdf"
tags: ["query:autoresearch"]
score: 7.0
evidence: 面向生物医学代理的多模态检索层，结合神经检索、BLAST和基于图的证据封装
tldr: BioRAG-DRAG提出本地优先多模态检索层，集成可插拔神经序列-文本检索、BLAST重排和DRAG图式证据，通过专用蛋白编码器与统一生物语言骨干处理混合查询。在258k条记录的BioRAG-Standard v0压力测试中，BLAST生物匹配近乎饱和，通用蛋白编码器胜出专有OmniGene蛋白嵌入，但DNA稠密检索仍弱。结果确认向量检索提供统一上下文，BLAST和DRAG赋予生物验证与归因，该架构为可信生物代理提供高效透明检索基础。
source: biorxiv
selection_source: fresh_fetch
motivation: 生物医学代理缺乏统一访问异质证据的接口，传统工具如BLAST无法提供上下文，限制了大模型代理的应用。
method: 构建本地优先的BioRAG-DRAG检索层，集成神经序列-文本检索、BLAST重排和DRAG图证据，采用ESM-2等编码器。
result: 在BioRAG-Standard v0的25.8万记录上测试，BLAST匹配近乎饱和，蛋白编码器优于OmniGene嵌入，DNA检索仍弱，索引开销小。
conclusion: 架构分工：向量检索提供候选上下文，BLAST与图验证归因，支持可追溯的生物代理，有助可信本地化部署。
---

## 摘要
生物医学代理需要可靠地访问异质证据：文献文本、基因与通路记录、蛋白质序列、DNA/cDNA序列以及结构化生物关系。经典的序列工具如BLAST仍是基于比对验证的正确选择，但它们并非面向大型语言模型代理的统一上下文接口。我们提出了BioRAG-DRAG，一个本地优先的多模态检索层，它结合了可插拔的神经序列-文本检索、BLAST验证以及基于图的证据打包。专用编码器如ESM-2可服务于蛋白质分区，而OmniGene CPT为混合序列/文本和面向代理的使用提供了统一的生物语言主干；BLAST对序列候选进行重排序或验证；DRAG图为下游代理暴露类型化、可追溯的路径。

我们引入了BioRAG-Standard v0，一个包含257,886条可检索记录的分区语料库/库，以及基于Open-Rosalind标准生物医学记录和序列窗口扩展构建的用于工程评估的初始注释层。在索引内序列窗口压力测试中，BLAST几乎达到生物学匹配饱和，而向量检索恢复了大量但较低的生物学匹配率。在保留的父片段对照中，公共蛋白质编码器优于当前的OmniGene蛋白质窗口嵌入，而即便使用现成的Nucleotide Transformer池化，DNA/cDNA密集检索仍然薄弱；这支持了模型无关的BioRAG设计，而非某一统一生成器主干是最佳序列搜索编码器的声明。在标准文本和10万个序列窗口集合上的索引化Chroma查询，仅在查询嵌入后增加少量查找开销；这并未测量端到端即时延迟。最后，探索性的序列DRAG追踪显示了可检查的生物邻域，包括免疫球蛋白家族和基因符号模块，初步的图对照表明其结构非随机但部分由序列相似性驱动。这些结果支持了一种有界架构：向量检索提供统一的候选上下文，而BLAST和DRAG提供生物学验证和证据归因。

## Abstract
Biomedical agents need reliable access to heterogeneous evidence: literature text, gene and pathway records, protein sequences, DNA/cDNA sequences, and structured biological relations. Classical sequence tools such as BLAST remain the right choice for alignment-grounded verification, but they are not a unified context interface for large language model agents. We present BioRAG-DRAG, a local-first multimodal retrieval layer that combines pluggable neural sequence-text retrieval, BLAST verification, and graph-based evidence packaging. Specialized encoders such as ESM-2 can serve protein partitions, while OmniGene CPT provides a unified biological-language backbone for mixed sequence/text and agent-facing use; BLAST reranks or verifies sequence candidates; and DRAG graphs expose typed, traceable paths for downstream agents.

We introduce BioRAG-Standard v0, a partitioned corpus/library with 257,886 retrievable records and an initial annotation layer for engineering evaluation built from Open-Rosalind Standard biomedical records and sequence-window extensions. On an in-index sequence-window stress test, BLAST nearly saturates biological matching, while vector retrieval recovers substantial but lower biological match rates. On held-out parent-fragment controls, public protein encoders outperform the current OmniGene protein-window embedding, while DNA/cDNA dense retrieval remains weak even with off-the-shelf Nucleotide Transformer pooling; this supports a model-agnostic BioRAG design rather than a claim that one unified generator backbone is the best sequence-search encoder. Indexed Chroma lookup over Standard text and 100k sequence-window collections adds only small lookup overhead after query embedding; this does not measure end-to-end instant latency. Finally, exploratory sequence DRAG traces show inspectable biological neighborhoods, including immunoglobulin-family and gene-symbol modules, with initial graph controls indicating non-random but partly sequence-similarity-driven structure. These results support a bounded architecture: vector retrieval supplies unified candidate context, while BLAST and DRAG provide biological verification and evidence attribution.