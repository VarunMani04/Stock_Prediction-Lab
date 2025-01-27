---
title: "Amazon Stock Price Prediction"
author: "Data Science Project"
date: "`r format(Sys.time(), '%d %B, %Y')`"
output: 
  html_document:
    toc: true
    toc_float: true
    theme: cosmo
---

```{r setup, include=FALSE}
knitr::opts_chunk$set(echo = TRUE)
```

## Project Overview

A machine learning project that analyzes and predicts Amazon (AMZN) stock prices using multiple regression models. The project compares the performance of Linear Regression, Lasso Regression, and XGBoost models to predict closing prices based on historical stock data.

## Features

* Historical stock data analysis from 1997 to 2021
* Comprehensive exploratory data analysis (EDA) with visualizations
* Multiple prediction models:
    + Linear Regression
    + Lasso Regression
    + XGBoost
* Performance comparison between models using RMSE and R² metrics
* Feature engineering including daily returns calculation
* Interactive visualizations using ggplot2

## Required Libraries

```{r libraries, eval=FALSE}
library(tidyverse)
library(quantmod)
library(xgboost)
library(caret)
library(glmnet)
library(lubridate)
library(plotly)
```

## Dataset

The project uses historical Amazon stock data (AMZN) from May 15, 1997, to July 8, 2021, fetched using the quantmod package. The dataset includes:

* Opening price
* Closing price
* High price
* Low price
* Adjusted closing price
* Trading volume
* Daily returns

## Model Performance

```{r model-performance, eval=FALSE}
# Model evaluation using RMSE and R²
model_metrics <- data.frame(
  Model = c("Linear Regression", "Lasso", "XGBoost"),
  RMSE = numeric(3),
  R_squared = numeric(3)
)
```

## Visualizations

* Historical stock price trends
* Monthly average price analysis
* Daily returns distribution
* Trading volume analysis
* Correlation heatmap
* Actual vs Predicted price comparisons
