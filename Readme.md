# Wave Energy Farm Optimization Project

## Introduction

### Background
Wave energy is a promising renewable energy source that captures the energy from ocean waves to generate electricity. It is an area of increasing interest due to its potential to provide sustainable and reliable energy. However, optimizing energy output from wave farms presents a significant challenge. The complex interactions between multiple wave energy converters (WECs) in a large-scale farm can impact the efficiency and effectiveness of power generation. Accurately predicting the total power output from such configurations requires advanced analytical methods and robust modelling to handle these interactions and enhance overall performance.

### Research Problem
The primary research problem of this project is to develop an accurate predictive model for the total power output of large-scale wave energy farms. The datasets involve configurations of wave energy converters (WECs) at different scales and locations, and the goal is to address the computational complexity associated with their interactions. By understanding and predicting the power output accurately, we can optimize the layout and operation of wave farms, leading to more efficient energy generation and better utilization of resources. This requires addressing challenges in data analysis, feature significance, and model performance.

### Objectives
1. **Develop a Predictive Model**: Create a machine learning model to accurately estimate the total power output of large-scale wave farms based on various WEC configurations. This model should be able to generalize well across different datasets.
2. **Analyze Key Features**: Identify and evaluate the most significant features that influence power output, such as spatial coordinates and hydrodynamic factors. The aim is to understand how these features impact total power and provide insights for optimization.
3. **Optimize Model Performance**: Implement and compare various machine learning techniques to ensure the model’s accuracy and efficiency. The objective is to refine the model based on performance metrics and feature importance to achieve optimal predictions.

### Hypothesis
1. **WEC Configuration Impact**: The configuration of WECs significantly impacts the total power output of the wave farm. By optimizing the arrangement of WECs, we can improve the overall power generation efficiency.
2. **Machine Learning Efficiency**: A well-trained machine learning model can accurately predict the power output of wave farms, potentially reducing the reliance on complex hydrodynamic calculations and improving decision-making in wave farm management.

## Methodology, Results, and Discussion

### Data Description
The dataset used for this project contains detailed information about wave energy converters and their power outputs under various configurations. It includes:

- **Source of Data**: The data was created by Mehdi Neshat, Bradley Alexander, Nataliia Sergiienko, and Markus Wagner, and it was published in 2023. It is licensed under Creative Commons Attribution 4.0 International (CC BY 4.0).
- **Period Collected**: Data was provided on September 16, 2023.
- **How it was Collected**: The data was derived from simulations conducted using the Phoenix HPC service at the University of Adelaide, which accounted for hydrodynamic interactions between WECs.
- **Under What Conditions it was Collected**: Extensive simulations were performed to model the interactions between WECs under various wave conditions, providing a comprehensive dataset for analysis.

#### Variables Description

| Variable Name | Role    | Type    | Description                              | Units | Missing Values |
| ------------- | ------- | ------- | ---------------------------------------- | ----- | --------------- |
| X1            | Feature | Integer | X-coordinate of the 1st WEC              | -     | No              |
| Y1            | Feature | Integer | Y-coordinate of the 1st WEC              | -     | No              |
| ...           | ...     | ...     | ...                                      | ...   | ...             |
| Xn            | Feature | Integer | X-coordinate of the nth WEC              | -     | No              |
| Yn            | Feature | Integer | Y-coordinate of the nth WEC              | -     | No              |
| Power         | Target  | Real    | Total power output of the wave farm      | kW    | No              |
| qw            | Feature | Real    | Hydrodynamic interaction factor          | -     | No              |

### Exploratory Data Analytics
**Descriptive Analytics**: Descriptive statistics were calculated to summarize the key characteristics of the total power output. This included measures of central tendency (mean, median) and dispersion (range, standard deviation). Visualizations such as histograms and density plots were used to illustrate the distribution of power outputs and other features.

**Diagnostics Analytics**: Diagnostic analytics involved analyzing relationships between features and total power output using scatter plots and correlation matrices. This helped to identify significant predictors and understand their impact on power output. Insights were drawn to refine feature selection and improve model accuracy.

### Data Cleaning/Pre-Treatment for Machine Learning
Before applying machine learning models, the data was cleaned and pre-processed. This included:
- **Handling Missing Values**: Replacing missing values with the mean for continuous variables or mode for categorical variables.
- **Normalization**: Scaling numerical features to ensure consistent range and improve model performance.
- **Feature Selection**: Identifying and selecting relevant features based on their significance and impact on the target variable.

### Predictive Data Analytics
**Machine Learning Models**: Various machine learning models were trained and evaluated, including linear regression and ensemble methods. The performance of each model was assessed using metrics such as Mean Squared Error (MSE), Mean Absolute Error (MAE), Root Mean Squared Error (RMSE), and R-squared (R²).

**Insights and Foresights**: The analysis revealed how well the models predicted power output and identified the most influential features. The findings provided actionable insights for optimizing wave farm configurations and improving power generation efficiency.

## Conclusion
The project successfully developed predictive models to estimate the total power output of large-scale wave energy farms. By analyzing the significance of features and evaluating model performance, we provided valuable insights into optimizing wave farm operations. The methodologies employed demonstrated the potential of machine learning to enhance decision-making in wave energy management, offering a practical approach to improving energy generation efficiency.

## References
- **Neshat, M., Alexander, B., Sergiienko, N., & Wagner, M.** (2023). Data on Wave Energy Converters and Power Output. [DOI: 10.24432/C5GG7Q](https://doi.org/10.24432/C5GG7Q)
- **Phoenix HPC Service**: University of Adelaide.
- **Creative Commons Attribution 4.0 International (CC BY 4.0) License**.

