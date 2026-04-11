# Experiment 17: Exploring Statistical and Specialized Data Visualization Techniques
### 1. Aim
To explore and implement advanced statistical visualization techniques using Python libraries (**Matplotlib** and **Seaborn**) to identify outliers, detect correlations, and visualize the distribution and composition of complex datasets.

### 2. Introduction to Libraries Used
* **Pandas (pd):** Used for structuring raw data into DataFrames, allowing for easy statistical calculations like correlation matrices.
* **Matplotlib (plt):** Provides the foundational canvas for plotting and granular control over figure sizes, titles, and labels.
* **Seaborn (sns):** A high-level library that simplifies complex statistical plots (like Boxplots and Heatmaps) with built-in themes and color palettes.
* **NumPy (np):** Used for handling numerical arrays and mathematical operations necessary for generating sample data.

### 3. Common Utility Functions
* `plt.figure(figsize=(w, h))`: Adjusts the dimensions of the plot to ensure clarity in complex visuals.
* `plt.title()` / `plt.xlabel()` / `plt.ylabel()`: Standard functions used to provide context and axis descriptions.
* `plt.show()`: Final command to render the generated visualization.

### 4. Step-by-Step Procedure and Plotting Functions

#### Step 1: Boxplots (Outlier Detection)
* **Purpose:** To visualize the five-number summary (minimum, first quartile, median, third quartile, and maximum) and identify data points that fall outside the typical range (outliers).
* **Function:** `sns.boxplot(x=df['Column'])`
* **Visual Encoding:** The "box" represents the interquartile range (IQR), the line inside is the median, and individual dots outside the "whiskers" indicate potential anomalies in the data.

#### Step 2: Heatmaps (Correlation Analysis)
* **Purpose:** To represent the strength of relationships between multiple numerical variables in a graphical format.
* **Function:** `sns.heatmap(data, annot=True, cmap='coolwarm')`
* **Logic:** First, a correlation matrix is calculated using `df.corr()`. The heatmap then maps these values to a color gradient.
* **Visual Encoding:** Darker or more intense colors signify a stronger correlation (positive or negative), while `annot=True` prints the exact correlation coefficient on the grid.

#### Step 3: Bubble Plots (Multivariate Relationship)
* **Purpose:** To extend a scatter plot by adding a third dimension of data.
* **Function:** `plt.scatter(x, y, s=size_variable)`
* **Visual Encoding:** While `x` and `y` show the position, the `s` (size) parameter maps the area of each bubble to a numerical value (e.g., Sales volume). This allows the viewer to see three variables simultaneously on a 2D plane.

#### Step 4: Pie Charts (Composition)
* **Purpose:** To show the proportional relationship of different categories to the whole.
* **Function:** `plt.pie(values, labels, autopct='%1.1f%%')`
* **Visual Encoding:** Data is mapped to the angle/area of circular slices. The `autopct` parameter is used to automatically format and display the percentage value on each slice.

#### Step 5: Specialized Seaborn Visuals (Violin Plots)
* **Purpose:** To combine the features of a boxplot and a kernel density plot.
* **Function:** `sns.violinplot(x, y, data)`
* **Visual Encoding:** The width of the "violin" indicates the frequency of data points at that value. It provides a deeper look into the probability density of the data than a standard boxplot.

### 5. Conclusion
This experiment demonstrates how specialized plots go beyond simple trend analysis to provide deep statistical insights. By utilizing **Boxplots** for cleaning data (outliers) and **Heatmaps** for feature selection (correlation), we can make more informed data-driven decisions. Seaborn proves to be an essential tool for creating these aesthetically pleasing and mathematically rigorous visualizations with minimal code.
