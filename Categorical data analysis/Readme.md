# Experiment 11 – Categorical Data Analysis Using Python

## Aim

To analyze categorical data using Python and the Pandas library by performing operations such as frequency counting, cross-tabulation, grouping, filtering, and percentage distribution.

---

## Objectives

* To understand the concept of categorical data
* To create and analyze categorical datasets using Pandas
* To compute frequency counts of categorical variables
* To identify unique values and the number of unique categories
* To perform cross-tabulation between categorical variables
* To calculate percentage distributions
* To filter and group categorical data for analysis

---

## Introduction

Categorical data refers to data that represents categories or groups rather than numerical values. Examples include gender, department, product category, payment mode, and delivery type.

In data analysis, categorical variables are commonly used to understand patterns, relationships, and distributions within datasets. Python provides powerful libraries such as **Pandas** that allow efficient analysis of categorical data.

Using Pandas, analysts can easily perform operations such as counting category frequencies, identifying unique values, creating cross-tabulations, and grouping data based on categories.

These techniques are widely used in business analytics, customer behavior analysis, academic research, and survey analysis.

---

## Theory

### 1. Categorical Data

Categorical data represents qualitative values that fall into specific categories. Unlike numerical data, categorical data describes attributes or labels.

Examples include:

* Product category
* Payment method
* Delivery type
* Customer type
* Department
* Gender

Categorical data helps in identifying patterns and relationships between different groups.

---

### 2. Frequency Count

Frequency count determines how many times each category appears in a dataset.

In Pandas, frequency counts can be calculated using:

```python
df['column_name'].value_counts()
```

This helps in understanding the distribution of categories within the dataset.

---

### 3. Unique Values

Unique values represent the distinct categories present in a dataset.

Pandas provides:

* `unique()` – Displays all unique values
* `nunique()` – Returns the number of unique values

Example:

```python
df['Category'].unique()
df['Category'].nunique()
```

---

### 4. Cross Tabulation

Cross-tabulation (contingency table) is used to analyze the relationship between two categorical variables.

It is implemented in Pandas using:

```python
pd.crosstab(column1, column2)
```

This helps in understanding how categories interact with each other.

Example:

* Category vs Payment Mode
* Gender vs Department

---

### 5. Percentage Distribution

Percentage distribution helps understand the proportion of each category in the dataset.

Example:

```python
df['Category'].value_counts(normalize=True) * 100
```

This converts frequency counts into percentages.

---

### 6. Filtering Data

Filtering allows extraction of rows that satisfy certain conditions.

Example:

```python
df[df['Category'] == 'Furniture']
```

This retrieves only rows belonging to the specified category.

---

### 7. Grouping Data

Grouping organizes data based on one or more categorical variables to perform analysis.

In Pandas, grouping is done using:

```python
df.groupby('Category')['Payment_Mode'].value_counts()
```

Grouping helps identify patterns within categories.

---

### 8. Sorting Data

Sorting arranges data in a specified order.

Example:

```python
df.sort_values(by='Category')
```

This organizes the dataset alphabetically by category.

---

## Algorithms

### Algorithm 1: Frequency Analysis

1. Start
2. Import Pandas library
3. Create or load dataset
4. Select categorical column
5. Use `value_counts()` to compute frequency
6. Display results
7. Stop

---

### Algorithm 2: Finding Unique Categories

1. Start
2. Load dataset using Pandas
3. Select categorical column
4. Use `unique()` to display distinct categories
5. Use `nunique()` to count unique categories
6. Display results
7. Stop

---

### Algorithm 3: Cross Tabulation

1. Start
2. Import Pandas library
3. Load dataset
4. Select two categorical variables
5. Use `pd.crosstab()` to create cross table
6. Display results
7. Stop

---

### Algorithm 4: Filtering and Grouping Data

1. Start
2. Load dataset into DataFrame
3. Apply filtering condition using logical expressions
4. Group dataset using `groupby()`
5. Perform required analysis
6. Display results
7. Stop

---

## Sample Code Snippets

### Creating Dataset

```python
import pandas as pd

data = {
    'Order_ID':['01','02','03'],
    'Category':['Furniture','Office Supplies','Technology'],
    'Payment_Mode':['COD','UPI','COD']
}

df = pd.DataFrame(data)
print(df)
```

---

### Frequency Count

```python
print(df['Category'].value_counts())
```

---

### Unique Values

```python
print(df['Category'].unique())
print(df['Category'].nunique())
```

---

### Cross Tabulation

```python
print(pd.crosstab(df['Category'], df['Payment_Mode']))
```

---

### Filtering Data

```python
print(df[df['Category'] == 'Furniture'])
```

---

### Grouping Data

```python
print(df.groupby('Category')['Payment_Mode'].value_counts())
```

---

## Applications

* Customer purchase behavior analysis
* Market basket analysis
* Academic performance analysis
* Survey data interpretation
* Business decision making
* Demographic data analysis

---

## Advantages

* Easy analysis of categorical variables
* Helps identify patterns and relationships between categories
* Efficient data grouping and summarization
* Supports percentage and frequency analysis
* Integrates easily with data visualization tools

---

## Result

Categorical data was successfully analyzed using Python and the Pandas library. Various operations such as frequency counting, unique value identification, cross-tabulation, filtering, grouping, and percentage distribution were performed to understand patterns and relationships within the dataset.
