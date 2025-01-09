# Text Mining Project
Project in the text mining course 732A81

This repository explores a comparative study on the performance of SQL-tuned T5 model and fine-tuning it on self made questions to see improvements. The best model is then incorporated into a Retrieval-Augmented Generation (RAG) pipeline. The analysis leverages a self-curated dataset of questions and answers, demonstrating the strengths and weaknesses of each approach.

## Project Overview

### Objectives
1. **Model Comparison**: Evaluate the effectiveness of a T5 model tuned to generate SQL queries versus a traditional fine-tuned T5 model on a domain-specific dataset.
2. **Integration**: Integrate the best approaches into a RAG pipeline for answering complex queries.
3. **Analysis**: Assess performance using metrics such as accuracy, exact matching and ROUGE 2, focusing on SQL execution success rates.

### Dataset
- **Source**: Self-created questions based on domain-specific knowledge.
- **Location**: The CSV dataset is hosted on Kaggle.
- **Format**: CSV files converted into SQL databases.
- **Scope**: Covers a range of years (2000-2015) with detailed metadata for realistic query generation.

### Key Components
1. **SQL-Tuned T5**: A T5 model([juierror/flan-t5-text2sql-with-schema-v2](https://huggingface.co/juierror/flan-t5-text2sql-with-schema-v2)) adapted to translate natural language queries into SQL statements.
2. **Fine-Tuned T5**: A T5 model fine-tuned on self made questions and SQL queries.
3. **RAG Pipeline**: Combines retrieval (SQL query execution) with generation (Llama-based answering  [meta-llama/Llama-3.3-70B-Instruct](https://huggingface.co/meta-llama/Llama-3.3-70B-Instruct)) to provide robust query responses.


The paper is written in latex in the ACL-style, the acl files are from [Acl-org github repo](https://github.com/acl-org/acl-style-files/) and are needed to go from [latex](https://github.com/Johhed15/Text-Mining-Project/blob/main/Text-mining-project.tex) to [pdf](https://github.com/Johhed15/Text-Mining-Project/blob/main/Text_mining.pdf).

## Question dictionary to Latex table

I've also made a function to go from the dictionaries with questions i python to latex so its easier and faster to add them as tables in the report. This function can be found here: [Dict to Latex](https://github.com/Johhed15/Text-Mining-Project/blob/main/latex_table_generator).


