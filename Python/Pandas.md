# Pandas

## LeetCode 30 Days Pandas

### Links


- General
  - [30 days Pandas](https://leetcode.com/studyplan/30-days-of-pandas/)
- Data Filtering
- String Methods
- Data Manipulation
  - [178. 🟡 Rank Scores](https://leetcode.com/problems/rank-scores)
  - [183. 🟡 Department Highest Salary](https://leetcode.com/problems/department-highest-salary/)

### Data Manipulation

## 📖 Definitions:

### Data Manipulation 🛠️

Data manipulation is the process of adjusting, changing, or controlling data to prepare it for analysis. It involves tasks like sorting, cleaning, and merging data.

### Bandwidth 🌐

Bandwidth is the maximum data transfer rate of a network or system. It's essential for fast data transfers, streaming, and more.

## 🐼 Data Manipulation in Pandas:

### 1. 🔧 Import Pandas
Always start with:
```python
import pandas as pd
```

### 2. 📑 Read Data

- **CSV 📄**:
```python
df = pd.read_csv('data.csv')
```

### 3. 🔍 Filtering Data

Find specific rows:
```python
filtered_data = df[df['age'] > 25]
```

### 4. 💧 Handle Missing Values

Fill missing spots:
```python
df['age'].fillna(df['age'].mean(), inplace=True)
```

### 5. 🧮 Aggregate Data

Group and calculate:
```python
avg_age = df.groupby('department')['age'].mean()
```

### 6. 🔄 Merge Data

Combine datasets:
```python
merged_data = pd.merge(df1, df2, on='id')
```

## 🤖 For Machine Learning:

### 1. 🏗️ Feature Engineering

Modify or create new data features.

### 2. ⚖️ Feature Scaling

Normalize or standardize data.

### 3. ✂️ Data Splitting

Separate data into train and test sets.

### 4. 🔡 Encode Data

Turns categories into numbers.
