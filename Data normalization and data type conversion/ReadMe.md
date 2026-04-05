# Experiment 14 — Data Normalization & Encoding of Categorical Variables in Python

---

## Aim

To understand and implement essential data preprocessing techniques using Python libraries such as Pandas and Scikit-learn. The experiment focuses on:

* Data Normalization techniques: Min-Max Scaling, Z-Score Standardization, and Decimal Scaling.
* Encoding categorical variables: Label Encoding, One-Hot Encoding, and Dummy Encoding.

---

## Introduction

In practical data science workflows, raw data is rarely in a usable format. Before applying machine learning algorithms, preprocessing is required to improve data quality and ensure compatibility.

Two major preprocessing tasks are:

### 1. Data Normalization

Numerical features in datasets often have different scales. For example, product prices may range in thousands while ratings remain within a small range. If not scaled properly, larger values dominate model behavior. Normalization adjusts feature values to a comparable scale without altering relationships.

### 2. Encoding Categorical Variables

Machine learning models require numerical input. Categorical attributes such as gender, department, or payment method must be converted into numeric representations using encoding techniques.

This experiment demonstrates these techniques using both manually created datasets and real-world datasets.

---

## Libraries Used

### Pandas

Used for data handling and manipulation. It provides DataFrames and functions for preprocessing tasks such as normalization and encoding.

### NumPy

Supports numerical operations like mean, standard deviation, and array computations used during normalization.

### Scikit-learn

Provides preprocessing utilities. The LabelEncoder class is used to convert categorical labels into numerical values.

---

## Preprocessing Techniques

### Part A: Data Normalization

#### Min-Max Scaling

Rescales values into the range [0, 1].

Formula:
(x - min) / (max - min)

Used when models require bounded inputs.

#### Z-Score Standardization

Transforms data to have mean 0 and standard deviation 1.

Formula:
(x - mean) / standard deviation

Useful for algorithms that assume normally distributed data.

#### Decimal Scaling

Divides values by a power of 10 to bring them into a smaller range.

Formula:
x / (10^k)

A quick and simple scaling approach.

#### Multi-Column Scaling

Applies normalization simultaneously to multiple columns using vectorized operations in Pandas.

---

### Part B: Encoding Categorical Variables

#### Label Encoding

Assigns a unique integer to each category.

Example:
Female → 0, Male → 1

Suitable for binary or ordinal data.

#### One-Hot Encoding

Creates separate binary columns for each category.

Example:
Payment_Method → Credit Card, PayPal → two separate columns

Best for nominal data with no ordering.

#### Dummy Encoding

Similar to One-Hot Encoding but removes one column to prevent redundancy.

Used in regression models to avoid multicollinearity.

---

## Theory Overview

### Min-Max Scaling

Transforms values proportionally within a fixed range. The smallest value becomes 0 and the largest becomes 1.

### Z-Score Standardization

Centers data around zero and scales based on spread, making it easier to compare distributions.

### Decimal Scaling

Reduces magnitude by dividing by powers of 10, based on the maximum value.

### Label Encoding

Converts text categories into numeric form but may introduce unintended ordering.

### One-Hot Encoding

Eliminates ordering issues by creating independent binary features.

### Dummy Encoding

Reduces feature redundancy while preserving information.

---

## Key Functions Used

* `pd.DataFrame()` – Create DataFrame
* `pd.read_csv()` – Load CSV files
* `df.min(), df.max(), df.mean(), df.std()` – Statistical calculations
* `pd.get_dummies()` – One-Hot/Dummy encoding
* `LabelEncoder()` – Encode categorical labels
* `fit_transform()` – Fit and apply transformation

---

## Algorithm / Procedure

### Part A: Normalization

1. Import required libraries.
2. Create dataset using a dictionary.
3. Apply Min-Max scaling to selected columns.
4. Perform Z-Score normalization.
5. Apply Decimal Scaling.
6. Normalize multiple columns simultaneously.
7. Load external dataset and repeat steps.
8. Verify outputs.

### Part B: Encoding

1. Create categorical dataset.
2. Apply Label Encoding to binary columns.
3. Perform One-Hot Encoding on nominal columns.
4. Apply Dummy Encoding with drop_first=True.
5. Load student dataset and repeat encoding.
6. Validate transformed outputs.

---

## Dataset Description

### Product Dataset

* Columns: Product, Price, Units_Sold, Discount
* Rows: 6
* Source: Manually created

### Amazon Dataset

* Columns: Product_ID, Product_Name, Price, Rating, Reviews, Units_Sold
* Rows: 50
* Source: CSV file

### Orders Dataset

* Columns: Order ID, Customer_Gender, Payment_Method, Category, City, Order_Value
* Rows: 6

### Student Dataset

* Columns: Roll_No, Gender, Department, CGPA, Backlogs, Attendance, Placement_Status, Salary
* Rows: 10

---

## Applications

* E-commerce recommendation systems
* Banking risk analysis
* Healthcare predictions
* Placement analytics
* Natural language processing
* Computer vision models

---

## Conclusion

This experiment demonstrated how normalization and encoding prepare data for machine learning models.

Normalization ensures that numerical features contribute equally, while encoding converts categorical values into machine-readable formats.

Choosing the correct method depends on:

* Data type (numerical or categorical)
* Nature of categories (ordinal or nominal)
* Model requirements

These preprocessing steps are essential for building accurate and efficient models.

---

## Additional Notes

### Label vs One-Hot Encoding

Label encoding should be used only for ordinal or binary data. One-Hot encoding is preferred for nominal variables.

### Dummy Variable Trap

Using all One-Hot columns can lead to redundancy. Dropping one column avoids this issue.

### fit vs transform

* fit(): Learns parameters
* transform(): Applies transformation
* fit_transform(): Combines both

### Normalization Guidelines

| Scenario             | Technique       |
| -------------------- | --------------- |
| Fixed range required | Min-Max         |
| Normal distribution  | Z-Score         |
| Quick scaling        | Decimal Scaling |
| Tree-based models    | Not necessary   |

---
