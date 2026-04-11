# Experiment 16 - Basic Charts and Visual Encoding

### Aim:

To implement basic charts in Python for visualizing data

### Tools used:

Google Colab or Jupyter Notebook

### Theory:

#### Matplotlib

Matplotlib is the foundational library in Python, which is used to create static and creative visualizations. It provides an object-oriented interface that allows granular control over every element of the figure, which includes axes, labels, line styles, edge color, etc. It is designed to resemble MATLAB's plotting capabilities. 

It is widely used for generating publication-quality plots such as line graphs, scatter plots, and histograms. While it is incredibly powerful, creating complex visualizations often requires writing extensive code to manage fine details. It serves as the base upon which many other specialized plotting libraries are built.

#### Seaborn

It is the high-level data visualization library built on Matplotlib, which is used for advanced statistical graphs. It simplifies the creation of complex plots by providing a more concise syntax and integrating seamlessly with Pandas DataFrames. 

Seaborn comes with built-in themes and color patterns, which makes the plot look professionally good and presentation-ready with minimal effort. The addition of features like edge color and line width is added by default without any specifications while writing the code. It excels at visualizing multivariate relationships, offering specialized functions for heatmaps, violin plots, and regression models.

#### Types of Charts:

1. Line Graph:

* A line graph displays information as a series of data points called "markers" connected by straight line segments to show how a value changes over a continuous interval.

  

* It is primarily used to track changes over short and long periods of time or to identify trends in data.

  

* By visualizing the slope between points, users can quickly determine if a variable is increasing, decreasing, or remaining stable.

  

* They are the standard choice for time-series analysis, such as monitoring temperature fluctuations or stock market trends.

2. Bar Chart:

* A bar chart represents categorical data with rectangular bars where the lengths or heights are proportional to the values they represent.

  

* These charts can be plotted vertically or horizontally and are used to compare distinct groups or categories against one another.

  

* They are highly effective for showing large differences in data and making specific values easy to read at a glance.

  

* Common uses include comparing the populations of different countries or the sales performance of various products within a single quarter.

3. Histogram:

* A histogram is used to represent the distribution of a single continuous numerical variable by dividing the data into "bins" or intervals.

  

* Unlike a bar chart, the bars in a histogram are adjacent to each other, indicating a continuous range of values rather than discrete categories.

  

* Its primary purpose is to show the underlying frequency distribution, such as whether the data is normal (bell-shaped), skewed, or contains outliers.

  

* It is essential for understanding the spread and central tendency of datasets, like exam scores or height measurements.

4. Scatter Plot:

* A scatter plot uses dots to represent the values for two different numeric variables, with the position of each dot representing a single data point on the horizontal and vertical axes.

  

* This visualization is used to observe and show relationships or correlations between two variables.

  

* It helps in identifying patterns such as positive or negative trends, clusters, or gaps in the data. Researchers often use scatter plots to determine if one variable might be a predictor of another, such as the relationship between study hours and test results.

5. Seaborn Line Plot:

* A Seaborn line plot is a high-level statistical visualization that enhances the basic line graph by automatically aggregating data and displaying uncertainty.

  

* It is specifically designed to handle Pandas DataFrames, making it easy to plot multiple observations for the same x-value, which it represents as a single line with a translucent "shadow" representing the confidence interval.

  

* The purpose of use is to visualize the relationship between two variables while accounting for variance or noise in the data. It is ideal for scientific research where showing the reliability of a trend is just as important as the trend itself.

### Learning Outcomes:

* Various charts such as bar graphs, line charts, and histograms are made to visualize the data in an animated way.

The figure size can be changed in the *.figure** function in Matplotlib.

Labels can be added to either of the axes by using the *.xlabel** and .ylabel commands.

* A for loop can be used to show the value of data marked in the chart as a numerical value.

* Seaborn is used to make advanced plots, which are made in Matplotlib, and also some extra plots such as heatmaps, boxplots, etc.

### Applications of lists:

* Stock Market Analysis: Line graphs are used to monitor the price fluctuations of shares over months or years to identify bullish or bearish trends.

* Survey Result Visualization: A bar chart is used by researchers to display responses and quickly show which opinion holds the majority within a demographic.

* Quality Control in Manufacturing: Engineers use histograms to visualize the weight or dimensions of parts to ensure most fall within the "target" range.

* Real Estate Pricing: Real estate agents plot house square footage against price to see how size influences cost and to spot undervalued properties.

* Seaborn Line Plot: Data scientists use these plots to track "loss" or "accuracy" over multiple training epochs, using the confidence interval to see model stability.

  

### Advantages:

* Rapid Data Interpretation: Charts allow the human brain to process large volumes of information at a glance by converting numbers into visual shapes.

* Identification of Patterns and Trends: Visualizing data makes it simple to recognize recurring cycles, seasonal variations, and long-term correlations between different variables.

* Spotting Anomalies and Outliers: Charts highlight data points that fall far outside the expected range, making errors or unique occurrences immediately obvious.

* Enhanced Decision Making: By providing a clear and objective summary of the current situation, charts support more accurate and confident strategic planning.

### Conclusion:

Thus, modules like Matplotlib and Seaborn were used to visualize data and observe trends in a dataset, and the output is verified.
