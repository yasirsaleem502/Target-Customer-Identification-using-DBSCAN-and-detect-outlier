# Target Customer Identification Using DBSCAN and Show Outliers

![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![Scikit-Learn](https://img.shields.io/badge/Framework-Scikit--Learn-green)
![License](https://img.shields.io/badge/License-MIT-yellow)

## Project Overview

This project aims to identify target customers using the **DBSCAN** (Density-Based Spatial Clustering of Applications with Noise) algorithm. The focus is on segmenting customers based on their behaviors and spending habits while also highlighting outliers in the dataset. This approach allows for better marketing strategies and a deeper understanding of customer profiles.

## Table of Contents

- [Introduction](#introduction)
- [Dataset](#dataset)
- [Installation](#installation)
- [Usage](#usage)
- [Results](#results)
- [Outlier Detection](#outlier-detection)
- [Contributing](#contributing)
- [License](#license)
- [Contact](#contact)

## Introduction

Customer segmentation is crucial for businesses to tailor their marketing strategies effectively. This project leverages the DBSCAN algorithm to identify groups of similar customers based on specific features such as annual income and spending score, while also detecting outliers that may represent unique customer behaviors.

## Dataset

The dataset used in this project contains the following attributes:

| Attribute                | Type          | Description                                                                                                                                       |
|--------------------------|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| **CustomerID**           | Integer       | A unique identifier for each customer.                                                                                                           |
| **Gender**               | Categorical   | Represents the gender of each customer (Male/Female).                                                                                            |
| **Age**                  | Integer       | The age of the customer in years.                                                                                                               |
| **Annual Income (k$)**   | Numerical     | Represents the annual income of each customer in thousands of dollars.                                                                          |
| **Spending Score (1-100)** | Numerical   | A score assigned to each customer, indicating their spending behavior relative to their income.                                                 |

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
