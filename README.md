# 🎬 Netflix Data Analysis & Visualization

> 📊 **Exploring Netflix Movies & TV Shows using Python, Pandas, NumPy, Matplotlib & Seaborn**

Welcome to **Netflix Data Analysis**! 🍿
This project performs **Exploratory Data Analysis (EDA)** on the Netflix titles dataset to discover patterns, distributions, missing data, and trends in Netflix's movies and TV shows.

The project also uses **data visualization** to make the insights easier to understand. 📈✨

---

## 🚀 Project Overview

The goal of this project is to explore the **Netflix Titles Dataset** and answer questions such as:

* 🎬 How many titles are available in the dataset?
* 📺 How many are **Movies** and how many are **TV Shows**?
* 🔍 Where is the data missing?
* 📅 How have Netflix releases changed over the years?
* 📊 What patterns can we observe from the available data?

---

## 🛠️ Technologies Used

| Technology        | Purpose                      |
| ----------------- | ---------------------------- |
| 🐍 **Python**     | Programming Language         |
| 🐼 **Pandas**     | Data manipulation & analysis |
| 🔢 **NumPy**      | Numerical operations         |
| 📊 **Matplotlib** | Data visualization           |
| 🎨 **Seaborn**    | Statistical visualization    |

---

## 📂 Dataset

The project uses the **Netflix Titles Dataset** stored as:

```text
netflix_titles.csv.zip
```

The dataset contains information about Netflix movies and TV shows, including details such as:

* 🎥 Title type
* 📝 Title
* 📅 Release year
* 🌍 Country
* 🎭 Genre / listed in
* 👤 Cast
* 🎬 Director
* ⏱️ Duration
* 🔞 Rating
* 📖 Description

---

## 🔎 Exploratory Data Analysis

The following analysis has been performed:

### 1️⃣ Dataset Overview

The program explores the dataset using:

```python
df.head()
df.tail()
df.shape
df.columns
df.info()
```

This helps understand the **structure, size, columns, and data types** of the dataset.

---

### 2️⃣ Total Number of Netflix Titles 🎬

The total number of records is calculated using:

```python
len(df)
```

This gives the overall number of Netflix titles available in the dataset.

---

### 3️⃣ Missing Data 🔍

Missing values are identified using:

```python
df.isnull().sum()
```

Only columns containing missing values are displayed for easier analysis.

A **Seaborn heatmap** is also used to visually identify where data is missing.

```python
sns.heatmap(df.isnull(), cbar=False)
```

📌 This makes it easier to understand the completeness of the dataset.

---

### 4️⃣ Movies vs TV Shows 🎥📺

The distribution of Netflix content types is analyzed using:

```python
df["type"].value_counts()
```

A **count plot** is created using Seaborn to visually compare:

* 🎬 Movies
* 📺 TV Shows

This provides a quick overview of the type of content available in the dataset.

---

### 5️⃣ Netflix Releases Over the Years 📅📈

The number of titles released in each year is calculated using:

```python
year_count = df["release_year"].value_counts().sort_index()
```

A line graph is then used to visualize the number of Netflix titles across different release years.

This helps identify **release trends and changes over time**.

---

## 📊 Visualizations

The project currently includes:

### 🔹 Missing Data Heatmap

Shows the locations of missing values in the dataset.

### 🔹 Movies vs TV Shows Count Plot

Compares the number of Movies and TV Shows.

### 🔹 Netflix Releases Over the Years

Shows how the number of titles varies by release year.

---

## 📁 Project Structure

```text
Netflix-Data-Analysis/
│
├── 📄 netflix_analysis.py
├── 📦 netflix_titles.csv.zip
└── 📖 README.md
```

---

## ⚙️ How to Run

### 1️⃣ Clone the repository

```bash
git clone <your-repository-url>
```

### 2️⃣ Navigate to the project folder

```bash
cd Netflix-Data-Analysis
```

### 3️⃣ Install the required libraries

```bash
pip install pandas numpy matplotlib seaborn
```

### 4️⃣ Run the Python program

```bash
python netflix_analysis.py
```

📌 Make sure `netflix_titles.csv.zip` is present in the same directory as the Python file.

---

## 💡 Key Learning Outcomes

Through this project, I practiced:

* 🐍 Working with Python for data analysis
* 🐼 Reading and exploring datasets using Pandas
* 🔍 Identifying missing values
* 📊 Performing basic Exploratory Data Analysis
* 📈 Creating visualizations with Matplotlib
* 🎨 Creating statistical plots with Seaborn
* 🧹 Understanding and inspecting real-world datasets

---

## 🌱 Future Improvements

This project can be extended by adding:

* ⭐ Rating distribution analysis
* 🌍 Country-wise content analysis
* 🎭 Genre analysis
* 📅 Detailed year-wise trends
* 🎬 Top directors and actors
* ⏱️ Movie duration analysis
* 🔞 Rating-wise content distribution
* 📊 Interactive dashboards
* 🤖 More advanced data analysis

---

## 👩‍💻 Author

**Misbah Fathima**

🎓 3rd Year Computer Science & Engineering Student
💻 Exploring **Python, Java, Data Structures & Data Analysis**

---

## ⭐ Support

If you find this project useful or interesting, consider giving the repository a **⭐ Star**!

> **“Data tells a story — visualization helps us see it.”** 📊✨

---

### 🏷️ Topics

`Python` `Pandas` `NumPy` `Matplotlib` `Seaborn` `Data-Analysis` `EDA` `Data-Visualization` `Netflix` `Machine-Learning`
