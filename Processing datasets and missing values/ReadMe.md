# **Experiment 12 – Data Wrangling Using Python**

---

## **Aim**

To perform data wrangling using Python and the Pandas library by cleaning, transforming, and preparing raw data into a structured and meaningful format suitable for analysis and decision-making.

---

## **Objectives**

* To understand the concept and importance of data wrangling in data analysis
* To identify and handle missing, inconsistent, and duplicate data effectively
* To clean and preprocess raw datasets using the Pandas library
* To transform and restructure data into a suitable format for analysis
* To perform operations such as renaming, filtering, sorting, and modifying data
* To merge and combine multiple datasets for comprehensive analysis
* To improve overall data quality and reliability before analysis

---

## **Introduction**

In real-world scenarios, data is rarely available in a clean and structured format. Most datasets contain missing values, duplicate entries, inconsistent formats, and errors that can negatively impact the results of data analysis. Data wrangling is the essential process of cleaning, organizing, and transforming such raw data into a usable form.

Data wrangling ensures that the dataset is accurate, consistent, and complete, thereby improving the quality of insights derived from it. Without proper data wrangling, analysis may lead to incorrect conclusions and poor decision-making.

Python, along with its powerful library Pandas, provides efficient tools and functions to perform data wrangling tasks. These include handling missing values, removing duplicates, transforming data types, and merging datasets. Data wrangling is a crucial step in fields such as data science, machine learning, business intelligence, and research, where clean data is the foundation for meaningful analysis.

---

## **Theory**

### **1. Data Wrangling**

Data wrangling refers to the process of cleaning, transforming, and organizing raw data into a structured format suitable for analysis. It involves multiple steps that ensure the dataset is free from errors and inconsistencies. This process is often time-consuming but is considered one of the most important stages in data analysis.

The main goal of data wrangling is to improve data quality so that accurate and reliable insights can be obtained. It includes tasks such as handling missing values, correcting data formats, removing duplicates, and combining data from different sources.

---

### **2. Handling Missing Values**

Missing values are common in real-world datasets and can occur due to various reasons such as data entry errors, system failures, or incomplete data collection. If not handled properly, missing data can distort analysis results.

Pandas provides several functions to detect and handle missing values. The `isnull()` function helps identify missing entries, while `dropna()` removes rows or columns containing missing values. The `fillna()` function replaces missing values with a specified value such as zero, mean, or median.

Handling missing values appropriately ensures that the dataset remains consistent and does not introduce bias in analysis.

---

### **3. Removing Duplicates**

Duplicate records can lead to incorrect interpretations and inflated results during analysis. These duplicates may occur due to repeated data entry or merging datasets without proper checks.

Pandas provides the `duplicated()` function to identify duplicate rows and the `drop_duplicates()` function to remove them. Removing duplicates ensures that each data entry is unique and contributes accurately to the analysis.

---

### **4. Data Transformation**

Data transformation involves converting data into a suitable format or structure that is easier to analyze. This may include changing data types, creating new columns, or applying mathematical operations to existing data.

For example, converting a column from string to integer type or calculating a new column such as total cost from quantity and price are common transformation tasks. These transformations enhance the usability of the dataset and allow deeper insights.

---

### **5. Renaming Columns**

In many datasets, column names may not be clear or descriptive. Renaming columns improves readability and makes the dataset easier to understand and analyze.

Pandas allows renaming of columns using the `rename()` function. This helps in maintaining consistency and clarity, especially when working with large datasets.

---

### **6. Filtering Data**

Filtering is the process of selecting specific rows from a dataset based on certain conditions. It allows analysts to focus only on relevant data for a particular analysis.

For example, filtering data based on a specific category or condition helps in isolating meaningful subsets of data. This makes analysis more efficient and targeted.

---

### **7. Sorting Data**

Sorting organizes data in a meaningful order, such as ascending or descending. It helps in identifying trends, patterns, and outliers in the dataset.

Pandas provides the `sort_values()` function to sort data based on one or more columns. Proper sorting improves data readability and simplifies analysis.

---

### **8. Merging and Joining Data**

In many cases, data is spread across multiple datasets. Merging and joining allow combining these datasets into a single dataset for comprehensive analysis.

Pandas provides functions like `merge()` to combine datasets based on a common column. This helps in integrating related information and performing more detailed analysis.

---

## **Algorithms**

### **Algorithm 1: Handling Missing Values**

1. Start
2. Import Pandas library
3. Load dataset into DataFrame
4. Check for missing values using `isnull()`
5. Analyze missing data pattern
6. Handle missing values using `dropna()` or `fillna()`
7. Display cleaned dataset
8. Stop

---

### **Algorithm 2: Removing Duplicates**

1. Start
2. Load dataset into DataFrame
3. Identify duplicate rows using `duplicated()`
4. Remove duplicates using `drop_duplicates()`
5. Verify dataset uniqueness
6. Display updated dataset
7. Stop

---

### **Algorithm 3: Data Transformation**

1. Start
2. Load dataset
3. Select relevant columns
4. Convert data types if required
5. Create new columns using operations
6. Apply transformations
7. Display updated dataset
8. Stop

---

### **Algorithm 4: Filtering and Sorting Data**

1. Start
2. Load dataset
3. Apply filtering conditions
4. Extract required subset of data
5. Sort data using `sort_values()`
6. Display results
7. Stop

---

## **Sample Code Snippets**

### **Loading Dataset**

```python
import pandas as pd

df = pd.read_csv("data.csv")
print(df)
```

---

### **Handling Missing Values**

```python
print(df.isnull())
df = df.fillna(0)
```

---

### **Removing Duplicates**

```python
df = df.drop_duplicates()
```

---

### **Data Transformation**

```python
df['Total'] = df['Quantity'] * df['Price']
```

---

### **Filtering Data**

```python
print(df[df['Category'] == 'Furniture'])
```

---

### **Sorting Data**

```python
print(df.sort_values(by='Price'))
```

---

### **Merging Data**

```python
df3 = pd.merge(df1, df2, on='ID')
```

---

## **Applications**

* Used in data preprocessing for machine learning models to improve accuracy
* Helps businesses clean and analyze large volumes of customer data
* Used in financial data analysis for accurate reporting and forecasting
* Assists researchers in preparing survey and experimental data
* Enables integration of multiple datasets for comprehensive analysis
* Improves decision-making by ensuring high-quality data

---

## **Advantages**

* Enhances data quality and reliability
* Reduces errors and inconsistencies in datasets
* Prepares data for further analysis and visualization
* Saves time during the data analysis process
* Supports integration with advanced analytics and machine learning tools
* Provides efficient handling of large datasets

---

## **Result**

Data wrangling was successfully performed using Python and the Pandas library. Various operations such as handling missing values, removing duplicate entries, transforming data, filtering, sorting, and merging datasets were carried out effectively. The dataset was cleaned and structured properly, making it suitable for accurate analysis and further processing.
