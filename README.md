# Adverse Childhood Experiences for Predicting Chronic Health Conditions
---
### README Contents:
- [Introduction](#Introduction)
- [Problem Statement](#Problem-Statement)
- [Executive Summary](#Executive-Summary)
- [Data Description](#Data-Description)
- [Data Acquisition, Ingestion, and Cleaning](#Data-Acquisition,-Ingestion,-and-Cleaning)
- [Datasets](#Datasets)
- [Data Dictionary](#Data-Dictionary)
- [Software Requirements](#Software-Requirements) 

### Code Contents
1. [Data Collection](./Code/Data.ipynb)
2. [EDA and Cleaning](./Code/EDA.ipynb)
3. [Models](./Code/Modeling.ipynb)
---
## Introduction
---


## Problem Statement:
Can a machine learning model use childhood trauma assessments to predict diabetes and high blood pressure in adults, and can this tool be used for preventative care? The model will be evaluated based on accuracy and F1-score, but more importantly will need high sensitivity to prevent false negatives that could hinder treatment for patients that need more care. The goal is for the sensitivity to be above 90% in order for it to be considered useful for preventative care.

## Executive Summary
---
The Adverse Childhood Experiences for Predicting Chronic Health Conditions project aims to explore the possibility of using childhood trauma assessments, specifically Adverse Childhood Experiences (ACE) scores, to predict the likelihood of adults developing chronic conditions such as diabetes and high blood pressure. The goal is to develop a machine learning model that can aid healthcare providers in identifying patients who may require preventative care based on their ACE scores.

Three different machine learning models were trained and evaluated using the Behavioral Risk Factor Surveillance System (BRFSS) dataset, focusing on diabetes and high blood pressure as the target variables. The models achieved technically high sensitivity, but they were unable to provide a useful prediction model. The models exhibited a tendency to predict true positives by increasing the number of false positives at a high rate, making them unreliable for preventative care purposes.

The limitations of the models include the reliance on 2021 data, the absence of distinguishing between type 1 and type 2 diabetes in the dataset, and potential biases introduced by the data collection protocol. Future improvements could involve incorporating data from multiple years, refining the target variable to differentiate between diabetes types, and addressing the biases associated with the data collection process.

Despite the current models' limitations, this project represents a step forward in utilizing ACE scores for preventative care. Further research, utilizing a more diverse and representative dataset and additional resources, may lead to the development of a more accurate and useful machine learning tool for healthcare providers.

## Data Description
---
The primary dataset used in this analysis is the 'clean_ace.csv' file, which contains information on the Adverse Childhood Experiences questionnaire and the presence of diabetes and high blood pressure in adults. This data in this dataset originated from the `LLCP2021.XPT` file provided by the Centers for Disease Control and Prevention. The 'clean_ace.csv' dataset includes columns DIABETE4, BPHIGH6, ACEDEPRS, ACEDRINK, ACEDRUGS, ACEPRISN, ACEDIVRC, ACEPUNCH, ACEHURT1, ACESWEAR, ACETOUCH, ACETTHEM, ACEHVSEX, ACEADSAF, and ACEADNED. These columns represent the presence of adverse childhood experiences (ACEs) and chronic conditions.

## Data Acquisition, Ingestion, and Cleaning
---
The data used in this analysis was obtained from the [CDC's BRFSS questionnaire](https://www.cdc.gov/brfss/annual_data/annual_2021.html). The initial dataset was cleaned and preprocessed to remove any missing or unnecessary values. Feature engineering techniques were employed to transform variables to be better suited for machine learning models and to group characteristics. 


## Datasets
---
* [`LLCP2021.XPT`](./Datasets/LLCP2021.XPT): Original BRFSS dataset for 2021 
* [`ace.csv`](./Datasets/ace.csv): Necessary variables from the original dataset saved for efficiency when cleaning  
* [`clean_ace.csv`](./Datasets/clean_ace.csv): Cleaned dataset with only the necessary variables for modeling


## Data Dictionary
---
Original BRFSS datasets data dictionaries and codebooks: 
[CDC Data Dictionary](https://www.cdc.gov/brfss/annual_data/2021/llcp_varlayout_21_onecolumn.html)
[CDC Codebook](https://www.cdc.gov/brfss/annual_data/2021/pdf/codebook21_llcp-v2-508.pdf)

| Feature                | Type     | Dataset        | Description                                                      |
|------------------------|----------|----------------|------------------------------------------------------------------|
| **DIABETE4**               | int64    | clean_ace.csv  | Indicates whether the individual has diabetes                     |
| **BPHIGH6**                | int64    | clean_ace.csv  | Indicates whether the individual has high blood pressure          |
| **ACEDEPRS**               | int64    | clean_ace.csv  | Indicates if the individual lived with anyone who was depressed, mentally ill, or suicidal in childhood |
| **ACEDRINK**               | int64    | clean_ace.csv  | Indicates if the individual lived with anyone who was a problem drinker or alcoholic in childhood |
| **ACEDRUGS**               | int64    | clean_ace.csv  | Indicates if the individual lived with anyone who used illegal street drugs or who abused prescription medications in childhood |
| **ACEPRISN**               | int64    | clean_ace.csv  | Indicates if the individual lived with anyone who served time or was sentenced to serve time in a prison, jail, or other correctional facility in childhood |
| **ACEDIVRC**               | int64    | clean_ace.csv  | Indicates if the individual experienced parents' divorce/separation in childhood |
| **ACEPUNCH**               | int64    | clean_ace.csv  | Indicates if the individuals' parents or adults in their home ever slapped, hit, kicked, punched or beat each other up |
| **ACEHURT1**               | int64    | clean_ace.csv  | Indicates if the individuals' parents or adults in their home ever hit, beat, kicked, or physically hurt them in any way |
| **ACESWEAR**               | int64    | clean_ace.csv  | Indicates if the individual had a parent or adult in their home ever swear at them, insult them, or put them down |
| **ACETOUCH**               | int64    | clean_ace.csv  | Indicates if the individual had anyone at least 5 years older than them or an adult, ever touch them sexually |
| **ACETTHEM**               | int64    | clean_ace.csv  | Indicates if the individual had anyone at least 5 years older than them or an adult, try to make them touch them sexually |
| **ACEHVSEX**               | int64    | clean_ace.csv  | Indicates if the individual had anyone at least 5 years older than them or an adult, force them to have sex |
| **ACEADSAF**               | int64    | clean_ace.csv  | Indicates if the individual had an adult in their household who made them feel safe and protected |
| **ACEADNED**               | int64    | clean_ace.csv  | Indicates if the individual had an adult in their household who tried hard to make sure their basic needs were met |

## Software Requirements
---
The following software libraries are required to run the analysis:

- Pandas
- NumPy
- Scikit-learn
- Matplotlib
- Seaborn
- Keras 
- Imbalanced-learn  
- Jupyter Notebook


