# CDE-Mapping-Tool
**Evaluation codes and relevance datasets**

CDEMapper is an Elasticsearch and Large Language Model (LLM)-powered mapping tool for biomedical and clinical researchers to efficiently map their study variables to the NIH CDE (Common Data Elements). CDEMapper integrates both essential and advanced services into a user-centered mapping workflow, allowing users to select different mapping strategies based on their project's needs or preferences. It provides the top 10 recommended CDEs for each user-provided variable, allowing users to select the most suitable match and corresponding values. Additionally, it supports further searches for NIH CDEs not included in the top 10 recommendations. The CDEMapper indexed all 23,328 CDEs from 19 Collections of the NIH CDE Repository, as of October 21, 2024. The LLM used in the CDEMapper V 1.1.0 is GPT-4o.

To evaluate the tool’s mapping capability, we collected four domains of data dictionaries or date elements, referred to as Eye (American Academy of Ophthalmology IRIS ® Registry (Intelligent Research in Sight) Analytics Data Dictionary), Stroke (Human Circadian/Diurnal Biology and Stroke Common Data Elements), ADRD (The National Alzheimer’s Coordinating Center - Uniform Data Set (UDS)), and COVID-19 (COVID-19 Therapeutic Trial Common Data Elements). The four datasets contained a total of 494 data elements and have been manually mapped to different domain-related NIH CDE collections for coverage assessment and tool performance evaluation.

Three mapping settings were established based on the annotators’ manual analysis, including "1 vs 1," "M vs 1," and "1 vs M." In "1 vs 1" mappings, one source element maps to a unique target element. In "M vs 1" mappings, multiple source elements map to a single target element. In "1 vs M" mappings, one source element maps to multiple target elements. If a target CDE was not found, no mapping was created for that entry. Gold standards were manually established by two annotators. In cases of conflict, the annotators engaged in discussions to resolve discrepancies and reach consensus. After achieving annotation consensus, we finalized 264 entries with effective mapping results for results evaluation.

Below are the evaluation codes:

* evaluations_retrieval.ipynb: Evaluates the overall retrieval performance ("Search All", "Embedding Search", "Query Expansion") for ADRD, Eye, and Stroke data.
* evaluations_retrieval-specific.ipynb: Evaluates ADRD, Eye, and Stroke data for 1 vs 1, M vs 1, and 1 vs M retrieval performance ("Search All", "Embedding Search", "Query Expansion").
* evaluations_retrieval-covid.ipynb: Evaluates the overall retrieval performance ("Search All", "Embedding Search", "Query Expansion") for Covid-19 data.
* evaluations_retrieval-covid-specific.ipynb: Evaluates Covid-19 data for 1 vs 1, M vs 1, and 1 vs M retrieval performance ("Search All", "Embedding Search", "Query Expansion").
* evaluations_rerank.ipynb: Evaluates the overall ranking performance for ADRD, Eye, and Stroke data based on the "Re-ranking" function.
* evaluations_rerank_specific.ipynb: Evaluates ADRD, Eye, and Stroke data for 1 vs 1, M vs 1, and 1 vs M ranking performance based on the "Re-ranking" function.
* evaluations_rerank-covid.ipynb: Evaluates the overall ranking performance for Covid-19 data based on the "Re-ranking" function.
* evaluations_rerank-covid-specific.ipynb: Evaluates Covid-19 data for 1 vs 1, M vs 1, and 1 vs M ranking performance based on the "Re-ranking" function.

Reference: Wang Y, Huang J, He H, Zhang V, Zhou Y, Hao X, Ram P, Qian L, Xie Q, Weng R, Lin F, Hu Y, Cui L, Jiang X, Xu H, Hong N. CDEMapper: Enhancing NIH Common Data Element Normalization using Large Language Models.  https://arxiv.org/abs/2412.00491

