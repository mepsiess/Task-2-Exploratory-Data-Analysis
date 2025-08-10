# Task 2 - Exploratory Data Analysis (EDA)

**Aim:** Understanding the Titanic dataset using descriptive statistics and visualizations with Pandas, Matplotlib, Seaborn, and Plotly.


## Tools and Libraries used in the Dataset

- Pandas: For Data Manipulation and Statistics
- Matplotlib: For basic plotting
- Seaborn: For advanced statistical visualizations
- Plotly: For interactive and engaging visualizations


---

## Introduction

This project focuses on performing **Exploratory Data Analysis (EDA)** on the Titanic dataset.  
EDA is a critical step in data science where we summarize main characteristics of the data and use visual methods to uncover patterns, relationships, and anomalies.

In this project, I explored the dataset using various statistical and graphical techniques to gain insights before applying any predictive models.

The main objectives were to:

- Generate summary statistics (mean, median, standard deviation, etc.)
- Visualize numeric features using histograms and boxplots
- Explore feature relationships through pairplots and correlation matrices
- Identify patterns, trends, and anomalies in the dataset
- Make feature-level inferences from the visuals

---

## Learning Outcomes

1. **Understanding EDA:**  
   EDA is the process of analyzing datasets to summarize their key characteristics, often with visual methods.  
   It helps identify trends, detect outliers, and guide further analysis or modeling.

2. **Summary Statistics:**  
   Learned how to calculate measures like mean, median, standard deviation, and skewness to understand data distribution.

3. **Data Visualization:**  
   Gained experience in creating histograms, boxplots, heatmaps, and pairplots to better understand numerical and categorical data.

4. **Pattern Recognition:**  
   Discovered survival patterns across different passenger classes, genders, and embarkation points.

5. **Anomaly Detection:**  
   Used boxplots and statistical checks to spot unusual values (e.g., very high fares or ages).

---

## Step-by-Step Explanation

### Step 1: Importing and Exploring the Dataset
The dataset was loaded using the `pandas` library. This step involved reading the CSV file into a DataFrame for structured analysis.

```
import pandas as pd
df = pd.read_csv("titanic.csv")
```


### Step 2: Generating Summary Statistics
Calculated descriptive statistics for numeric columns:
- Mean, median, and standard deviation
- Skewness to identify asymmetric distributions


### Step 3: Visualizing Data Distributions
Created histograms and boxplots to see the spread and detect potential outliers:
- Age Distribution
- Fare Distribution
- Passenger Class Distribution

```
import seaborn as sns
import matplotlib.pyplot as plt

sns.histplot(df['Age'], bins=20, kde=True)
plt.title("Age Distribution")
plt.show()
```


### Step 4: Exploring Feature Relationships
Used correlation matrices and pairplots to identify relationships between features:
- Positive and negative correlations between variables
- Survival correlations with Fare, Age, and Class

```
numeric_df = df.select_dtypes(include=['number'])
sns.heatmap(numeric_df.corr(), annot=True, cmap="coolwarm")
```


### Step 5: Identifying Trends, Patterns, and Anomalies
- Higher survival rate among females and first-class passengers
- Passengers who paid higher fares tended to survive more
- Outliers detected in Fare and Age using boxplots


### Step 6: Making Feature-Level Inferences
While inspecting the visualizations I recorded:
- Women had a significantly higher survival rate
- First-class passengers were more likely to survive
- Average fare of survivors was higher than non-survivors


## Dataset Used
[Titanic Dataset](https://www.kaggle.com/datasets/yasserh/titanic-dataset)


## Made By: Mansi Gupta
