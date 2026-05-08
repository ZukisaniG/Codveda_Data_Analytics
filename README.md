# Stock Prices Data Analytics Project

## Project Overview

This project is a data analytics project completed as part of the Codveda Data Analytics task list. The project demonstrates a full data analytics workflow using Python, Tableau, and machine learning techniques.

The project focuses mainly on stock prices data, which was used for data cleaning, exploratory data analysis, basic visualization, regression analysis, time-series analysis, and dashboard development. A separate sentiment dataset was also used for natural language processing and sentiment analysis.

The main goal of the project is to clean, analyse, visualise, model, and present data insights in a clear and practical way.

---

## Datasets Used

The project uses two datasets:

### 1. Stock Prices Dataset

File:

`2) Stock Prices Data Set.csv`

Cleaned version:

`cleaned_stock_prices.csv`

The stock prices dataset contains stock market information with the following fields:

- Symbol
- Date
- Open
- High
- Low
- Close
- Volume

The dataset contains 497,472 rows and 7 columns.

### 2. Sentiment Dataset

File:

`3) Sentiment dataset.csv`

The sentiment dataset contains textual data used for natural language processing and sentiment analysis.

---

## Tools and Technologies Used

- Python
- pandas
- matplotlib
- seaborn
- scikit-learn
- statsmodels
- nltk
- TextBlob
- WordCloud
- Tableau
- VS Code
- Jupyter Notebook
- GitHub

---

# Tasks Completed

## Level 1: Task 1 - Data Cleaning and Preprocessing

The raw stock prices dataset was loaded using pandas and inspected for missing values, duplicate rows, data types, and inconsistent formats.

Cleaning steps included:

- Loaded the dataset using pandas
- Checked the number of rows and columns
- Checked column names and data types
- Identified missing values
- Checked for duplicate rows
- Standardized column names
- Converted the `date` column to datetime format
- Sorted the data by `symbol` and `date`
- Filled missing values in price-related columns
- Standardized the `symbol` column
- Saved the cleaned dataset as `cleaned_stock_prices.csv`

Missing values found:

- `open`: 11 missing values
- `high`: 8 missing values
- `low`: 8 missing values

No duplicate rows were found.

---

## Level 1: Task 2 - Exploratory Data Analysis

Exploratory Data Analysis was performed on the cleaned stock prices dataset to understand patterns, trends, and relationships.

EDA steps included:

- Calculated summary statistics
- Calculated mean, median, mode, and standard deviation
- Created histograms to show data distributions
- Created boxplots to identify spread and possible outliers
- Created scatter plots to examine relationships between variables
- Calculated correlations between numerical features
- Created a correlation heatmap

Key findings:

- The stock price columns `open`, `high`, `low`, and `close` were strongly correlated.
- This strong relationship is expected because these fields all describe stock price movement during the same trading period.
- Trading volume behaved differently from the price variables and showed weaker relationships with stock prices.

---

## Level 1: Task 3 - Basic Data Visualization

Basic visualizations were created using matplotlib and seaborn.

Visualizations created:

- Bar chart showing top stocks by average trading volume
- Line chart showing average closing price over time
- Scatter plot showing the relationship between opening price and closing price
- Scatter plot showing the relationship between trading volume and closing price

The charts were customized with:

- Clear titles
- Axis labels
- Legends where needed
- Exported image files for reporting

Output images include:

- `top_10_stocks_by_volume.png`
- `average_closing_price_over_time.png`
- `open_vs_close_scatter.png`
- `volume_vs_close_scatter.png`

---

## Level 2: Task 1 - Regression Analysis

A simple linear regression model was built using scikit-learn.

The goal was to predict the closing stock price using the opening stock price.

Model setup:

- Independent variable: `open`
- Dependent variable: `close`
- Model used: Linear Regression
- Training and testing split: 80% training data and 20% testing data

Evaluation metrics used:

- Mean Squared Error
- R-squared score

Key finding:

The regression analysis showed a strong positive relationship between opening price and closing price. This means that stocks with higher opening prices generally also had higher closing prices.

Output image:

- `simple_linear_regression_open_vs_close.png`

---

## Level 2: Task 2 - Time Series Analysis

Time-series analysis was performed using the cleaned stock prices dataset.

The analysis focused on stock closing prices over time.

Steps completed:

- Converted the `date` column to datetime format
- Selected a stock symbol for analysis
- Plotted the original closing price over time
- Applied moving average smoothing
- Created 30-day and 90-day moving averages
- Resampled daily data into monthly average closing prices
- Decomposed the time series using statsmodels
- Separated the series into trend, seasonality, and residual components

Output images include:

- `closing_price_over_time.png`
- `moving_average_smoothing.png`
- `time_series_decomposition.png`
- `AAPL_closing_price_over_time.png`

Key finding:

Moving averages helped smooth short-term price fluctuations and made the overall trend easier to observe. Time-series decomposition helped separate the stock price movement into trend, seasonal, and residual components.

---

## Level 3: Task 2 - Building Dashboards with Tableau

An interactive dashboard was created using Tableau.

Dashboard title:

`Stock Prices Analysis Dashboard`

The dashboard includes:

- Line chart showing average closing price over time
- Scatter plot showing the relationship between average opening price and average closing price
- Bar chart showing average trading volume by stock symbol
- Symbol filter
- Date filter

The dashboard allows users to interactively explore:

- Stock price trends
- Trading volume comparisons
- Relationships between opening and closing prices
- Selected stocks and selected time periods

A Tableau Story was also created to explain the dashboard insights step by step.

Tableau workbook file:

`Stock_Prices_Analysis_Dashboard.twbx`

---

## Level 3: Task 3 - Natural Language Processing Sentiment Analysis

Sentiment analysis was performed on a textual dataset using Python, nltk, TextBlob, pandas, matplotlib, and WordCloud.

Steps completed:

- Loaded the sentiment dataset
- Inspected the dataset structure and missing values
- Selected the main text column for analysis
- Cleaned the text data
- Converted text to lowercase
- Removed URLs, mentions, hashtags, punctuation, numbers, and special characters
- Removed stopwords
- Applied lemmatization
- Used TextBlob to calculate sentiment polarity scores
- Classified text as Positive, Negative, or Neutral
- Visualized sentiment distribution
- Created a word cloud showing frequent words
- Saved the sentiment analysis results as a CSV file

Output files include:

- `sentiment_analysis_results.csv`
- `sentiment_distribution.png`
- `word_cloud.png`

Key finding:

The NLP analysis classified text entries into sentiment categories and showed the overall distribution of positive, negative, and neutral sentiment. The word cloud helped identify frequently used words in the cleaned text data.

---

# Project Files

The repository contains:

- `README.md`
- `2) Stock Prices Data Set.csv`
- `3) Sentiment dataset.csv`
- `cleaned_stock_prices.csv`
- `sentiment_analysis_results.csv`
- `Stock_Prices_Analysis_Dashboard.twbx`

Notebook files:

- `task_1_data_cleaning.ipynb`
- `task_2_exploratory_data_analysis.ipynb`
- `task_3_basic_data_visualisation.ipynb`
- `task_1_regression_analysis.ipynb`
- `task_2_time_series_analysis.ipynb`
- `task_3_nlp_sentiment_analysis.ipynb`

Visualization files:

- `average_closing_price_over_time.png`
- `top_10_stocks_by_volume.png`
- `open_vs_close_scatter.png`
- `volume_vs_close_scatter.png`
- `simple_linear_regression_open_vs_close.png`
- `closing_price_over_time.png`
- `moving_average_smoothing.png`
- `time_series_decomposition.png`
- `AAPL_closing_price_over_time.png`
- `sentiment_distribution.png`
- `word_cloud.png`

---

# How to Run the Project

## 1. Clone the Repository

```bash
https://github.com/ZukisaniG/Codveda_Data_Analytics.git
