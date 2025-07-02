# 📊 Layoffs Data Analysis using SQL

## 📝 Project Overview

This project focuses on **data cleaning** and **exploratory data analysis (EDA)** using SQL on a dataset containing details of layoffs across companies, industries, and countries. The analysis aims to uncover insights into layoff trends, industry impact, funding stage correlations, and company-specific statistics.

---

## 🧹 Step 1: Data Cleaning

### ✔️ Actions Performed:

* **Removed duplicates** using `ROW_NUMBER()` and deleted redundant entries.
* **Trimmed white spaces** in textual fields like `company` and `country`.
* **Standardized values** (e.g., unified variations of "Crypto").
* **Converted date formats** from string to `DATE` type using `STR_TO_DATE()`.
* **Handled missing values:**

  * Replaced empty strings with `NULL`.
  * Imputed missing `industry` values using self-joins.
  * Identified completely null records for review.
* **Dropped unnecessary columns** (like temporary `row_num`).

> ✅ Cleaned dataset: `layoffs_staging2`

---

## 📈 Step 2: Exploratory Data Analysis (EDA)

### 🔍 General Insights

* **Max layoffs**: Retrieved max values for total and percentage layoffs.
* **Complete layoffs**: Identified companies with 100% workforce laid off.
* **Top affected companies/countries** by layoffs.
* **Trends over time**: Monthly and yearly breakdown of layoffs.

### 📊 Aggregated Group Analysis

* **By Country**: Total layoffs per country.
* **By Industry**: Unique industry count and distribution.
* **By Stage**: Layoffs based on funding stage and corresponding average funding.
* **By Year/Month**: Rolling total of layoffs computed monthly.

### 🏆 Rankings & Trends

* **Top 5 companies** per year based on total layoffs using `DENSE_RANK()`.
* **Companies with highest funds raised** and their total layoffs.
* **Companies with missing/null fields** analyzed in count summaries.

### 📉 Summary Statistics

* **Funds Raised**: Calculated min, max, and mean.
* **Layoff Timeline**: Earliest and latest layoffs in dataset.

### 📌 Key Queries Used

* Window functions: `ROW_NUMBER()`, `DENSE_RANK()`, `SUM() OVER (...)`
* Aggregations: `SUM()`, `AVG()`, `COUNT()`, `MIN()`, `MAX()`
* Temporal groupings: `YEAR(date)`, `SUBSTRING(date, 1, 7)`

---



## 🛠️ Tools Used

* **MySQL** – Data cleaning & SQL-based EDA


---

## 📌 Future Scope

* Visualization using Tableau or Matplotlib/Seaborn in Python
* Predictive modeling for future layoff trends
* Sentiment analysis on company news (external data integration)

---
