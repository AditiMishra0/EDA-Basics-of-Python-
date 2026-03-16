# Experiment 10 – Creating and Loading Dataset using Pandas


## Aim

To understand the process of creating datasets manually and loading external datasets using the Pandas library in Python for data analysis.


## Objectives

* To understand the concept of datasets in data analysis
* To create datasets using Python data structures
* To convert structured data into Pandas DataFrame
* To save datasets into CSV format
* To load datasets from CSV and Excel files
* To inspect and analyze datasets using Pandas functions
* To perform basic data manipulation operations

## Introduction

A dataset is a structured collection of data that can be analyzed and processed using computational tools. In real-world data analysis, datasets are either:

1. Created manually for testing and experimentation
2. Loaded from external sources such as CSV files, Excel files, or databases

The Pandas library provides efficient tools for dataset creation, storage, loading, and manipulation. It is widely used in data science, machine learning, business analytics, and research.

Pandas simplifies working with structured data using its primary data structure:

* **DataFrame** – A two-dimensional labeled table with rows and columns


## Theory

### 1. Creating a Dataset

Datasets can be created using:

* Python dictionaries
* Lists of values
* NumPy arrays

These structures can be converted into a DataFrame using:

```python
pd.DataFrame(data)
```

Creating datasets manually is useful for learning, testing algorithms, and performing small experiments.

---

### 2. Saving a Dataset

Once created, datasets can be stored permanently using:

* `to_csv()` – Save as CSV file
* `to_excel()` – Save as Excel file

Example:

```python
df.to_csv("file_name.csv", index=False)
```

Saving datasets allows future reuse and sharing.

---

### 3. Loading a Dataset

Datasets stored in files can be loaded using:

* `pd.read_csv()` – Load CSV file
* `pd.read_excel()` – Load Excel file
* `pd.read_json()` – Load JSON file

Example:

```python
df = pd.read_csv("file_name.csv")
```

Loading datasets is an essential step in real-world data analysis projects.

---

### 4. Dataset Inspection

After loading a dataset, it is important to inspect its structure using:

* `df.head()` – View first few rows
* `df.tail()` – View last few rows
* `df.shape` – Number of rows and columns
* `df.size` – Total number of elements
* `df.columns` – Column names
* `df.dtypes` – Data types
* `df.info()` – Summary of dataset
* `df.describe()` – Statistical summary

---

### 5. Data Manipulation

Common dataset operations include:

* Selecting specific columns
* Accessing rows using `loc[]` and `iloc[]`
* Filtering data using conditions
* Adding new columns
* Deleting existing columns
* Performing statistical operations

These operations help transform raw data into meaningful information.

---

## Algorithms

### Algorithm 1: Creating a Dataset

1. Start
2. Import Pandas library
3. Create structured data using dictionary or lists
4. Convert data into DataFrame
5. Display dataset
6. Stop

---

### Algorithm 2: Saving Dataset

1. Start
2. Create or load DataFrame
3. Use `to_csv()` or `to_excel()` function
4. Specify file name
5. Save file
6. Stop

---

### Algorithm 3: Loading Dataset

1. Start
2. Import Pandas library
3. Use appropriate `read_` function
4. Provide file path
5. Store dataset in DataFrame
6. Display dataset
7. Stop

---

### Algorithm 4: Inspecting Dataset

1. Start
2. Load dataset
3. Check shape and size
4. Display column names and data types
5. Generate statistical summary
6. Stop

---

## Sample Code Snippets

### Creating a Dataset

```python
import pandas as pd

data = {
    "Name": ["A", "B", "C"],
    "Age": [18, 19, 20]
}

df = pd.DataFrame(data)
print(df)
```

---

### Saving Dataset

```python
df.to_csv("data.csv", index=False)
```

---

### Loading Dataset

```python
df = pd.read_csv("data.csv")
print(df.head())
```

---

### Inspecting Dataset

```python
print(df.shape)
print(df.info())
print(df.describe())
```

---

## Applications

* Data preprocessing for machine learning
* Academic data analysis
* Business reporting
* Financial analysis
* Research data processing
* Survey data management

---

## Advantages

* Simple and efficient dataset creation
* Supports multiple file formats
* Easy data inspection and manipulation
* Efficient handling of large datasets
* Integration with visualization and machine learning libraries

---

## Result

Datasets were successfully created and loaded using the Pandas library. Various inspection and manipulation techniques were applied to analyze and understand the dataset structure.

---

## Conclusion

Creating and loading datasets is a fundamental step in data analysis. The Pandas library provides powerful and flexible tools to manage structured data efficiently. This experiment provided practical understanding of dataset creation, storage, loading, and analysis using Python.
