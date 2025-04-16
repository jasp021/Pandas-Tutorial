# 📊 Pandas Practice on Ubuntu WSL with VS Code

Welcome to my journey of learning **Pandas** using **Ubuntu WSL** on **Windows 11** with **Visual Studio Code**! 🚀  
This repository documents hands-on examples inspired by [Code With Harry’s tutorial](https://youtu.be/RhEjmHeDNoA?si=WMHZN94ogMhoEUWQ). Whether you're a beginner or just brushing up, you'll find valuable examples here!

---

## 📦 Requirements

Before diving into the code, make sure you have the following installed:

```bash
pip install pandas
pip install numpy
pip install xlrd
pip install openpyxl
```
These packages enable us to:

- **pandas**: For data manipulation and analysis 🐼

- **numpy**: For numerical operations ➕➖✖️➗

- **xlrd & openpyxl**: For reading and writing Excel files 📗
------------------------------------
## 🛠️ What You’ll Learn

### 🧱 Creating DataFrames

```python
import pandas as pd
import numpy as np

data = {
    "name": ['harry', 'rohan', 'skillf', 'shubh'],
    "marks": [92, 34, 24, 17],
    "city": ['rampur', 'kolkata', 'bareilly', 'antarctica'],
}

df = pd.DataFrame(data)
```
-----------------------------------------
### 💾 Exporting to CSV

```python
df.to_csv('friends.csv')  # Includes index
df.to_csv('friends_index_false.csv', index=False)  # Excludes index
```
-----------------------
### 👀 Viewing Data

```python
df.head(2)  # First 2 rows
df.tail(2)  # Last 2 rows
df.describe()  # Summary statistics
```
------------------------------
### 📖 Reading CSV & Excel

```python
jaspreet = pd.read_csv('jaspreet.csv')
data = pd.read_excel('data.xlsx', sheet_name='Sheet2')
```
-------------------------------------
### 🧪 DataFrame Operations
- Setting custom indices

  **jaspreet.index = ['first', 'second', 'third', 'fourth']**    

- Creating random data:

```python
newdf = pd.DataFrame(np.random.rand(334, 5), index=np.arange(334))
```
- Modifying and querying:

```python
newdf.loc[0, 0] = 654
newdf.columns = list("ABCDE")
newdf = newdf.drop(0, axis=1)
```
----------------------------------
### 🧹 Cleaning Data

- Drop duplicates:

```python
df.drop_duplicates(subset=["name"], keep="last")
```
- Reset index:

```python
newdf.reset_index(drop=True, inplace=True)
```
- Handling missing data:

```python
df['toy'].value_counts(dropna=False)
```
--------------------------------
### 📈 Statistics and Correlations

```python
dfsol.mean()
dfsol.corr()
dfsol.count()
dfsol.max()
dfsol.min()
dfsol.median()
dfsol.std()
```
------------------------------
### 📌 Notes
- Used WSL on Windows 11 for Linux-like environment 💻🐧

- Coding and testing done in Visual Studio Code

- Practiced reading/writing Excel and CSV files for real-world data scenarios 📊📁

-----------------------------
### 🔗 Credits
Big thanks to [Code With Harry](https://www.codewithharry.com/) for the excellent tutorial!

-----------------------------
### 📜 License

This project is licensed under the MIT License.
You are free to use, modify, and distribute it — just give credit! ❤️

------------------------------

#### ⭐ If you find this helpful, consider giving this repo a star!
#### Happy coding! 🧑‍💻🌟
-----------------------------
