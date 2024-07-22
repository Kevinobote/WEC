# Predicting Power Output in Large-Scale Wave Energy Farms

## Table of Contents

1. [Introduction](#introduction)
2. [Dataset Description](#dataset-description)
3. [Methodology](#methodology)
4. [Data Exploration](#data-exploration)
5. [Predictive Modeling](#predictive-modeling)
6. [Results and Discussion](#results-and-discussion)
7. [Conclusion](#conclusion)
8. [References](#references)

## Introduction

### Background

Wave energy is a rapidly advancing renewable energy source that harnesses the power of ocean waves to generate electricity. It holds great promise in addressing global challenges such as climate change and energy security. However, optimizing the energy output in large wave farms is a complex problem due to the computationally expensive hydrodynamic interactions between wave energy converters (WECs). This project aims to develop efficient and accurate models to predict the power output of wave farms, which is crucial for advancing this technology.

### Research Problem

The primary research problem addressed is the optimization of energy output in large-scale wave farms. The dataset consists of configurations involving 49 and 100 WECs, along with their power outputs and related variables. The challenge lies in predicting the total power output based on these configurations and overcoming the computational difficulties associated with the interactions between multiple WECs.

### Objectives

1. **Develop a Predictive Model**: Create a machine learning model to accurately estimate the total power output of large-scale wave farms based on WEC configurations.
2. **Analyze Key Features**: Identify and analyze the most significant features that influence the power output of wave farms.
3. **Optimize Model Performance**: Implement various machine learning techniques and evaluate their performance to ensure the model's accuracy and efficiency.

### Hypothesis

1. **WEC Configuration Impact**: The configuration of WECs significantly impacts the total power output of a wave farm.
2. **Machine Learning Efficiency**: A well-trained machine learning model can accurately predict the power output of a wave farm, reducing the need for complex hydrodynamic calculations.

## Dataset Description

The dataset used in this project was created to develop a surrogate model for predicting the total power output of large wave farms. It contains 63,600 instances and 149 features, covering 49 and 100 WEC configurations under Perth and Sydney wave scenarios.

### Source of Data

- **Creators**: Mehdi Neshat, Bradley Alexander, Nataliia Sergiienko, Markus Wagner
- **Published**: 2023
- **License**: Creative Commons Attribution 4.0 International (CC BY 4.0)
- **DOI**: [10.24432/C5GG7Q](https://doi.org/10.24432/C5GG7Q)

### Period Collected

- **Year and Month/Day**: Data was donated on September 16, 2023.

### How it was Collected

The dataset was derived from a study published at the GECCO conference, which used a multi-strategy evolutionary framework to optimize large wave farms.

### Under What Conditions it was Collected

The data collection involved extensive simulations using the Phoenix HPC service at the University of Adelaide to account for hydrodynamic interactions between WECs.

### Variables

| Variable Name | Role    | Type    | Description                              | Units | Missing Values |
| ------------- | ------- | ------- | ---------------------------------------- | ----- | --------------- |
| X1            | Feature | Integer | X-coordinate of the 1st WEC              | -     | No              |
| Y1            | Feature | Integer | Y-coordinate of the 1st WEC              | -     | No              |
| ...           | ...     | ...     | ...                                      | ...   | ...             |
| Xn            | Feature | Integer | X-coordinate of the nth WEC              | -     | No              |
| Yn            | Feature | Integer | Y-coordinate of the nth WEC              | -     | No              |
| Power         | Target  | Real    | Total power output of the wave farm      | kW    | No              |
| Q-factor      | Feature | Real    | Hydrodynamic interaction factor          | -     | No              |

## Methodology

1. **Data Loading and Inspection**: Loaded the dataset from CSV files and displayed information about the datasets, including the shape and a statistical summary.

2. **Handling Null Values**: Checked for and handled null values by filling them with the mean of the respective columns.


3. **Exploratory Data Analysis (EDA)**: Performed EDA to understand the distribution and relationships within the data, including:
   - Distribution of `Total_Power`
   - Correlation matrix
   - Identification of top features correlated with `Total_Power`

4. **Predictive Modeling**: Trained and evaluated machine learning models, specifically Linear Regression, to predict `Total_Power`.

## Data Exploration

### Descriptive Statistics

Provided summary statistics, including mean, median, mode, standard deviation, and range for `Total_Power` and other key features.

### Distribution Analysis

Visualized the distribution of `Total_Power` using histograms and KDE plots to understand its spread and identify outliers.

### Correlation Analysis

Examined the correlation matrix to understand the relationships between `Total_Power` and other features.

### Top Features Analysis

Identified the top features most strongly correlated with `Total_Power` to assist in feature selection.

## Results and Discussion

The surrogate model developed accurately predicts the power output of large-scale wave energy farms. The exploratory data analysis provided valuable insights into data distribution and feature significance. The predictive model demonstrated promising performance with the evaluation metrics.

## Conclusion

This project successfully developed a surrogate model for predicting power output in large-scale wave energy farms. Through thorough data exploration, cleaning, and machine learning modeling, significant accuracy was achieved. Future work may involve exploring more advanced models and incorporating additional environmental variables to enhance prediction accuracy.

## References

- Neshat, M., Alexander, B., Sergiienko, N., & Wagner, M. (2023). Large-scale Wave Energy Farm. UCI Machine Learning Repository. [DOI: 10.24432/C5GG7Q](https://doi.org/10.24432/C5GG7Q)
- Neshat, M., Alexander, B., Sergiienko, N., & Wagner, M. (2020). Optimisation of large wave farms using a multi-strategy evolutionary framework. In Proceedings of the 2020 Genetic and Evolutionary Computation Conference, pp. 1150-1158.
