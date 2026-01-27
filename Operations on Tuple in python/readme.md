# Experiment 4 - Tuples in Python: Creation, Access, and Operations

## Aim

 To understand Python tuples and perform operations such as creation, indexing, slicing, and use of built-in functions.

## Objectives

- To understand the concept of tuples in Python
- To study characteristics and advantages of tuples
- To perform indexing and slicing on tuples
- To apply built-in tuple functions
- To understand immutability of tuples

## Theory

**1\. Introduction to Tuples**

A **tuple** is an ordered collection of elements in Python, similar to a list, but **immutable** in nature. Tuples are written using **parentheses ( )** and elements are separated by commas.

Example:

(10, 20, 30)

**2\. Characteristics of Tuples**

- Ordered
- Indexed
- Immutable (cannot be changed after creation)
- Allows duplicate values
- Can store heterogeneous data types

**3\. Why Tuples are Used**

- Faster than lists
- Data integrity (values cannot be modified)
- Used for fixed data such as coordinates, days of week, database records

**4\. Creating Tuples**

Tuples can be created:

- With parentheses
- Without parentheses (tuple packing)
- Using the tuple() constructor

Special cases:

- Single element tuple must have a trailing comma  
    (10,)

**5\. Indexing in Tuples**

Tuple elements are accessed using **index numbers**, starting from 0.

Both:

- **Positive indexing**
- **Negative indexing**

are supported.

**6\. Slicing in Tuples**

Slicing is used to extract a portion of a tuple.

**General Syntax:**

tuple_name\[start : end : step\]

### Meaning of each part

- **start** → index to begin slicing (included)
- **end** → index to stop slicing (excluded)
- **step** → gap between elements (optional)

**7\. Immutability of Tuples**

Once a tuple is created:

- Elements cannot be added
- Elements cannot be removed
- Elements cannot be updated

Any attempt to modify results in an error.

**8\. Built-in Functions for Tuples**

| **Function** | **Description** |
| --- | --- |
| len() | Number of elements |
| max() | Maximum value |
| min() | Minimum value |
| sum() | Sum of elements |
| count() | Count occurrences |
| index() | Find index of element |

**9\. Difference Between List and Tuple**

| **List** | **Tuple** |
| --- | --- |
| Mutable | Immutable |
| Uses \[ \] | Uses ( ) |
| Slower | Faster |
| Dynamic | Fixed |

## ****Conclusion****

Thus, Python tuples were studied and operations such as creation, ind
