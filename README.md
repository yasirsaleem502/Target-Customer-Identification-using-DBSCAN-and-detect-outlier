# Target Customer Identification Using DBSCAN and Detect Outliers

![Python](https://img.shields.io/badge/Python-3.8+-green)
![Jupyter Notebook](https://img.shields.io/badge/Tools-Jupyter%20Notebook-orange)
![Scikit-learn](https://img.shields.io/badge/Library-Scikit--learn-blue)
![Pandas](https://img.shields.io/badge/Library-Pandas-yellow)
![Matplotlib](https://img.shields.io/badge/Library-Matplotlib-lightblue)

## Project Overview

The objective of this case study is to develop a clustering model that segments customers based on their spending behavior, income, and other demographics. Additionally, the model should identify outliers—customers whose behavior significantly deviates from the general population. Outliers can often represent either very high-value or very low-value customers, both of which could require different marketing approaches

## Objective
The primary objectives of this analysis are:
- To segment customers based on demographics and spending behaviour.
- To understand the relationship between income, age, gender, and spending score.
- To provide actionable insights for targeted marketing strategies

## Table of Contents
- [Introduction](#introduction)
- [Features](#features)
- [Dataset](#dataset)
- [Methodology](#methodology)
- [DBSCAN Algorithm](#dBSCAN-algorithm)
- [Contact](#contact)

- 
## Introduction

Understanding customer behavior is vital for businesses, especially in the retail sector. By analyzing customer demographics and spending habits, companies can enhance their marketing strategies, improve customer satisfaction, and boost overall sales. This case study focuses on analyzing a customer dataset from a mall to derive insights into customer segments based on gender, age, annual income, and spending score.

## Dataset

This dataset provides essential information for segmentation by combining demographic data with financial and behavioural indicators.

The dataset used in this project contains the following attributes:

| Attribute                | Type          | Description                                                                                                                                       |
|--------------------------|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| **CustomerID**           | Integer       | A unique identifier for each customer.                                                                                                           |
| **Gender**               | Categorical   | Represents the gender of each customer (Male/Female).                                                                                            |
| **Age**                  | Integer       | The age of the customer in years.                                                                                                               |
| **Annual Income (k$)**   | Numerical     | Represents the annual income of each customer in thousands of dollars.                                                                          |
| **Spending Score (1-100)** | Numerical   | A score assigned to each customer, indicating their spending behavior relative to their income.     |

Dataset link: https://www.kaggle.com/datasets/muhammadyasirsaleem/mall-customer-dataset


## Methodology

To solve the problem of customer segmentation and outlier detection, the DBSCAN clustering algorithm was applied. Unlike other clustering methods such as K-Means, DBSCAN is ideal for this scenario because it does not require prior knowledge of the number of clusters. Additionally, DBSCAN is robust in detecting noise and outliers, which can represent unusual customers in this context.

### DBSCAN Algorithm
DBSCAN (Density-Based Spatial Clustering of Applications with Noise) is a clustering algorithm that groups points in dense regions while marking points in sparse regions as outliers. The algorithm works by defining two key parameters:

- eps: The maximum distance between two samples for them to be considered as part of the same neighborhood.
- min_samples: The minimum number of points required to form a dense region (i.e., a cluster).
  
### Key advantages of DBSCAN include:

- Detecting clusters of varying shapes and sizes.
- Identifying outliers or noise, which are customers whose behavior deviates significantly from the average.

 - Steps Followed

### Data Preprocessing:

- Converted categorical data (Gender) into numerical format using label encoding.
- Scaled the numerical data using StandardScaler to normalize features such as age, income, and spending score.
  
### Clustering with DBSCAN:

- Applied DBSCAN with varying parameters (eps and min_samples) to identify clusters and outliers.
- Used the Manhattan distance metric for distance calculations, as it performed better for this dataset compared to Euclidean distance.
  
### Outlier Detection:

- Outliers were detected by DBSCAN and labeled as -1 in the results. 
- These outliers represent customers who do not belong to any of the clusters and exhibit unusual spending behavior or income.

### Evaluation:
- Evaluated clustering performance using the Silhouette Score, which measures how well points are clustered in terms of cohesion and separation.
- Visualized the clusters and outliers using Principal Component Analysis (PCA) for dimensionality reduction.








## Installation

To run this project, you need to have Python 3.8 or above and the following libraries installed:

- `pandas`
- `numpy`
- `matplotlib`
- `seaborn`
- `scikit-learn`

You can install the required libraries using pip:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn
