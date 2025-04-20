# EHRSQL: A Practical Text-to-SQL Benchmark for Electronic Health Records

## Overview

EHRSQL is a large-scale, high-quality dataset designed for text-to-SQL question answering on Electronic Health Records from [MIMIC-III](https://physionet.org/content/mimiciii/1.4/) and [eICU](https://physionet.org/content/eicu-crd/2.0/). The dataset includes questions collected from 222 hospital staff, such as physicians, nurses, insurance reviewers, and health records teams. It can be used to test three aspects of QA models: generating a wide range of SQL queries asked in the hospital workplace, understanding various types of time expressions (absolute, relative, or both), and the capability to abstain from answering (querying the database) when the model's prediction is not confident.

The dataset is released along with our paper titled [EHRSQL: A Practical Text-to-SQL Benchmark for Electronic Health Records](https://arxiv.org/abs/2301.07695) (NeurIPS 2022 Datasets and Benchmarks). For further details, please refer to our paper.

## Data Source

To access the databases, PhysioNet’s credentialed access (see license) is needed. Below are the links to the download pages.

- [MIMIC-III-1.4](https://physionet.org/content/mimiciii/1.4/)

## Getting Started

###  Requirments and Installation
- Python version >= 3.9
```
git clone https://github.com/glee4810/EHRSQL.git
cd EHRSQL
conda env create -f environment.yml
conda activate EHRSQL
```

## Executions

### T5 Model(s) Generation (Run in Google Colab)
- `MIMIC_III_T5_Base.ipynb` : Run this for training with mimic iii train.json data with-out the schema.

- `MIMIC_III_T5_Base_WithSchema.ipynb` : Run this for training with mimic iii train.json data with the schema.

### Evaluations (Run locally)
- `evaluations.ipynb` : Run all cells to get different evaluation matrixs.

### Analyize Training logs (Run locally)
- `training_log_analysis.ipynb` : This will give average epoch time and training loss chart.
