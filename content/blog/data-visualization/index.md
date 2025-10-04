---
title: Data Visualization in R
summary: Learn the basics of ggplot2 package for your numerous data visualization task.
date: 2023-10-25
authors:
  - admin
tags:
  - Data Visualization
  - ggplot2
  - Grammar of graphics
image:
  caption: ''
---

## Data Visualization in R using ggplot2
Data visualization is an important step in data analysis. It helps us to understand patterns, trends, and relationships in the data.  
In R, one of the most popular packages for visualization is **ggplot2**. It is based on the **Grammar of Graphics**, which builds plots by layering components 
such as data, aesthetics, and geoms. To use this package in R, we will first need to install it if it is not already installed and then load the library to use it the functions available within the package.
```r
install.packages("ggplot2") # Install ggplot2 if not already installed
library(ggplot2) # Load the library
```
We’ll use the mtcars dataset which contains data on fuel consumption and car design. Then, we can plot mpg (miles per gallon) against hp (horsepower).
```r
head(mtcars)
ggplot(data = mtcars, aes(x = hp, y = mpg)) +
  geom_point(color = "blue", size = 3) +
  labs(title = "Scatter Plot of Horsepower vs. MPG",
       x = "Horsepower",
       y = "Miles per Gallon") +
  theme_minimal()
```
{{< figure src="/images/histogram.png" title="" >}}

The plot output shows that cars with higher horsepower tend to have lower fuel efficiency (mpg). We can add more embelishment to several components of the plot but for this short tutorial, we will only learn how to add color by group.
```r
ggplot(mtcars, aes(x = hp, y = mpg, color = factor(cyl))) +
  geom_point(size = 3) +
  labs(title = "Horsepower vs. MPG Colored by Cylinders",
       color = "Cylinders", x = "Horsepower", y = "Miles per Gallon") +
  theme_light()
```
{{< figure src="/images/histogram_color.png" title="" >}}
We can also create an histogram looking at the distribution of miles per gallon (mpg) using the line of code below:
```r
ggplot(mtcars, aes(x = mpg)) +
  geom_histogram(binwidth = 2, fill = "skyblue", color = "black") +
  labs(title = "Distribution of Miles per Gallon",
       x = "Miles per Gallon",
       y = "Count") +
  theme_classic()
```
{{< figure src="/images/hist.png" title="" >}}
This histogram shows how mpg values are distributed across cars.
Boxplots are also very useful to see spread and outliers present in our data. In the line of code below, we will visualize mpg across different cylinder groups.
```r
ggplot(mtcars, aes(x = factor(cyl), y = mpg, fill = factor(cyl))) +
  geom_boxplot() +
  labs(title = "Boxplot of MPG by Number of Cylinders",
       x = "Cylinders",
       y = "Miles per Gallon") +
  theme_bw()
```
{{< figure src="/images/boxplot.png" title="" >}}
This boxplot shows that cars with more cylinders generally have lower mpg. With ggplot2, we can build many types of plots with a simple and flexible syntax.
From scatter plots to boxplots, ggplot2 provides an excellent toolkit for data visualization. Try experimenting with your own datasets and layering more components such as smooth lines, facets, or themes which was not covered in this short tutorial.

In case you want to download the dataset used for this tutorial which is also readily available in base r, use the button below:

{{< button url="/data/results.csv" style="outline" icon="document-arrow-down" >}}Download Data{{< /button >}}

To also learn more on data visualization using R, check out these websites.

{{< button url="https://r4ds.hadley.nz/" new_tab="true" style="secondary" rounded="full" align="center" >}}R for Data Science{{< /button >}}

&nbsp;

{{< button url="https://ggplot2-book.org/" new_tab="true" style="primary" rounded="full" align="center" icon="rocket-launch" >}}Elegant Graphics for Data Analysis{{< /button >}}


### Did you find this page helpful? Consider sharing it 🙌
