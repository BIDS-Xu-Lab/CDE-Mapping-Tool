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
| [`evaluations_retrieval-specific.ipynb`](./EvaluationCode/evaluations_retrieval-specific.ipynb) | Evaluates **1 vs 1, M vs 1, 1 vs M** retrieval performance for **ADRD, Eye, Stroke** datasets. |
| [`evaluations_retrieval-covid.ipynb`](./EvaluationCode/evaluations_retrieval-covid.ipynb) | Evaluates overall retrieval performance (**Search All, Embedding Search, Query Expansion**) for **COVID-19** dataset. |
| [`evaluations_retrieval-covid-specific.ipynb`](./EvaluationCode/evaluations_retrieval-covid-specific.ipynb) | Evaluates **1 vs 1, M vs 1, 1 vs M** retrieval performance for **COVID-19** dataset. |

### 📊 Ranking Evaluation:
| Script | Description |
|--------|------------|
| [`evaluations_rerank.ipynb`](./EvaluationCode/evaluations_rerank.ipynb) | Evaluates overall **ranking performance** for **ADRD, Eye, Stroke** datasets using the **Re-ranking function**. |
| [`evaluations_rerank_specific.ipynb`](./EvaluationCode/evaluations_rerank_specific.ipynb) | Evaluates **1 vs 1, M vs 1, 1 vs M** ranking performance for **ADRD, Eye, Stroke** datasets. |
| [`evaluations_rerank-covid.ipynb`](./EvaluationCode/evaluations_rerank-covid.ipynb) | Evaluates overall **ranking performance** for **COVID-19** dataset using the **Re-ranking function**. |
| [`evaluations_rerank-covid-specific.ipynb`](./EvaluationCode/evaluations_rerank-covid-specific.ipynb) | Evaluates **1 vs 1, M vs 1, 1 vs M** ranking performance for **COVID-19** dataset. |

---

## 📖 Usage Guide

For detailed instructions on how to use **CDEMapper**, please refer to the **[CDEMapper User Manual](./CDEMapper_User_Manual)**.

---

## 📄 Citation

If you use **CDEMapper**, please cite:

```bibtex
@misc{wang2024cdemapperenhancingnihcommon,
      title={CDEMapper: Enhancing NIH Common Data Element Normalization using Large Language Models}, 
      author={Yan Wang and Jimin Huang and Huan He and Vincent Zhang and Yujia Zhou and Xubing Hao and Pritham Ram and Lingfei Qian and Qianqian Xie and Ruey-Ling Weng and Fongci Lin and Yan Hu and Licong Cui and Xiaoqian Jiang and Hua Xu and Na Hong},
      year={2024},
      eprint={2412.00491},
      archivePrefix={arXiv},
      primaryClass={cs.IR},
      url={https://arxiv.org/abs/2412.00491}, 
}


---

