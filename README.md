# Stock Prices Data Analytics Project

## Project Overview

This project is a data analytics project completed as part of the Codveda Data Analytics task list. The project uses a stock prices dataset to perform data cleaning, exploratory data analysis, basic data visualization, regression analysis, and interactive dashboard creation using Tableau.

The main goal of the project is to clean and analyze stock price data, identify trends and relationships, build a simple predictive model, and present insights through an interactive dashboard.

---

## Dataset

The dataset used in this project is:

`2) Stock Prices Data Set.csv`

After cleaning, the final dataset was saved as:

`cleaned_stock_prices.csv`

The dataset contains stock market information with the following fields:

- Symbol
- Date
- Open
- High
- Low
- Close
- Volume

The dataset contains 497,472 rows and 7 columns.

---

## Tools and Technologies Used

- Python
- pandas
- matplotlib
- seaborn
- scikit-learn
- Tableau
- VS Code
- Jupyter Notebook
- GitHub

---

## Project Tasks Completed

## Level 1: Task 1 - Data Cleaning and Preprocessing

The raw stock prices dataset was loaded using pandas. The dataset was inspected for missing values, duplicate rows, incorrect data types, and inconsistent formats.

Cleaning steps included:

- Loaded the CSV file using pandas
- Checked the shape, column names, and data types
- Identified missing values
- Found missing values in the `open`, `high`, and `low` columns
- Checked for duplicate rows
- Converted the `date` column into datetime format
- Standardized the `symbol` column
- Filled missing stock price values using logical methods
- Saved the cleaned dataset as `cleaned_stock_prices.csv`

Missing values found:

- `open`: 11 missing values
- `high`: 8 missing values
- `low`: 8 missing values

There were no duplicate rows in the dataset.

---

## Level 1: Task 2 - Exploratory Data Analysis

Exploratory Data Analysis was performed to understand the dataset and identify patterns, trends, and relationships.

EDA steps included:

- Calculated summary statistics
- Calculated mean, median, mode, and standard deviation
- Created histograms to understand data distributions
- Created boxplots to identify spread and possible outliers
- Created scatter plots to examine relationships between variables
- Calculated correlations between numerical features
- Created a correlation heatmap

The analysis showed that stock price variables such as `open`, `high`, `low`, and `close` are strongly correlated with each other. This is expected because they all represent price movements within the same trading period.

---

## Level 1: Task 3 - Basic Data Visualization

Basic visualizations were created using matplotlib and seaborn.

Visualizations created:

- Bar plot showing top stocks by average trading volume
- Line chart showing average closing price over time
- Scatter plot showing the relationship between opening price and closing price
- Scatter plot showing the relationship between volume and closing price

The charts were customized with clear titles, axis labels, and legends. The visualizations were also exported as image files for reporting purposes.

---

## Level 2: Task 1 - Regression Analysis

A simple linear regression model was built using scikit-learn.

The goal was to predict the closing stock price using the opening stock price.

Model setup:

- Independent variable: `open`
- Dependent variable: `close`
- Train-test split: 80% training data and 20% testing data
- Model used: Linear Regression

The model was evaluated using:

- Mean Squared Error
- R-squared score

The regression analysis showed a strong positive relationship between opening price and closing price. This means that stocks with higher opening prices generally also have higher closing prices.

---

## Tableau Dashboard

An interactive dashboard was created using Tableau.

Dashboard title:

`Stock Prices Analysis Dashboard`

The dashboard includes:

- Line chart: Average Closing Price Over Time
- Scatter plot: Open Price vs Close Price
- Bar chart: Average Volume by Stock Symbol
- Symbol filter
- Date filter

The dashboard allows users to interactively explore stock price trends, compare trading volume, and examine the relationship between opening and closing prices.

---

## Tableau Story

A Tableau Story was also created to explain the dashboard insights step by step.

Story title:

`Stock Prices Analysis Story`

The story explains:

- Overall dashboard purpose
- Closing price trends over time
- Relationship between opening and closing prices
- Trading volume comparison by stock symbol

---

## Key Insights

The main insights from the project are:

- The dataset had missing values in the `open`, `high`, and `low` columns.
- No duplicate rows were found.
- Stock price variables are strongly related to each other.
- Opening price and closing price have a strong positive relationship.
- Some stocks have much higher average trading volume than others.
- Tableau filters make it easier to explore selected stocks and time periods.

---

## Project Files

The repository contains:

- `task_1_data_cleaning.ipynb`
- `task_2_eda.ipynb`
- `task_3_visualization.ipynb`
- `level_2_regression_analysis.ipynb`
- `cleaned_stock_prices.csv`
- `visualizations/`
- `Stock_Prices_Analysis_Dashboard.twbx`
- `README.md`

---

## How to Run the Python Files

1. Clone this repository:

```bash
git clone https://github.com/your-username/stock-prices-data-analytics.git
