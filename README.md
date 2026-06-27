
#  Cafe Sales Data Cleaning Project

A complete data cleaning project performed on a dirty cafe sales dataset using **Python, Pandas, NumPy, Matplotlib, and Seaborn**.

The objective of this project is to identify and fix common data quality issues such as missing values, incorrect data types, duplicate records, inconsistent values, and outliers before preparing the dataset for analysis.

---

#  Table of Contents

- [Project Overview](#project-overview)
- [Dataset](#dataset)
- [Tools & Libraries Used](#tools--libraries-used)
- [Import Dataset & Quality Check](#import-dataset--quality-check)
- [Handling Missing Values](#handling-missing-values)
- [Checking Duplicate Records](#checking-duplicate-records)
- [Data Imputation](#data-imputation)
- [Standardization](#standardization)
- [Outlier Detection & Visualization](#outlier-detection--visualization)
- [Saving the Cleaned Dataset](#saving-the-cleaned-dataset)
- [Results](#results)

---

# Project Overview

Raw datasets often contain missing values, inconsistent formatting, invalid entries, and incorrect data types. Cleaning the data is one of the most important steps before performing any analysis or machine learning.

This project demonstrates a complete data cleaning workflow on a Cafe Sales dataset.

---

# Dataset

The dataset contains **10,000 cafe sales transactions** with the following columns:

| Column |
|----------|
| Transaction ID |
| Item |
| Quantity |
| Price Per Unit |
| Total Spent |
| Payment Method |
| Location |
| Transaction Date |

Common data quality issues include:

- Missing values
- Invalid entries (e.g., ERROR, UNKNOWN)
- Incorrect data types
- Outliers
- Inconsistent categorical values

---

# Tools & Libraries Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn

---

# Import Dataset & Quality Check

The dataset was imported into Pandas and inspected using:

- `head()`
- `info()`
- `describe()`
- `isnull().sum()`
- `value_counts()`

These checks helped identify:

- Missing values
- Incorrect data types
- Invalid entries
- Dataset dimensions

---

# Handling Missing Values

Invalid placeholders such as **ERROR** and **UNKNOWN** were converted into missing values (`NaN`).

Missing values were identified using:

```python
df.isnull().sum()
```

---

# Checking Duplicate Records

Duplicate rows were checked using:

```python
df.duplicated().sum()
```

No duplicate records were found in the dataset.

---

# Data Imputation

Different imputation techniques were applied depending on the data type.

| Column | Method Used |
|----------|-------------|
| Item | Mode |
| Quantity | Median |
| Price Per Unit | Median |
| Total Spent | Median |
| Payment Method | Mode |
| Location | Mode |

---

# Standardization

Categorical values were inspected for inconsistent formatting.

Examples include:

- Removing extra spaces
- Correcting capitalization
- Replacing invalid values

Date values were converted into proper datetime format using:

```python
pd.to_datetime()
```

---

# Outlier Detection & Visualization

Outliers were detected using the **Interquartile Range (IQR)** method.

The following numeric columns were checked:

- Quantity
- Price Per Unit
- Total Spent

Outliers were visualized using **Seaborn Boxplots**.

Example:

```python
sns.boxplot(y=df["Total Spent"])
```

---

# Saving the Cleaned Dataset

After cleaning, the dataset was exported as a CSV file.

```python
df.to_csv("cleaned_cafe_sales.csv", index=False)
```

---


# Results

1.  Removed invalid entries

2.  Handled missing values

3.  Verified duplicate records

4.  Corrected data types

5.  Standardized categorical data

6.  Detected and visualized outliers

7.  Exported a clean dataset ready for analysis

---

## ⭐ If you found this project useful, consider giving it a star!
