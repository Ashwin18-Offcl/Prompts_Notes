# Pandas_Notes — Complete Pandas Guide (Beginner → Advanced)

**Pandas_Notes** is a structured, easy-to-understand collection of pandas notes, examples, cheat-sheets, and hands-on practice files to master data analysis, data cleaning, transformation, and exploration using Python’s pandas library.

---

## 🖼️ Visual Banner  
<p align="center">
  <img src="https://github.com/Ashwin18-Offcl/Pandas_Notes/blob/main/pandas.png"
       width="1200"
       height="360"
       alt="Pandas Banner"/>
</p>

---

## 🚀 Quick Overview
- **What:** Beginner-friendly + professional pandas notes for practical use.  
- **Who:** Data Analysts, Students, Python Learners & Interview Preparation.  
- **Covers:** DataFrames, I/O, cleaning, merging, grouping, reshaping, time series & performance.

## 📚 Table of Contents
1. [Introduction](#-introduction)  
2. [Why pandas?](#-why-pandas)  
3. [Repository Structure](#-repository-structure)  
4. [How to Use](#-how-to-use)  
5. [Step-by-Step Topics](#-step-by-step-topics)  
6. [Code Examples](#-code-examples)  
7. [CheatSheet & Practice](#-cheatsheet--practice)  
8. [Contributing](#-contributing)  
9. [Tags](#-tags)  
10. [License](#-license)

## 🧩 Introduction
**pandas** is a powerful Python library for working with structured (tabular) data.  
It provides two essential data structures:

- **Series** → 1D labeled array  
- **DataFrame** → 2D table-like data  

This repository simplifies pandas concepts using short notes, clean examples, cheat sheets, and real-world tasks.

## ✨ Why pandas?
- Easy handling of tabular data  
- Fast CSV/Excel/SQL reading & writing  
- Powerful groupby + aggregation  
- Simple merging, joining, concatenation  
- Supports time series, reshaping & pivoting  
- Ideal for data analysis & ML pipelines  

## 📂 Repository Structure
```
Pandas_Notes/
├─ README.md
├─ Introduction_to_Pandas.md
├─ 01_Series_and_DataFrame.md
├─ 02_IO_Read_Write.md
├─ 03_Indexing_Filtering.md
├─ 04_Missing_Data.md
├─ 05_GroupBy_Aggregation.md
├─ 06_Merge_Join_Concat.md
├─ 07_Reshape_Pivot.md
├─ 08_TimeSeries.md
├─ 09_Performance.md
├─ 10_Practice_Problems.md
├─ Examples/
│   ├─ basics.ipynb
│   ├─ cleaning_examples.py
│   ├─ groupby_examples.ipynb
├─ CheatSheet.pdf
└─ images/
    └─ pandas.png
```
## ⚙️ How to Use

### 1. Clone the repository
```bash
git clone https://github.com/Ashwin18-Offcl/Pandas_Notes.git
cd Pandas_Notes
```
### 2. (Optional) Create virtual environment
```bash
python -m venv venv
source venv/bin/activate       # macOS/Linux
venv\Scripts\activate          # Windows
```
### 3. Install pandas
```bash
pip install pandas jupyter matplotlib
```
### 4. Run examples
```bash
jupyter notebook Examples/basics.ipynb
python Examples/cleaning_examples.py
```
## 🧭 Step-by-Step Topics

### **Beginner**
- Series & DataFrame basics  
- Creating DataFrames  
- Reading data: CSV, Excel, JSON  
- Indexing & slicing (`loc`, `iloc`)  
- Filtering with conditions  

### **Intermediate**
- Handle missing data (dropna, fillna)  
- GroupBy, aggregation, transform  
- Merging & joining tables  
- Concatenate, append, combine  
- Reshape with pivot, melt, stack  

### **Advanced**
- Time series: resample, shifting  
- Categorical data & memory optimization  
- Rolling/expanding windows  
- `.query()` & `.eval()` performance tricks  
- Real world data cleaning workflows  

## 🧪 Code Examples

### Create DataFrame
```python
import pandas as pd

df = pd.DataFrame({
    "Name": ["A", "B", "C"],
    "Age": [20, 30, 25],
    "Score": [85, 90, 88]
})
print(df)
```

### Read CSV & clean missing values
```python
df = pd.read_csv("data.csv")
df.dropna(subset=["Age"], inplace=True)
df["Age"] = df["Age"].astype(int)
```

### GroupBy aggregation
```python
grouped = df.groupby("Department").agg(
    total_salary=("Salary", "sum"),
    avg_salary=("Salary", "mean"),
    employees=("ID", "count")
)
print(grouped)
```

### Merge / Join
```python
merged = orders.merge(customers, on="customer_id", how="left")
```

### Pivot Table
```python
pivot = df.pivot_table(
    index="Region",
    columns="Product",
    values="Sales",
    aggfunc="sum",
    fill_value=0
)
print(pivot)
```

### Time Series Resampling
```python
df["Date"] = pd.to_datetime(df["Date"])
df.set_index("Date", inplace=True)
monthly = df["Sales"].resample("M").sum()
```

## 📄 CheatSheet & Practice
- **CheatSheet.pdf** provides quick formulas & function summaries  
- Practice problems include:  
  - Cleaning datasets  
  - GroupBy challenges  
  - Pivot table transformations  
  - Time series operations  
  - End-to-end data manipulation tasks
    
## 🤝 Contributing
Contributions are welcome!

You can add:
- More examples  
- Additional topic explanations  
- New practice problems  
- Bug fixes or formatting improvements  

Steps:
1. Fork this repo  
2. Create a new branch  
3. Commit changes  
4. Submit a Pull Request  


## 🏷 Tags
```
python, pandas, data-analysis, data-cleaning, data-science, pandas-notes, jupyter, cheat-sheet, learning-resources
```

