---
title: Building a classification model to predict type-2 diabetes
excerpt: A machine learning model to predict type-2 diabetes
layout: single
author_profile: true
toc: true
toc_sticky: true
header:
  teaser: /assets/obsidian/2b2c15a072165ff6293fa65fe74937c4.png
---

## **Business Scenario**

Diabetes is a common chronic disease caused by increasing blood sugar level in the body above a certain threshold. Diabetes is classified into type-1 and type-2, in which type-2 diabetes patients account for the majority number of total diabetes patients. Early detection is very important because it helps to reduce complications and minimize death rate.  Therefore, this app is aim to build a machine learning classification model to predict type-2 diabetes.

## Techniques

- Download data from URL and extract data: requests, zipfile
- Data manipulation: pandas, numpy
- Data Visualization: matplotlib, seaborn
- Handling imbalanced datasets: imbalanced-learn
- Encoding, scaling features, model training: scikit-learn
- Model deploying via web app: streamlit

## **Workflow**

### 1. Data Collection 
- **Download and Extract Data**: Dataset is downloaded from [Behavioral Risk Factor Surveillance System](https://www.cdc.gov/brfss/annual_data/annual_2022.html) (BRFSS) 2022, which was released on July 07, 2023. BRFSS is one of the biggest on-going health-related telephone surveys system in the world, which collects health-related risk behavior, chronic health issues and other data from people more than 18 years old living in the US and participating US territories annually.
- Selects specific columns relevant to the analysis: We select 15 features related to diabetes in the original dataset to analyze, in which DIABETE4 is output and 14 remaining attributes are input.
<img src="/assets/obsidian/392e6365c6f637f35c2b527b25fbdfd3.png" />
- Maps categorical values to more readable labels: because original data is represented in number value, we map them to their actual values by referencing the [code book](https://www.cdc.gov/brfss/annual_data/2022/zip/codebook22_llcp-v2-508.zip).
- Renames columns to more descriptive names: Since original column name in 2022 BRFSS is complex, we will change names of columns into simpler strings.
<img src="/assets/obsidian/52504088f15e583626b680192df01723.png" />

### 2. Data Preprocessing 

- Handle duplicates, missing values
- Handle records that have the values "Refused" or "Don't know/Not sure"
- Handle outliers which is our of range Q1 - 1.5 IQR and Q3 + 1.5 IQR

### 3. **Model Building**

- Applies encoding and scaling to the data
- Uses sampling methods to handle imbalanced datasets
- Model Training: Defines a set of basic models (e.g., Decision Tree, Random Forest, Gradient Boosting, XGBoost, LightGBM). Fine-tuning on the best performing models and then compares them based on performance metrics and select the best one

### 4. **Model Deploying**

- Load the best model from the pickle file
- Uses the loaded model to make predictions on new data
- Building a streamlit app to deploy the model online

## Functionalities

- predict type-2 diabetes probabilities of an individual from user input
<img src="/assets/obsidian/2b2c15a072165ff6293fa65fe74937c4.png" />

<img src="/assets/obsidian/4709f53bcbf8cc448e40b9ab2022be79.png" />

<img src="/assets/obsidian/79f24330f8b4c12f21f08e7482adfc18.png" />

- determine which indicators are highly associated with type-2 diabetes

<img src="/assets/obsidian/ef7a10f20394540cc9f4b7e4f531ff9b.png" />

<img src="/assets/obsidian/5ff167211d7419d58b85835c2c9bf237.png" />
<img src="/assets/obsidian/5eb126a9bb682912ed6bdfad01637843.png" />

<img src="/assets/obsidian/e4fcf031fe0afdfc8da91339302fef90.png" />

## Demo

<iframe width="560" height="315" src="https://www.youtube.com/embed/hLZoEJCJGlo?si=LTgYkWrBklLzY8Xi" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>





