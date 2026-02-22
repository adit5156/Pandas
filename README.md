# 🐼 Pandas – Data Analysis & Manipulation for Data Analytics

<p align="center">
  <b>Mastering Structured Data Processing for Analytics & Machine Learning</b>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Python-3.x-blue?logo=python">
  <img src="https://img.shields.io/badge/Library-Pandas-purple">
  <img src="https://img.shields.io/badge/Level-Beginner%20to%20Intermediate-green">
  <img src="https://img.shields.io/badge/Status-Completed-success">
  <img src="https://img.shields.io/badge/License-Educational-lightgrey">
</p>

---

# 📌 Introduction

**Pandas** is a powerful open-source Python library used for **data analysis, data manipulation, and data cleaning**.

It is built on top of NumPy and is one of the most important tools in the Data Analytics ecosystem.

Pandas allows you to:

- Work with structured datasets (tables)
- Clean and transform raw data
- Perform aggregation and statistical analysis
- Prepare data for Machine Learning models

---

# 🚀 Why Pandas is Important in Data Analytics

In real-world analytics:

- Data is messy
- Data comes in CSV, Excel, JSON formats
- Missing values exist
- Data needs transformation before modeling

Pandas provides efficient tools to:

- Load data
- Inspect data
- Clean data
- Transform data
- Analyze data

It is the backbone of most Data Analyst workflows.

---

# ⚙️ Installation

### 🔹 Install using pip

```bash
pip install pandas
```

### 🔹 Install using conda

```bash
conda install pandas
```

### 🔹 Verify Installation

```python
import pandas as pd
print(pd.__version__)
```

---

# 📦 Importing Pandas

```python
import pandas as pd
```

---

# 📊 Core Data Structures in Pandas

## 1️⃣ Series (1D Data)

A **Series** is a one-dimensional labeled array.

```python
import pandas as pd

data = [10, 20, 30, 40]
series = pd.Series(data)

print(series)
```

### Series with Custom Index

```python
series = pd.Series(data, index=["a", "b", "c", "d"])
print(series)
```

---

## 2️⃣ DataFrame (2D Data)

A **DataFrame** is a two-dimensional table with rows and columns.

```python
data = {
    "Name": ["Aditya", "Rahul", "Sneha"],
    "Age": [22, 23, 21],
    "City": ["Asansol", "Delhi", "Mumbai"]
}

df = pd.DataFrame(data)
print(df)
```

---

# 🔍 Exploring Data

```python
df.head()        # First 5 rows
df.tail()        # Last 5 rows
df.info()        # Data summary
df.describe()    # Statistical summary
df.shape         # (rows, columns)
df.columns       # Column names
df.dtypes        # Data types
```

---

# 🎯 Selecting & Filtering Data

## Selecting Columns

```python
df["Name"]
df[["Name", "Age"]]
```

## Selecting Rows

```python
df.loc[0]        # By label
df.iloc[0]       # By index position
```

## Conditional Filtering

```python
df[df["Age"] > 21]
```

---

# 🛠️ Data Cleaning

## Handling Missing Values

```python
df.isnull()
df.isnull().sum()
df.dropna()
df.fillna(0)
```

## Renaming Columns

```python
df.rename(columns={"Age": "User_Age"})
```

## Changing Data Types

```python
df["Age"] = df["Age"].astype(int)
```

---

# 🔄 Data Manipulation

## Adding a New Column

```python
df["Salary"] = [30000, 40000, 35000]
```

## Dropping Columns

```python
df.drop("Salary", axis=1)
```

## Sorting Values

```python
df.sort_values("Age")
```

---

# 📈 Grouping & Aggregation

```python
df.groupby("City")["Age"].mean()
```

Common Aggregation Functions:

- `mean()`
- `sum()`
- `count()`
- `min()`
- `max()`

---

# 🔗 Merging & Joining Data

```python
pd.merge(df1, df2, on="ID", how="inner")
pd.merge(df1, df2, on="ID", how="left")
pd.merge(df1, df2, on="ID", how="right")
pd.merge(df1, df2, on="ID", how="outer")
```

---

# 📂 Reading & Writing Files

## Read CSV

```python
df = pd.read_csv("data.csv")
```

## Read Excel

```python
df = pd.read_excel("data.xlsx")
```

## Save to CSV

```python
df.to_csv("output.csv", index=False)
```

---

# 🧠 Core Concepts Covered

- Series & DataFrame creation
- Data inspection & summary
- Indexing (`loc`, `iloc`)
- Filtering & conditional selection
- Missing value handling
- Data transformation
- GroupBy & aggregation
- Merging & joining datasets
- Reading and exporting files

---

# 🎯 Learning Outcomes

After completing this module, you will be able to:

- Load and inspect real-world datasets
- Clean messy data
- Perform exploratory data analysis (EDA)
- Transform data efficiently
- Prepare datasets for Machine Learning
- Use Pandas in end-to-end analytics workflows

---

# 📂 Repository Structure

```
03_Pandas.ipynb
README.md
```

---

# 📈 Future Enhancements (Roadmap)

- [ ] Advanced GroupBy operations
- [ ] Pivot tables
- [ ] Multi-indexing
- [ ] Time-series analysis
- [ ] Window functions
- [ ] Real-world dataset mini project

---

# 🧑‍💻 Who This Repository Is For

- Aspiring Data Analysts
- Data Science beginners
- Python learners
- Students preparing for analytics roles
- Anyone building a structured Pandas foundation

---

# 🤝 Connect & Collaboration

This repository is part of my structured journey toward becoming a **Data Analyst**.

I am documenting foundational modules including:

- Python
- NumPy
- Pandas
- Data Visualization
- Exploratory Data Analysis

Feedback and collaboration are always welcome.

---

# 📄 License

This project is created for educational and portfolio purposes.
