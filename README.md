# CDE-Mapping-Tool

## Overview

**CDEMapper** is an Elasticsearch and Large Language Model (LLM)-powered mapping tool designed for biomedical and clinical researchers to efficiently map study variables to the **NIH Common Data Elements (CDEs)**. It integrates essential and advanced services into a user-centered mapping workflow, allowing users to choose different mapping strategies based on their project's needs.  

### Key Features:
- **Top-10 CDE Recommendations**: Provides the top 10 recommended NIH CDEs for each user-provided variable.
- **Customizable Search**: Supports further searches beyond the top 10 recommendations.
- **Comprehensive CDE Indexing**: Indexed **23,328 CDEs** from **19 NIH CDE Collections** (as of October 21, 2024).
- **LLM Integration**: CDEMapper v1.1.0 utilizes **GPT-4o** for enhanced mapping accuracy.

---

## Evaluation Datasets

To assess the tool’s mapping capabilities, we collected data dictionaries from four domains:

| **Domain**  | **Source**  |
|------------|------------|
| **Eye** | American Academy of Ophthalmology IRIS ® Registry (Intelligent Research in Sight) Analytics Data Dictionary |
| **Stroke** | Human Circadian/Diurnal Biology and Stroke Common Data Elements |
| **ADRD** | National Alzheimer’s Coordinating Center - Uniform Data Set (UDS) |
| **COVID-19** | COVID-19 Therapeutic Trial Common Data Elements |

These datasets include **494 data elements**, which have been manually mapped to NIH CDE collections for **coverage assessment and tool performance evaluation**.

---

## Mapping Settings

We defined three mapping settings based on manual annotation:

1. **1 vs 1**: One source element maps to a unique target element.
2. **M vs 1**: Multiple source elements map to a single target element.
3. **1 vs M**: One source element maps to multiple target elements.

If a target CDE was not found, no mapping was created for that entry. **Two annotators** manually established the gold standards, resolving discrepancies through discussion. Ultimately, **264 entries** with effective mappings were finalized for evaluation.

---

## Evaluation Codes

The evaluation scripts assess **retrieval and ranking performance** across different datasets and mapping settings.

### 🔍 Retrieval Evaluation:
| Script | Description |
|--------|------------|
| [`evaluations_retrieval.ipynb`](./EvaluationCode/evaluations_retrieval.ipynb) | Evaluates overall retrieval performance (**Search All, Embedding Search, Query Expansion**) for **ADRD, Eye, Stroke** datasets. |
| [`evaluations_retrieval-specific.ipynb`](./evaluations_retrieval-specific.ipynb) | Evaluates **1 vs 1, M vs 1, 1 vs M** retrieval performance for **ADRD, Eye, Stroke** datasets. |
| [`evaluations_retrieval-covid.ipynb`](./evaluations_retrieval-covid.ipynb) | Evaluates overall retrieval performance (**Search All, Embedding Search, Query Expansion**) for **COVID-19** dataset. |
| [`evaluations_retrieval-covid-specific.ipynb`](./evaluations_retrieval-covid-specific.ipynb) | Evaluates **1 vs 1, M vs 1, 1 vs M** retrieval performance for **COVID-19** dataset. |

### 📊 Ranking Evaluation:
| Script | Description |
|--------|------------|
| [`evaluations_rerank.ipynb`](./evaluations_rerank.ipynb) | Evaluates overall **ranking performance** for **ADRD, Eye, Stroke** datasets using the **Re-ranking function**. |
| [`evaluations_rerank_specific.ipynb`](./evaluations_rerank_specific.ipynb) | Evaluates **1 vs 1, M vs 1, 1 vs M** ranking performance for **ADRD, Eye, Stroke** datasets. |
| [`evaluations_rerank-covid.ipynb`](./evaluations_rerank-covid.ipynb) | Evaluates overall **ranking performance** for **COVID-19** dataset using the **Re-ranking function**. |
| [`evaluations_rerank-covid-specific.ipynb`](./evaluations_rerank-covid-specific.ipynb) | Evaluates **1 vs 1, M vs 1, 1 vs M** ranking performance for **COVID-19** dataset. |

---

## 📄 Reference

If you use **CDEMapper**, please cite:

**Wang Y, Huang J, He H, Zhang V, Zhou Y, Hao X, Ram P, Qian L, Xie Q, Weng R, Lin F, Hu Y, Cui L, Jiang X, Xu H, Hong N.**  
*CDEMapper: Enhancing NIH Common Data Element Normalization using Large Language Models.*  
[arXiv:2412.00491](https://arxiv.org/abs/2412.00491)

---

