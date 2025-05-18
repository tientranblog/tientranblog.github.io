---
title: Building a time series model to forecast COVID-19 new cases 
excerpt: A time series model to predict number of COVID-19 case for a selected country
layout: single
author_profile: true
toc: true
toc_sticky: true
header:
  teaser: /assets/obsidian/486c43060ef00da98947be16bb4765da.png
---
## **Business Scenario**

This app provides an interactive, visual, and quantitative COVID-19 forecasting tool using advanced time series and machine learning techniques. The training dataset originates from COVID-19 data curated by Our World in Data (OWID), based on reports from [the Johns Hopkins University Center for Systems Science and Engineering (JHU CSSE)](https://raw.githubusercontent.com/owid/covid-19-data/master/public/data/jhu/full_data.csv). It offers daily time series information on confirmed cases and deaths across various countries and regions. Note that JHU CSSE stopped updating this dataset as of March 10, 2023. The aim of this app is to anticipate case surges and supports data-driven decision-making.

## **Techniques**

- **Time Series Forecasting:**
  - **SARIMA Model:** Captures seasonality and trends in COVID-19 case data.
  - **LightGBM Regressor:** Models residuals from SARIMA to capture fine-grained, non-linear patterns.
- **Data Smoothing:** 30-day rolling mean to reduce noise in daily case counts.
- **Model Evaluation:** MAE, RMSE, and MAPE metrics.

## **Workflow**

### Step 1: Data Loading
- Fetches global COVID-19 data from an online CSV.
- Filters by user-selected country.

### Step 2: Preprocessing
- Converts dates, sets index, and smooths new cases.

### Step 3: Modelling
- Splits data into training and test sets based on forecast horizon.
- Fits SARIMA on training data.
- Computes residuals and creates lag features.
- Trains LightGBM on residuals.
- Combines SARIMA and LightGBM predictions for final forecast.

### Step 4: Evaluation
- Calculates and displays error metrics.

### Step 5: Visualization
- Plots actual vs. predicted cases for the forecast period.

## **Functionalities**

Interactive plot of forecast vs. actual cases on main page (default Country = `United States` and Forecast Horizon = `30` days)

<img src="/assets/obsidian/486c43060ef00da98947be16bb4765da.png" />

Dropbox for country and forecast horizon selection. Model performances are displayed on sidebar

<img src="/assets/obsidian/9ce97decf3f7bd3eab64d959730f4395.png" />

## **Demo**

[Web App](https://covid-19-prediction-ztgs.onrender.com)

<iframe width="560" height="315" src="https://www.youtube.com/embed/fkAlOTXT-I4?si=gLKcDMv4G8mhXZ4r" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
