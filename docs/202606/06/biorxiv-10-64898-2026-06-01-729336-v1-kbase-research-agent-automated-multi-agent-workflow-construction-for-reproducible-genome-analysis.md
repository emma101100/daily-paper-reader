---
title: "KBase Research Agent: Automated Multi-Agent Workflow Construction for Reproducible Genome Analysis"
title_zh: KBase研究智能体：面向可重复基因组分析的自动化多智能体工作流构建
authors: "Gupta, P., Riehl, W. J., Cashman, M., Chivian, D., Neely, C. J., Canon, S. R., Cottingham, R., Henry, C., Arkin, A. P., Dehal, P. S."
date: 2026-06-04
pdf: "https://www.biorxiv.org/content/10.64898/2026.06.01.729336v1.full.pdf"
tags: ["query:autoresearch"]
score: 9.0
evidence: 用于科学工作流构建的自主多代理系统
tldr: 多步骤生物信息学工作流构建（例如读段质控到基因组组装及注释）需深厚专业知识，严重制约可重复分析。KBase研究代理采用多智能体系统与知识图谱，在DOE系统生物学知识库中自动化设计、执行分析流程。在参考工作流和100个未分析细菌基因组上，它准确完成质控、组装、分类与注释，生成可重复Narrative和手稿初稿。这证明了基于领域知识的端到端科学工作流自动化可行性，推动可重复研究发展。
source: biorxiv
selection_source: fresh_fetch
motivation: 多步骤基因组分析流程构建依赖综合专业知识，严重阻碍大规模可重复研究。
method: 提出KBase研究代理，基于多智能体与知识图谱，在DOE知识库中实现自动化工作流构建与执行。
result: 在参考工作流和100个菌株上，自主完成质控、组装、分类与注释，产出可重复Narrative和论文草稿。
conclusion: 证明了在生物信息学平台中实现领域知识驱动的端到端科学工作流自动化可行，促进可重复分析。
---

## 摘要
构建从读段质量控制到基因组组装再到功能注释的多步骤生物信息学工作流，需要生物学和计算工具选择方面的专业知识，为可扩展和可重复的分析带来了瓶颈。我们提出了KBase研究智能体，这是一个多智能体系统，可在美国能源部系统生物学知识库（KBase）内自动化此类工作流。给定一组测序读段和一个研究目标，该智能体基于KBase文档和KBase应用程序目录的知识图谱（KG）制定分析计划，然后选择、参数化、验证并执行适当的KBase应用程序来执行工作流。最终的分析结果被保存为可重复的KBase Narrative。我们根据来自同行评审的《微生物学资源公告》的参考工作流构建的地面真值，评估了系统的规划和执行质量。我们进一步将该智能体应用于来自JGI IMG/M数据库的100个先前未分析的细菌分离株基因组，它自主执行了读段质量控制、基因组组装、使用GTDB-Tk进行分类学分类以及下游分析，生成了注释基因组、可重复的Narratives和草稿手稿，无需人工干预。在这些实验中，KBase研究智能体证明了在产出的生物信息学平台中，以领域为基础、端到端的科学工作流自动化是可行的。

## Abstract
Constructing multi-step bioinformatics workflows, from read quality control through genome assembly to functional annotation, requires expertise in both biology and computational tool selection, creating a bottleneck for scalable and reproducible analysis. We present the KBase Research Agent, a multi-agent system for automating such workflows within the DOE Systems Biology Knowledgebase (KBase). Given a set of sequencing reads and a research objective, the agent constructs an analysis plan grounded in KBase documentation and a Knowledge Graph (KG) of the KBase application catalog, then selects, parameterizes, validates and executes appropriate KBase applications to carry out the workflow. The resulting analysis is preserved as a reproducible KBase Narrative. We evaluate the system's planning and execution quality against ground truth constructed from reference workflows derived from peer-reviewed Microbiology Resource Announcements. We further apply the agent to 100 previously unanalyzed bacterial isolate genomes from the JGI IMG/M database, where it autonomously performed read quality control, genome assembly, taxonomic classification with GTDB-Tk, and downstream analysis producing annotated genomes, reproducible Narratives, and draft manuscripts without human intervention. Across these experiments, the KBase Research Agent demonstrates the feasibility of domain-grounded, end-to-end scientific workflow automation in a production bioinformatics platform.

---

## 论文详细总结（自动生成）

## 1. 研究动机与核心问题
- **背景**：从原始测序读段到基因组组装、分类与功能注释的多步骤生物信息学工作流构建，高度依赖生物学洞见与计算工具的双重专业知识，成为大规模、可重复基因组分析的关键瓶颈。
- **核心问题**：能否将上述端到端流程自动化，使非专家用户也能可靠地执行可重复分析，从而突破专业知识壁垒、提升研究效率与可复制性。
- **整体含义**：该研究试图证明，在成熟的知识库平台内，通过领域知识驱动的自主智能体系统，可以实现真正“无人值守”的科学工作流构建与执行，并直接产出可发表的成果初稿。

## 2. 方法论
- **核心思想**：基于多智能体架构，耦合KBase平台的知识图谱（KG），将研究目标与具体工具链自动对齐。
- **关键技术细节**：
  - **知识图谱构建**：利用KBase的官方文档与应用目录，构建一个描述工具、参数、数据类型及相互依赖关系的知识图谱，作为智能体制定计划的依据。
  - **多智能体协作**：系统包含若干功能智能体，协同完成“计划制定—应用选择—参数配置—执行验证”的闭环。
  - **工作流生成流程**：
    1. 输入测序读段与高层研究目标。
    2. 规划智能体查询知识图谱，生成细化的分析步骤计划。
    3. 执行智能体根据计划从KBase应用目录中选取适配的应用（如Trimmomatic、SPAdes、GTDB-Tk等），并按最佳实践自动设定参数。
    4. 验证智能体检查中间输出格式与兼容性，确保流程顺利衔接。
    5. 全部计算完成后，结果自动封装为可交互、可重放的KBase Narrative，并可进一步生成论文草稿。
- **算法/公式**：文章未披露具体算法公式或规划优化函数，侧重于系统工程设计与领域知识集成。

## 3. 实验设计
- **评估数据集/场景**：
  - **地面真值评估集**：依据同行评审《微生物学资源公告》中已发表的标准基因组分析工作流，手工构建参考工作流作为“金标准”，用于评价智能体的计划与执行是否准确。
  - **大规模盲测集**：从JGI IMG/M数据库选取100个先前未被分析的细菌分离株基因组（仅有原始测序读段），完全交由系统自主完成全流程分析。
- **Benchmark与对比方法**：
  - 主要基准为人工专家构建的参考工作流，对比系统生成的工作流在步骤选择、工具选取和参数设置上的一致性（即“规划质量”与“执行质量”）。
  - 文摘未提及其他自动化工作流工具（如Galaxy、Snakemake、Nextflow平台上的自动化方案）的横向对比。

## 4. 资源与算力
- 全文摘要及元数据中**未明确说明**实验所使用的算力资源，例如未提及GPU型号、数量、CPU核心数，也未给出单次分析耗时或训练时长。因此无法对算力消耗做定量总结。

## 5. 实验数量与充分性
- **整体实验组数**：至少包含两类主要实验——①基于参考工作流的地面真值对比评估；②100个未分析菌株的端到端自动化分析。
- **实验充分性与客观性**：
  - *优势*：在真实平台（DOE KBase）上，用100个独立样本验证了系统的可扩展性与自动化程度，产出成果包括组装基因组、注释Narrative和手稿初稿，证明了工程实用性。
  - *局限*：未设计消融研究（如去掉知识图谱、去掉多智能体协同会如何），也缺少与其它自动化范式（如大语言模型直接生成脚本、传统流程引擎的自动参数推荐）的定量对比，客观评判维度相对单一。地面真值来自同一领域的公告，可能偏向已知标准流程，泛化性尚需更广泛评估。

## 6. 主要结论与发现
- KBase研究智能体能够自主完成读段质控、基因组组装、GTDB-Tk分类学注、功能注释等一系列复杂步骤。
- 在参考工作流测试中，系统的规划和执行与专家手册流程高度一致。
- 对100个全新菌株，系统无需人工干预即产出可重复的Narrative和草稿手稿，显著缩短从原始数据到可报告结果的时间。
- **核心发现**：在生产级生物信息学平台内，基于领域知识图谱的端到端科学工作流自动化是完全可行的，能够实质性地推动可重复研究的发展。

## 7. 优点
- **领域深度结合**：不是通用流程自动化，而是专门针对KBase平台及其应用目录构建知识图谱，确保工具推荐和参数配置符合领域最佳实践。
- **产物完整度**：直接生成可重复执行的Narrative和论文初稿，将自动化延伸到成果传播环节。
- **规模化验证**：用100个真实未分析菌株进行实战检验，比仅用少数案例更有说服力。
- **降低门槛**：极大减少了对用户生物信息学技能的依赖，有利于提高微生物基因组分析的通量。

## 8. 不足与局限
- **平台锁定的泛化风险**：系统深度依赖KBase生态，若迁移至其他平台需重新构建知识图谱与功能衔接，方法本身的可移植性待验证。
- **对比基线薄弱**：未与其他自动化工作流构建工具或大语言模型辅助方案进行定量比较，难以定位该多智能体方法的相对优势。
- **实验覆盖不全**：缺少消融实验，无法解析知识图谱、多智能体架构、参数策略等组件各自的贡献；错误案例（如组装失败、分类错误）的分析缺失。
- **论文草稿质量未评估**：生成的“草稿手稿”未说明是否经过人工评审、是否达到投稿标准，其成熟度存疑。
- **算力细节缺失**：未分析计算开销、时间成本，难以评估其在大规模项目中的经济可行性。

（完）
