# 🎬 Netflix Data Analysis & Visualization

> 📊 Exploring **8,807 Netflix Movies & TV Shows** using Python, Pandas, NumPy, Matplotlib & Seaborn.

Welcome to my **Netflix Data Analysis** project! 🍿📈

This project is an **Exploratory Data Analysis (EDA)** of the Netflix Titles dataset. The analysis focuses on understanding the structure of the dataset, identifying missing values, comparing **Movies vs TV Shows**, and exploring Netflix release trends over the years.

The entire analysis was performed using **Google Colab** and the notebook is available in this repository. 🚀

---

## 🌟 Project Highlights

🔹 Explore the Netflix dataset and understand its structure
🔹 Analyze **8,807 Netflix titles**
🔹 Identify missing values in different columns
🔹 Visualize missing data using a heatmap
🔹 Compare **Movies vs TV Shows**
🔹 Analyze Netflix releases across different years
🔹 Create meaningful visualizations using Matplotlib & Seaborn

---

## 🛠️ Technologies & Libraries

🐍 **Python**

🐼 **Pandas** — Data manipulation and analysis

🔢 **NumPy** — Numerical operations

📊 **Matplotlib** — Data visualization

🎨 **Seaborn** — Statistical visualization

☁️ **Google Colab** — Development environment

---

## 📂 Dataset

The project uses the **Netflix Titles Dataset**, containing information about movies and TV shows available on Netflix.

### 📌 Dataset Information

* 🎬 **Total Titles:** 8,807
* 📋 **Total Columns:** 12
* 🎥 **Content Types:** Movies & TV Shows
* 📅 **Release Years:** 1925–2021

### Dataset Columns

| Column         | Description                         |
| -------------- | ----------------------------------- |
| `show_id`      | Unique ID of the title              |
| `type`         | Movie or TV Show                    |
| `title`        | Name of the title                   |
| `director`     | Director of the title               |
| `cast`         | Cast members                        |
| `country`      | Country of production               |
| `date_added`   | Date added to Netflix               |
| `release_year` | Original release year               |
| `rating`       | Content rating                      |
| `duration`     | Movie duration or number of seasons |
| `listed_in`    | Genre/category                      |
| `description`  | Description of the title            |

---

# 🔍 Exploratory Data Analysis

## 1️⃣ Importing Libraries

The project begins by importing the required Python libraries:

```python
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns
```

These libraries are used for **data processing, numerical operations, and visualization**.

---

## 2️⃣ Loading the Dataset 📦

The Netflix dataset is loaded using Pandas:

```python
df = pd.read_csv("netflix_titles.csv.zip")
```

The first and last few records are then displayed using:

```python
df.head()
df.tail()
```

This gives an initial understanding of how the dataset is structured.

---

## 3️⃣ Understanding the Dataset 🧠

The dataset structure is explored using:

```python
df.shape
df.columns
df.info()
```

### 📊 Dataset Summary

| Property        |     Value |
| --------------- | --------: |
| Total Rows      | **8,807** |
| Total Columns   |    **12** |
| Numeric Columns |     **1** |
| Object Columns  |    **11** |

This step helps understand the **size, columns, data types, and non-null values** present in the dataset.

---

## 4️⃣ Total Netflix Titles 🎬

The total number of Netflix titles is calculated using:

```python
print("Total Netflix titles: ", len(df))
```

### Result

🎬 **Total Netflix Titles: 8,807**

---

# 🔎 Missing Value Analysis

Missing values are checked using:

```python
df.isnull().sum()
```

The columns containing missing values are then filtered:

```python
missing = df.isnull().sum()
print(missing[missing > 0])
```

### 📌 Missing Values Found

| Column       | Missing Values |
| ------------ | -------------: |
| `director`   |          2,634 |
| `cast`       |            825 |
| `country`    |            831 |
| `date_added` |             10 |
| `rating`     |              4 |
| `duration`   |              3 |

The missing values are also visualized using a **Seaborn heatmap**.

```python
sns.heatmap(df.isnull(), cbar=False)
```

📊 This provides a visual representation of where information is missing in the dataset.

---

# 🎥 Movies vs TV Shows

The dataset contains two major types of Netflix content:

* 🎬 Movies
* 📺 TV Shows

The distribution is analyzed using:

```python
df["type"].value_counts()
```

A Seaborn count plot is then used to visualize the comparison:

```python
sns.countplot(data=df, x="type")
```

This makes it easier to visually compare the number of **Movies and TV Shows** in the dataset.

---

# 📅 Netflix Releases Over the Years

The number of titles released in each year is calculated using:

```python
year_count = df["release_year"].value_counts().sort_index()
```

A line graph is then created to visualize the release trend:

```python
plt.figure(figsize=(12,5))
plt.plot(year_count.index, year_count.values)
```

### 📈 Observation

The dataset contains titles released between **1925 and 2021**.

Some of the highest numbers of titles in the dataset were released during the late 2010s, with:

* 🥇 **2018 — 1,147 titles**
* 🥈 **2017 — 1,032 titles**
* 🥉 **2019 — 1,030 titles**
* **2020 — 953 titles**
* **2021 — 592 titles**

This visualization helps identify how the number of titles varies across different release years.

---

# 📊 Visualizations

The project currently includes the following visualizations:

### 🔹 Missing Values Heatmap

Helps identify missing data across the dataset.

### 🔹 Movies vs TV Shows Count Plot

Shows the distribution of Netflix content by type.

### 🔹 Netflix Releases Over the Years

A line chart showing the number of titles released in each year.

---

# 📓 Google Colab Notebook

This project was created and executed using **Google Colab**.

You can open the notebook directly in Google Colab and run the analysis step by step.

> ☁️ **Recommended:** Open the `.ipynb` file in Google Colab for the complete analysis and visualizations.

---

# 📁 Repository Structure

```text
Netflix-Data-Analysis/
│
├── 📜 LICENSE
├── 📓 Netflix_Data_Analysis.ipynb
├── 📖 README.md
└── 📦 netflix_titles.csv.zip
```

> 📌 If the dataset is not included in the repository, download the dataset separately and place it in the same directory as the notebook.

---

# 🚀 Future Improvements

This project can be expanded with more detailed analysis such as:

⭐ Rating-wise analysis
🌍 Country-wise Netflix content
🎭 Genre-wise analysis
🎬 Top directors and actors
📅 Content added to Netflix by year
⏱️ Movie duration analysis
📺 TV Show season analysis
🔥 Most common Netflix genres
📊 Interactive dashboards

---

# 🎯 Learning Outcomes

Through this project, I practiced:

✅ Loading real-world datasets using Pandas
✅ Understanding DataFrame structure
✅ Exploring rows and columns
✅ Checking data types and missing values
✅ Performing basic EDA
✅ Using Pandas for data analysis
✅ Creating visualizations with Matplotlib
✅ Creating statistical plots with Seaborn
✅ Interpreting patterns and trends in data

---

## 📜 License

This project is licensed under the MIT License.

See the [LICENSE](LICENSE) file for more details.

# 👩‍💻 Author

### Misbah Fathima

🎓 3rd Year Computer Science & Engineering Student
💻 Exploring **Python, Java, Data Structures & Data Analysis**

---

## ⭐ If You Like This Project

If you found this project interesting, consider giving the repository a **⭐ Star**!

> 💡 **“Data becomes powerful when we turn it into insights.”** 📊✨

---

### 🏷️ Topics

`Python` `Pandas` `NumPy` `Matplotlib` `Seaborn` `Netflix` `Data-Analysis` `EDA` `Data-Visualization` `Google-Colab` `Jupyter-Notebook`
