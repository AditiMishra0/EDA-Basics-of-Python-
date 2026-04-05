# Experiment 14 - Data Normalization and Data Type Conversion

Data Normalization is the process of organizing data to reduce redundancy and improve integrity, typically by scaling numeric values to a standard range or structuring a database into tables.

Data Type Conversion is the process of changing a data value from one format to another, such as turning the string "10" into the integer 10 so that mathematical operations can be performed on it.

### Aim:

To implement Data Normalization and Data type Conversion in external Dataset

### Tools used:

Google Colab or Jupyter Notebook

### Theory:

#### Data Normalization:

Data normalization is a critical process used to keep data organized, efficient, and readable. It is used to convert the data into a uniform range and makes it easier to compare with other features. Normalization is the process of structuring a relational database to reduce data redundancy and improve data integrity.

#### Types of Data Normalization:

1. Min - Max Normalization:

   * It is the most straightforward method.
     
   * It squashes all the data into 0 or 1.
     
   * But, it is not useful when your data has outliers
     
   * If you have one massive value (an outlier), it will squash all the "normal" data points into a tiny, indistinguishable range near 0.
  
   * Formula:

             x' = x - min (x) / max (x) - min (x)

2. Z Score Normalization:

   * Z-Score normalization transforms data so that it has a mean ($\mu$) of 0 and a standard deviation ($\sigma$) of 1.
     
   * It centers the data around zero. Positive scores are above the mean; negative scores are below it.
     
   * It can handle Outliers much better than Min - Max method because it doesn't have a predefined range
  
   * Formula:

           z = x - mean / standard deviation

3. Decimal Scaling Normalization:

   * Decimal scaling normalizes by moving the decimal point of values.
   * The number of places the decimal moves depends on the maximum value of that particular feature (or) attribute
  
   * Formula:

           x' = x / {10^j}


#### Data Type Conversion:

Data Type Conversion is the process of transforming data from one type into a more appropriate type for computation. It is mostly used to convert Categorical Data into Quantitative Data

#### Scikit - Learn Library:

* Scikit-learn is the most popular Python library for "traditional" machine learning. It provides simple and efficient tools for predictive data analysis, built on top of NumPy, SciPy, and matplotlib.

* Scikit-learn is used for Mathematical Conversion. Machine learning models usually cannot process text (like "Red", "Blue", "Green"); Scikit-learn converts these labels into numbers that a computer can understand

#### Modules for conversion Scikit - Learn

Module used for data type conversion if **sklearn.preprocessing**

Following are the commands used for Data type conversion in Data Analysis using Scikit learn:

1. Label Encoder:

   * It converts the data present in a column either to 0 or 1
     
   * It is best suitable for attributes which have only 2 values present
     
   * The numbering 0 or 1 is done based on alphabetical order
  
**Syntax for importing and defining**

          from sklearn.preprocessing import LabelEncoder
          le = LabelEncoder()
  
2. One Hot Encoding:

   * This is the process of creating ew columns for each value present in a column.
     
   * if a column is created for the value **Red** then only the rows with value red will have the value **True** all others will have **False**
  
   * This can be done for single or multiple columns at a time
  
**Syntax for usage:**

          df_encoded = pd.get_dummies(df, columns=['Payment_Method'])
  
3. Dummy Encoding:

   * It is a Special type of One hot encoding, where the columns are divided as per the value present in a column but one value is dropped
     
   * By default it is the value with index 0 which is dropped
  
**Syntax for Usage:**

          df_dummy = pd.get_dummies(df, columns = ['Payment_Method'], drop_first = True)

### Learning Outcomes:

* Since python cannot process Categorical Data fastly, it is usually converted into quantitative data, and that data is normailzed using the process called **Data Normalization** and **Data Type Conversion**

* **Min - Max** normalization is always preferred when the data has no outlers beacue it is very simple to implement

* Sci - kit is a powerful module which is used to perform data type conversion easilt by using the functions inside it

* Common types of Data type conversion

        --> Label Encoder
        --> One hot Encoding
        --> Dummy Encoding

### Real Time Applications:

* **Financial Services:** Normalizing stock prices and trading volumes ensures that a high-priced stock (e.g., $4,000) doesn't carry more weight in a portfolio analysis than a low-priced stock (e.g., $10).

* **Financial Reporting:** Converting currency stored as text into decimal or float so that it is easy to perform audits, calculate revenue or tax

* **E - Commerce Recommendations:** Normalizing user ratings allows a system to compare a harsh reviewer to a good one

* **IoT Sensor Networks:** Converting raw texts from temperature sensors to float numbers allows thermostat to perform the mathematical logic which is needed to turn on the AC
  
### Advantages:

* **Improved Model Accuracy:** By scaling all features to a similar range, you prevent machine learning algorithms from being biased toward variables with larger numerical magnitudes.

* **Faster Convergence:** Optimization algorithms (like Gradient Descent) reach the "best" solution much quicker because the error surface is more symmetrical and less distorted.

* **Reduced Storage and Redundancy:** In databases, it eliminates duplicate information, which saves disk space and ensures that data remains consistent across the entire system.

### Conclusion:

Thus, different types of Data Normalization and Data Conversion methods has been performed in the dataset and the output is verified.
