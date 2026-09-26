# 📊 Sample Superstore Data Analysis

## 📌 Project Overview

This project performs **Exploratory Data Analysis (EDA)** on the Sample Superstore dataset to understand sales, profit, quantity, discounts, customer segments, shipping modes, product categories, and regional performance.

The analysis uses **Python, Pandas, NumPy, Matplotlib, and Seaborn** to clean, explore, visualize, and identify patterns and relationships within the dataset.

---

## 🎯 Objectives

* Understand the structure and characteristics of the Superstore dataset.
* Perform data cleaning and preprocessing.
* Analyze categorical and numerical variables.
* Identify patterns, trends, and relationships in the data.
* Analyze Sales, Profit, Quantity, and Discount.
* Compare performance across regions, segments, categories, and shipping modes.
* Detect and handle potential outliers.
* Create meaningful visualizations to support data-driven insights.
* Perform statistical and correlation analysis.

---

## 🗂️ Dataset

The project uses the **Sample Superstore dataset**.

The dataset contains information related to:

* Ship Mode
* Segment
* Country
* City
* State
* Region
* Category
* Sub-Category
* Sales
* Quantity
* Discount
* Profit
* Postal Code

The dataset is loaded into a Pandas DataFrame using:

```python
df = pd.read_csv("SampleSuperstore.csv")
```

---

## 🛠️ Technologies Used

| Technology       | Purpose                              |
| ---------------- | ------------------------------------ |
| Python           | Programming language                 |
| Pandas           | Data manipulation and analysis       |
| NumPy            | Numerical operations                 |
| Matplotlib       | Data visualization                   |
| Seaborn          | Statistical visualization            |
| Jupyter Notebook | Development and analysis environment |

---

## 🔍 Project Workflow

```text
Dataset
   ↓
Data Loading
   ↓
Data Understanding
   ↓
Data Cleaning
   ↓
Exploratory Data Analysis
   ↓
Univariate Analysis
   ↓
Bivariate / Multivariate Analysis
   ↓
Outlier Analysis
   ↓
Statistical Analysis
   ↓
Correlation Analysis
   ↓
Data Visualization
   ↓
Insights
```

---

## 🧹 Data Preprocessing

The following preprocessing and data-understanding steps were performed:

* Loaded the dataset using Pandas.
* Examined column names.
* Viewed the first and last records.
* Checked dataset dimensions.
* Checked data types.
* Inspected dataset information.
* Generated descriptive statistics.
* Checked for missing values.
* Removed the `Postal Code` column from analysis.
* Converted selected numerical columns to integer data types.

Example:

```python
df.isnull().sum()
```

```python
df['Sales'] = df['Sales'].astype(int)
df['Profit'] = df['Profit'].astype(int)
```

---

## 📈 Exploratory Data Analysis

### 1. Univariate Analysis

Univariate analysis was performed to understand individual variables and identify distributions, patterns, and potential outliers.

Categorical variables analyzed include:

* Ship Mode
* Segment
* Country
* City
* State
* Region
* Category
* Sub-Category

Numerical variables analyzed include:

* Sales
* Profit
* Quantity
* Discount

Visualizations include:

* Bar charts
* Histograms
* Distribution plots
* Count plots
* Pie charts

---

### 2. Bivariate and Multivariate Analysis

Relationships between multiple variables were explored using different visualization techniques.

Examples include:

* Sales vs Profit
* Discount vs Profit
* Quantity vs Sales
* Ship Mode vs Sales
* Region vs Sales
* Category vs Profit
* Segment vs Profit
* Region vs Discount

Visualizations include:

* Scatter plots
* Bar plots
* Line plots
* Box plots
* Violin plots

Example:

```python
sns.scatterplot(
    x='Sales',
    y='Profit',
    hue='Ship Mode',
    data=df
)
```

---

## 📦 Outlier Analysis

Box plots were used to identify potential outliers in numerical variables such as:

* Sales
* Profit
* Quantity
* Discount

The notebook also explores filtered datasets to examine the effect of removing selected extreme values.

Example:

```python
dfs = df[df['Quantity'] < 10]
```

---

## 📊 Statistical Analysis

A pivot table was created to summarize:

* Average Profit
* Total Quantity
* Total Sales

based on:

* Segment
* Ship Mode

Example:

```python
table = pd.pivot_table(
    df,
    index=['Segment', 'Ship Mode'],
    aggfunc={
        'Profit': np.mean,
        'Quantity': np.sum,
        'Sales': np.sum
    }
)
```

---

## 🔥 Correlation Analysis

Correlation analysis was performed on numerical variables to understand relationships between the quantitative features.

A **correlation heatmap** was created using Seaborn to visually represent the correlation matrix.

Key numerical variables include:

* Sales
* Quantity
* Profit
* Discount

---

## 📊 Visualizations

The project contains multiple visualizations, including:

* Count plots
* Bar charts
* Pie charts
* Histograms
* Distribution plots
* Scatter plots
* Line plots
* Box plots
* Violin plots
* Correlation heatmap

These visualizations help provide a better understanding of the dataset and its underlying patterns.

---

## 📁 Project Structure

```text
Sample-Superstore-Analysis/
│
├── Sample superstore analysis.ipynb
├── SampleSuperstore.csv
└── README.md
```

---

## 🚀 How to Run the Project

### 1. Clone the repository

```bash
git clone https://github.com/your-username/Sample-Superstore-Analysis.git
```

### 2. Navigate to the project directory

```bash
cd Sample-Superstore-Analysis
```

### 3. Install the required libraries

```bash
pip install numpy pandas matplotlib seaborn jupyter
```

### 4. Start Jupyter Notebook

```bash
jupyter notebook
```

### 5. Open the notebook

Open:

```text
Sample superstore analysis.ipynb
```

Make sure `SampleSuperstore.csv` is located in the same directory as the notebook.

---

## 💡 Key Analysis Areas

The project focuses on understanding:

* Sales distribution
* Profit distribution
* Quantity distribution
* Discount distribution
* Regional performance
* Customer segment distribution
* Product category distribution
* Sub-category distribution
* Shipping mode distribution
* Relationships between Sales and Profit
* Relationship between Discount and Profit
* Potential outliers
* Correlations between numerical variables

---

## 📌 Conclusion

This project demonstrates the use of **Python-based exploratory data analysis** to examine a retail Superstore dataset.

Through data preprocessing, statistical analysis, visualization, correlation analysis, and outlier analysis, the project provides a structured approach to understanding sales and profitability-related data.

The project also demonstrates practical skills in **Pandas, NumPy, Matplotlib, Seaborn, data cleaning, EDA, and data visualization**.

---

## 👨‍💻 Author

**Shaik Imam Sharif**

B.Tech – Data Science | 2026

### Skills Demonstrated

`Python` `Pandas` `NumPy` `Matplotlib` `Seaborn` `Data Analysis` `EDA` `Data Visualization` `Statistical Analysis`

---

⭐ If you find this project useful, consider giving the repository a star!
