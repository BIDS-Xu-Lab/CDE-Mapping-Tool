# CDE-Mapping-Tool
Evaluation codes and relevance datasets
All evaluation datasets are available in the EvaluationData folder, including one ADRD dataset, one Eye dataset, one Stroke dataset, and nine Covid datasets. You can use these datasets to test our CDEMapper tool at: https://cdemapper.clinicalnlp.org/.

To use the tool, you will need to sign up with your email if you do not already have an account. After that, you can upload our evaluation data or even your own data, provided it follows the same format. If you want to use your own data, create a CSV file with three required columns: Element, Description, and Value (where multiple values are separated by "|"). For reference, you can look at the data in the EvaluationData folder.

As described in our paper, you can use various search functions, such as "Search All", "Embedding Search", and "Query Expansion", to generate more accurate element candidates. The "Re-ranking" function, which is powered by the GPT-4o model, can also be used to obtain recommendations from the LLM. For mapping values, the "Value Linking" function will automatically match your value set with the target value set. Finally, click the "Download" button to get the result file.

Once you have the result file, you can use our evaluation code to evaluate your results. We provide eight evaluation codes in total:

* evaluations_retrieval.ipynb: Evaluates the overall retrieval performance ("Search All", "Embedding Search", "Query Expansion") for ADRD, Eye, and Stroke data.
* evaluations_retrieval-specific.ipynb: Evaluates ADRD, Eye, and Stroke data for 1 vs 1, M vs 1, and 1 vs M retrieval performance ("Search All", "Embedding Search", "Query Expansion").
* evaluations_retrieval-covid.ipynb: Evaluates the overall retrieval performance ("Search All", "Embedding Search", "Query Expansion") for Covid-19 data.
* evaluations_retrieval-covid-specific.ipynb: Evaluates Covid-19 data for 1 vs 1, M vs 1, and 1 vs M retrieval performance ("Search All", "Embedding Search", "Query Expansion").
* evaluations_rerank.ipynb: Evaluates the overall ranking performance for ADRD, Eye, and Stroke data based on the "Re-ranking" function.
* evaluations_rerank_specific.ipynb: Evaluates ADRD, Eye, and Stroke data for 1 vs 1, M vs 1, and 1 vs M ranking performance based on the "Re-ranking" function.
* evaluations_rerank-covid.ipynb: Evaluates the overall ranking performance for Covid-19 data based on the "Re-ranking" function.
* evaluations_rerank-covid-specific.ipynb: Evaluates Covid-19 data for 1 vs 1, M vs 1, and 1 vs M ranking performance based on the "Re-ranking" function.
