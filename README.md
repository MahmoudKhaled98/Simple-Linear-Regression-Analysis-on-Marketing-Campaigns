# Simple Linear Regression Analysis on Marketing Campaigns

## Project Overview

In this project, I will use **simple linear regression** to explore the relationship between two continuous variables, specifically focusing on the impact of marketing promotional budgets on sales. The analysis will involve creating and fitting a model, checking model assumptions, analyzing performance, interpreting coefficients, and communicating the results to stakeholders. This project is especially relevant for decision-making in influencer marketing, where understanding the correlation between promotional spending and revenue generation is crucial.

The dataset contains information about marketing campaigns across various platforms, including **TV, radio, and social media**, along with the corresponding revenue generated. Insights from this analysis will guide company leaders in optimizing future marketing strategies.

## Table of Contents

- [Introduction](#introduction)
- [Step 1: Imports](#step-1-imports)
- [Step 2: Data Exploration](#step-2-data-exploration)
- [Step 3: Model Building](#step-3-model-building)
- [Step 4: Results and Evaluation](#step-4-results-and-evaluation)
- [Conclusion](#conclusion)
- [How to Run](#how-to-run)
- [References](#references)

## Introduction

In this project, I will explore the relationship between marketing promotional budgets and sales through simple linear regression analysis. Understanding this relationship is crucial for company leaders as they determine where to allocate future marketing resources effectively.

## Step 1: Imports

### Import packages
- Import the necessary libraries for data manipulation, visualization, and modeling.

### Load the dataset
- Load the marketing dataset that contains information on promotional spending and corresponding sales.

## Step 2: Data Exploration

### Familiarizing with the Data's Features

Starting with an exploratory data analysis (EDA) to understand and prepare the data for modeling. The features in the dataset include:
- TV promotion budget (in millions of dollars)
- Social media promotion budget (in millions of dollars)
- Radio promotion budget (in millions of dollars)
- Sales (in millions of dollars)

Each row represents a distinct marketing promotion. The goal is to identify which feature most strongly predicts sales to inform future investments in marketing.

### Reasons for Conducting EDA

- Understand which variables are present in the data.
- Analyze the distribution of features (min, mean, max values).
- Visualize relationships between the dependent and independent variables to identify the best predictors for sales.
- Identify any data quality issues, including missing values.

### Exploring the Data Size
- Review the overall structure and size of the dataset.

### Exploring the Independent Variables
- Use descriptive statistics to examine the three continuous independent variables: `TV`, `Radio`, and `Social_Media`.

### Exploring the Dependent Variable
- Check for missing values in the `Sales` column to ensure data quality.

- The preceding output shows that 0.13% of rows are missing the Sales value.

### Removing Missing Data
- Implement strategies to handle missing values.

### Visualizing the Sales Distribution
- Create a histogram to visualize the distribution of sales, noting that it is evenly distributed between 25 and 350 million.

## Step 3: Model Building

- Create a pairplot to visualize relationships between variable pairs, helping select the best independent variable for regression.

- Based on analysis, TV promotions are chosen as the independent variable `X`, given its stronger linear relationship with sales compared to other variables.

### Build and Fit the Model
- Construct the simple linear regression model using `TV` as the independent variable.

### Checking Model Assumptions
- Verify that the following assumptions for linear regression are met:
  - Linearity
  - Independence of observations
  - Normality of residuals
  - Homoscedasticity

## Step 4: Results and Evaluation

### Displaying the OLS Regression Results
- Review the OLS regression output, particularly focusing on the R-squared value, which indicates how well the model explains sales variation.

### Interpreting the Model Results
- Analyze the slope coefficient, which indicates the impact of TV promotional budgets on sales. 

- The final model can be expressed as:  
  **Sales = -0.1263 + 3.561 * TV promotions**

### Measuring the Uncertainty of the Coefficient Estimates
- Assess the statistical significance of the model's coefficients and the confidence intervals.

## Conclusion

### Key Insights to Share

1. **Sales Distribution**: Sales are evenly distributed between **$25 million and $350 million** across all channels.
2. **Relationship Between Promotions and Sales**: 
   - **TV** shows the strongest positive linear relationship with sales.
   - **Radio** has a moderate relationship, while **Social Media** shows a weak correlation.
3. **Model Coefficients**: The TV coefficient suggests that an increase of one million dollars in TV spending results in an estimated increase of $3.5614 million in sales.
4. **Statistical Significance**: The strong p-value for the TV coefficient indicates its importance for driving sales.

### Recommendations to Leadership
- Prioritize increasing the TV promotional budget for maximizing sales, as it has the strongest predictive relationship with sales outcomes.

### Summary for Stakeholders
- TV advertising is the **most effective channel** for driving sales, explaining almost all the variability in sales outcomes.

- For every **1\$ million** increase in TV spending, sales are expected to rise by about **3.56\$ million**.


- We are **95% confident** that the true increase in sales per **1\$ million** spent on TV promotions falls within a **range of  3.558\$ to 3.565\$ million**.

- The model's results are statistically robust, with a high R-squared value and significant coefficients, making TV promotions a key focus for maximizing sales growth.

## How to Run

1. **Clone the repository**:

    ```bash
    git clone <https://github.com/MahmoudKhaled98/Simple-Linear-Regression-Analysis-on-Marketing-Campaigns.git>
    ```

2. **Install the required dependencies**:

    ```bash
    pip install -r requirements.txt
    ```

3. **Run the Jupyter notebook**:

    ```bash
    jupyter notebook
    ```

## References

- Saragih, H.S. (2020). [*Marketing and Sales Data*](https://www.kaggle.com/datasets/harrimansaragih/dummy-advertising-and-sales-data).

- [Pandas Documentation](https://pandas.pydata.org/)
- [Seaborn Documentation](https://seaborn.pydata.org/)
- [Matplotlib Documentation](https://matplotlib.org/stable/contents.html)
- [Statsmodels Documentation](https://www.statsmodels.org/stable/index.html)
