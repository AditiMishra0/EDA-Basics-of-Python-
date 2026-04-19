# **Experiment 18-  Advanced Visualizations: Hierarchical, Interactive, and Multi-Dimensional Charts**

## Aim

To understand and implement advanced data visualization techniques used for representing complex datasets using Python libraries such as **Plotly**, **SciPy**, and **Matplotlib-Venn**.

## Introduction

Data visualization plays a critical role in transforming raw numerical information into meaningful visual insights. While traditional charts such as bar graphs, pie charts, and line plots are useful for basic comparisons, they often fail to represent complex relationships found in real-world datasets.

Modern applications require visualization techniques that can illustrate:

* Nested or hierarchical relationships
* Movement of data between stages
* Overlapping data sets
* Multi-variable relationships
* Three-dimensional interactions

Advanced visualization tools enable users to interact with the data through zooming, rotating, filtering, and hovering features. These interactions improve user understanding and allow analysts to explore patterns that might otherwise remain hidden in static representations.

This experiment demonstrates how specialized visualization methods can be used to represent structured, clustered, and multi-dimensional data effectively.

---

## Theoretical Background

### 1. Treemap Visualization

A Treemap is a hierarchical visualization technique that represents data using nested rectangular regions. Each rectangle corresponds to a category, and its area is proportional to the numerical value it represents.

Treemaps are especially useful when dealing with hierarchical datasets where each parent category contains multiple subcategories. Instead of using multiple pie charts or bar graphs, a Treemap consolidates all levels of hierarchy into a single visual layout.

### Key Characteristics

* Represents hierarchical relationships visually
* Uses area to indicate magnitude
* Supports multiple nested levels
* Efficient use of available display space

### Applications

Treemaps are widely used in:

* Financial portfolio distribution
* File system storage analysis
* Market share comparison
* Budget allocation representation

---

### 2. Dendrogram and Hierarchical Clustering

A Dendrogram is a tree-like structure used to visualize hierarchical clustering results. It represents how individual data points group together step-by-step during clustering.

Hierarchical clustering is an unsupervised learning technique used to group similar objects into clusters based on distance measures. The clustering process begins by treating each data point as an individual cluster and then successively merges clusters based on similarity.

The **linkage method** determines how distances between clusters are calculated. In this experiment, the **Ward method** is used, which minimizes the total variance within clusters.

### Key Characteristics

* Displays cluster formation sequence
* Helps identify natural groupings
* Determines optimal number of clusters
* Useful for pattern recognition

### Applications

Dendrograms are commonly used in:

* Bioinformatics for gene classification
* Customer segmentation
* Pattern recognition
* Image processing

---

### 3. Sankey Diagram

A Sankey diagram is a specialized flow diagram used to represent the movement of quantities from one stage to another. The defining feature of a Sankey diagram is that the width of each flow path is proportional to the quantity it represents.

This visualization technique helps in understanding how resources, energy, or data are distributed across different stages of a system.

### Key Characteristics

* Represents directional flow
* Uses variable-width connections
* Displays multiple pathways
* Highlights loss or gain between stages

### Applications

Sankey diagrams are widely used in:

* Energy consumption tracking
* Student progression analysis
* Supply chain visualization
* Resource allocation studies

---

### 4. Radar (Spider) Chart

A Radar Chart, also known as a Spider Chart, is used to visualize multi-dimensional numerical data. Each variable is represented as an axis radiating outward from a central point. Data values are plotted on these axes and connected to form a polygon.

Radar charts are particularly useful for comparing multiple attributes simultaneously.

### Key Characteristics

* Displays multiple variables at once
* Allows comparison between categories
* Highlights strengths and weaknesses
* Useful for performance evaluation

### Applications

Radar charts are commonly used in:

* Skill assessment analysis
* Employee performance evaluation
* Athlete performance comparison
* Product feature comparison

---

### 5. 3D Scatter Plot

A 3D Scatter Plot extends traditional scatter plots by introducing a third dimension represented along the Z-axis. This allows simultaneous visualization of three continuous variables within a single graphical space.

3D visualization enables analysts to study relationships that may not be visible in two-dimensional plots.

### Key Characteristics

* Represents three variables simultaneously
* Supports rotation and zoom interaction
* Helps detect correlations and clusters
* Improves spatial data interpretation

### Applications

3D scatter plots are widely used in:

* Academic performance analysis
* Engineering simulations
* Scientific modeling
* Machine learning data exploration

---

### 6. Venn Diagram (Set Visualization)

A Venn Diagram visually represents logical relationships between sets. It uses overlapping circles to show common elements shared between groups.

This visualization technique is based on the principles of set theory and is useful for analyzing similarities and differences between datasets.

### Key Characteristics

* Shows intersections between sets
* Highlights unique and shared elements
* Supports comparative analysis
* Simple yet effective visualization

### Applications

Venn diagrams are used in:

* Data comparison studies
* Marketing audience analysis
* Survey result comparison
* Logical reasoning tasks

---

## Procedure

The experiment was carried out in the following structured steps:

### Step 1: Import Required Libraries

Essential Python libraries were imported to support visualization and clustering operations.

* Plotly Express
* Plotly Graph Objects
* SciPy Hierarchical Clustering
* Matplotlib-Venn

---

### Step 2: Perform Hierarchical Clustering

A coordinate-based dataset was created and hierarchical clustering was applied using the linkage method.

The dendrogram function was then used to visualize how clusters were formed based on similarity.

---

### Step 3: Generate Interactive 3D Scatter Plot

A dataset containing Study Hours, Marks, and Attendance was used to generate a 3D scatter plot.

Interactive rotation and zoom features allowed deeper analysis of relationships among variables.

---

### Step 4: Create Sankey Diagram

A Sankey diagram was constructed to represent the flow of students through different academic stages such as Admission, First Year, Second Year, and Placement.

---

### Step 5: Develop Radar Chart

Student skill levels across multiple technical domains were plotted using a Radar chart to analyze strengths and weaknesses visually.

---

### Step 6: Construct Treemap

Hierarchical data categories were visualized using nested rectangles to represent relative proportions effectively.

---

### Step 7: Generate Venn Diagram

Set intersections were visualized using overlapping circles to represent common and unique elements between datasets.

---

## Implementation Highlights

### 3D Scatter Plot using Plotly

```python
fig = px.scatter_3d(df, 
                    x='Study_Hours', 
                    y='Marks', 
                    z='Attendance')

fig.show()
```

---

### Hierarchical Clustering using SciPy

```python
from scipy.cluster.hierarchy import dendrogram, linkage

linked = linkage(data, method='ward')

dendrogram(linked)
```

---

### Sankey Diagram Flow Visualization

```python
fig = go.Figure(data=[go.Sankey(
    node=dict(label=["Admission",
                     "First Year",
                     "Second Year",
                     "Placed"]),
                     
    link=dict(source=[0, 1, 2],
              target=[1, 2, 3],
              value=[100, 80, 60])
)])
```

---

## Key Functions Used

| Function          | Library              | Purpose                                     |
| ----------------- | -------------------- | ------------------------------------------- |
| px.treemap()      | Plotly Express       | Creates hierarchical treemap visualizations |
| linkage()         | SciPy                | Performs hierarchical clustering            |
| dendrogram()      | SciPy                | Displays cluster relationships              |
| venn2()           | Matplotlib-Venn      | Displays intersections between two sets     |
| go.Sankey()       | Plotly Graph Objects | Visualizes flow between stages              |
| go.Scatterpolar() | Plotly Graph Objects | Generates Radar/Spider charts               |
| px.scatter_3d()   | Plotly Express       | Creates interactive 3D scatter plots        |

---

## Applications

Advanced visualization techniques are widely applied across various domains.

### Education Technology

Used to track student retention, performance patterns, and academic progression using Sankey diagrams and clustering techniques.

### Human Resource Analytics

Radar charts help identify skill gaps, measure employee competencies, and assist in recruitment decisions.

### Financial Analysis

Treemaps allow visualization of investment distribution across sectors, improving portfolio management.

### Biological Research

Dendrograms are useful in studying genetic similarities and evolutionary relationships among species.

### Engineering Systems

Flow diagrams help analyze system performance, resource distribution, and production workflows.

---

## Results and Observations

The experiment demonstrated that advanced visualization techniques provide significantly greater analytical clarity compared to traditional charts.

Interactive plots improved the ability to explore relationships dynamically. Hierarchical clustering revealed meaningful data groupings, while flow diagrams helped track transitions across different stages.

Multi-dimensional charts enhanced understanding of relationships among multiple variables simultaneously.

---

## Outcome

By completing this experiment, the following outcomes were achieved:

* Developed proficiency in creating interactive visualizations
* Learned techniques to represent hierarchical and clustered data
* Gained experience in visualizing multi-dimensional datasets
* Improved ability to interpret complex data relationships
* Enhanced skills in scientific and analytical data storytelling

---

## Conclusion
Advanced visualization techniques significantly enhance the process of data analysis by enabling the representation of complex relationships that cannot be captured using standard charts.
By integrating tools such as Plotly and SciPy, it becomes possible to create dynamic and informative visual models capable of handling hierarchical, multi-dimensional, and flow-based datasets.
These visualization methods not only improve analytical efficiency but also contribute to better communication of insights across scientific, engineering, and business applications.
