# CDE-Mapping-Tool
Evaluation codes and relevance datasets
All of evaluation datasets are in the EvaluationData, including one ADRD data, one Eye data, one Stroke data, and nine Covid data. You can use all of these data to test our CDEMapper tool: https://cdemapper.clinicalnlp.org/

For this tool, you should sign up with your email first if you don't have an account. After that, you can upload our evaluation data even your own data with the same format as our evaluation data to test our tool.
If you want to use your own data, you should create a CSV file with three required columns: Element, Description, and Value, where Values are split by "|". Specificlly, you can refer to the data in the EvaluationData folder.
As our paper said, you can use various search functions like "search all", "search", "embedding search" and "query expansion" to generate more accurate element candidates. You can also use the "Re-ranking" function which is achieved by the GPT-4o model to obtain the LLM's recommendation. If you need map values, you can also use the "Value Linking" function to automatically match your own value set with the target value set. Finally, you can download the results by clicking the "Download" button to get the result file.

Once you get the result file, you can you our evaluation code to evalute your results. We totaly have eight evaluation codes:
* evaluations_retrieval.ipynb: It is used for evaluating "ADRD", "Eye", and "Stroke" data on overall performance
* 
