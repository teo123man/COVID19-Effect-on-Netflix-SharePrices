# Netflix Stock Price Prediction using Stringency Index

This project explores the impact of the COVID-19 pandemic, specifically the government-imposed **Stringency Index**, on **Netflix stock prices**. It employs two machine learning models — **K-Nearest Neighbours (KNN)** and **Random Forest Regression** — to predict stock price changes based on the Stringency Index.

---

## Table of Contents

- [Project Description](#project-description)
- [Data Sources](#data-sources)
- [Preprocessing](#preprocessing)
- [Exploratory Data Analysis (EDA)](#exploratory-data-analysis-eda)
- [Machine Learning Models](#machine-learning-models)
- [Results](#results)
- [How to Run](#how-to-run)
- [Conclusion](#conclusion)

---

## Project Description

The study demonstrates how government policies (as measured by the Stringency Index) influenced Netflix stock prices during the COVID-19 pandemic. By analyzing this relationship using advanced machine learning techniques, we aim to uncover trends and assess model effectiveness.

---

## Data Sources

Two datasets are utilized:

1. **`owid-covid-data.csv`**: Contains daily data on the Stringency Index for various countries.
2. **`Stock Market Dataset.csv`**: Includes historical stock prices for several US companies, including Netflix.

---

## Preprocessing

Key preprocessing steps include:
- **Data Cleaning**: Handled missing values and standardized data types.
- **Data Filtering**: Extracted US-specific data from the Stringency Index dataset.
- **Normalization**: Applied MinMaxScaler to normalize values to a 0–1 range for improved performance.

---

## Exploratory Data Analysis (EDA)

Performed detailed analyses to uncover patterns:
- **Descriptive Statistics**: Summarized the Stringency Index.
- **Histograms**: Visualized the distribution of the Stringency Index.
- **Scatter Plots**: Analyzed the relationship between Stringency Index and Netflix stock prices.
- **Correlation Analysis**: Confirmed a statistically significant positive correlation using Pearson's correlation coefficient.

---

## Machine Learning Models

### 1. K-Nearest Neighbours (KNN) Regression
- Predicts stock prices based on the average of nearest neighbors.
- Hyperparameter tuning (`k` value) was done using cross-validation.
- Evaluated using **Root Mean Squared Error (RMSE)**.

### 2. Random Forest Regression
- Constructs multiple decision trees and averages predictions.
- Hyperparameters like tree depth and number of trees were fine-tuned using **GridSearchCV**.
- More robust against overfitting compared to KNN.

---

## Results

| Model                 | RMSE           |
|-----------------------|----------------|
| KNN Regression        | 0.0571         |
| Random Forest         | 0.0425         |

- **Random Forest** consistently outperformed KNN, suggesting a non-linear relationship between the Stringency Index and stock prices.
- Feature importance analysis revealed that the Stringency Index was the sole predictor for Random Forest.

---

## How to Run

1. Clone this repository:
   ```bash
   git clone https://github.com/your-username/Netflix-Stock-Prediction.git
   ```
2. Navigate to the project directory:
   ```bash
   cd Netflix-Stock-Prediction
   ```
3. Run the Jupyter Notebook:
   ```bash
   jupyter notebook CS210-Project.ipynb
   ```
