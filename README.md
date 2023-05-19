# ACE
# Childhood Trauma Assessment for Predicting Chronic Conditions

## Problem Statement:
Can a machine learning model use childhood trauma assessments to predict diabetes and high blood pressure in adults, and can this tool be used for preventative care? The model will be evaluated based on accuracy and F1-score, but more importantly will need high sensitivity to prevent false negatives that could hinder treatment for patients that need more care. The goal is for the sensitivity to be above 90% in order for it to be considered useful for preventative care.

## Executive Summary

The Childhood Trauma Assessment for Predicting Chronic Conditions project aims to explore the possibility of using childhood trauma assessments, specifically Adverse Childhood Experiences (ACE) scores, to predict the likelihood of adults developing chronic conditions such as diabetes and high blood pressure. The goal is to develop a machine learning model that can aid healthcare providers in identifying patients who may require preventative care based on their ACE scores.

Three different machine learning models were trained and evaluated using the Behavioral Risk Factor Surveillance System (BRFSS) dataset, focusing on diabetes and high blood pressure as the target variables. The models achieved technically high sensitivity, but they were unable to provide a useful prediction model. The models exhibited a tendency to predict true positives by increasing the number of false positives at a high rate, making them unreliable for preventative care purposes.

The limitations of the models include the reliance on 2021 data, the absence of distinguishing between type 1 and type 2 diabetes in the dataset, and potential biases introduced by the data collection protocol. Future improvements could involve incorporating data from multiple years, refining the target variable to differentiate between diabetes types, and addressing the biases associated with the data collection process.

Despite the current models' limitations, this project represents a step forward in utilizing ACE scores for preventative care. Further research, utilizing a more diverse and representative dataset and additional resources, may lead to the development of a more accurate and useful machine learning tool for healthcare providers.

## Data Dictionary

[CDC Data Dictionary]('https://www.cdc.gov/brfss/annual_data/2021/llcp_varlayout_21_onecolumn.html')

[CDC Codebook]('https://www.cdc.gov/brfss/annual_data/2021/pdf/codebook21_llcp-v2-508.pdf')

The following variables are included in the dataset used for the Childhood Trauma Assessment for Predicting Chronic Conditions project:

- `DIABETE4` (Target variable for diabetes prediction): Binary variable indicating the presence (1) or absence (0) of diabetes.
- `BPHIGH6` (Target variable for high blood pressure prediction): Binary variable indicating the presence (1) or absence (0) of high blood pressure.
- Other variables: The dataset contains various input features related to childhood trauma assessments, socio-demographic information, and health-related factors. These features include information such as age, gender, race, education level, income, ACE scores, and lifestyle habits.

Please refer to the original dataset documentation for detailed descriptions and further information about each variable.

