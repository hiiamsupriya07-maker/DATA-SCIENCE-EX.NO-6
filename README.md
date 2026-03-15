# EXNO-6-DS-DATA VISUALIZATION USING SEABORN LIBRARY

# Aim:
  To Perform Data Visualization using seaborn python library for the given datas.

# EXPLANATION:
Data visualization is the graphical representation of information and data. By using visual elements like charts, graphs, and maps, data visualization tools provide an accessible way to see and understand trends, outliers, and patterns in data.

# Algorithm:
STEP 1:Include the necessary Library.

STEP 2:Read the given Data.

STEP 3:Apply data visualization techniques to identify the patterns of the data.

STEP 4:Apply the various data visualization tools wherever necessary.

STEP 5:Include Necessary parameters in each functions.

# Coding and Output:
```
# Import required libraries
import pandas as pd
import seaborn as sns
import matplotlib.pyplot as plt
# Load the iris dataset
iris = sns.load_dataset("iris")

# Display first five rows
print(iris.head())

# Display dataset information
print(iris.info())
sns.pairplot(
    data=iris,
    hue="species",       # color based on species
    palette="Set2"       # color style
)

plt.title("Pair Plot of Iris Dataset")
plt.show()
sns.scatterplot(
    x="sepal_length",
    y="sepal_width",
    hue="species",
    style="species",
    data=iris,
    palette="deep"
)

plt.title("Sepal Length vs Sepal Width")
plt.xlabel("Sepal Length")
plt.ylabel("Sepal Width")
plt.show()
sns.boxplot(
    x="species",
    y="petal_length",
    data=iris,
    palette="Set3"
)

plt.title("Box Plot of Petal Length by Species")
plt.show()
sns.violinplot(
    x="species",
    y="petal_width",
    data=iris,
    palette="pastel"
)

plt.title("Violin Plot of Petal Width by Species")
plt.show()
sns.histplot(
    data=iris,
    x="sepal_length",
    kde=True,          # Kernel Density Estimate
    bins=20,
    color="blue"
)

plt.title("Distribution of Sepal Length")
plt.show()
sns.barplot(
    x="species",
    y="sepal_length",
    data=iris,
    palette="Set1",
    ci=None
)

plt.title("Average Sepal Length for each Species")
plt.xlabel("Species")
plt.ylabel("Sepal Length")
plt.show()
sns.countplot(
    x="species",
    data=iris,
    palette="Set2"
)

plt.title("Count of Each Iris Species")
plt.xlabel("Species")
plt.ylabel("Count")
plt.show()
sns.jointplot(
    x="sepal_length",
    y="sepal_width",
    data=iris,
    kind="scatter",
    color="purple",
    height=6
)

plt.show()
sns.distplot(
    iris["petal_length"],
    bins=20,
    kde=True,
    color="green"
)

plt.title("Distribution of Petal Length")
plt.xlabel("Petal Length")
plt.ylabel("Density")
plt.show()
sns.histplot(
    data=iris,
    x="petal_length",
    bins=20,
    kde=True,
    color="green"
)

plt.title("Distribution of Petal Length")
plt.show()
```
# Result:
 Thus ,data visualization using seaborn python library was done successfully. 
