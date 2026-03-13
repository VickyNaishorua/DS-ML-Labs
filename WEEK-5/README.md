#  Pandas, NumPy & Matplotlib

## Lab Title

**Data Manipulation, Numerical Computing, and Data Visualization using Pandas, NumPy, and Matplotlib**

---

## Objective

The objective of this lab is to:

* Understand how to manipulate datasets using **Pandas**
* Perform **numerical computations** using **NumPy**
* Create **data visualizations** using **Matplotlib**
* Practice **data merging, filtering, grouping, and aggregation**
* Learn **array operations and matrix manipulation**
* Visualize datasets using different types of plots

---

## Tools Used

* **Python 3**
* **Jupyter Notebook**
* **Pandas**
* **NumPy**
* **Matplotlib**
* **Git & GitHub**

---

# Step-by-Step Process

## 1. Data Manipulation with Pandas

### Creating DataFrames

DataFrames were created from dictionaries to simulate tabular datasets.

```python
import pandas as pd

df_5 = pd.DataFrame({
    'Names': ['Ama', 'Barry', 'Celestine', 'Dela'],
    'Score1': [1,2,3,4]
})

df_6 = pd.DataFrame({
    'Names': ['Barry', 'Dela', 'Emma', 'Frank'],
    'Score2': [5,6,7,8]
})
```
### Screenshot of result
![DataFrames Output](https://i.postimg.cc/sxX86KN4/merge-df.png)

---

## 2. Merging DataFrames

Different merge techniques were explored.

### Inner Merge

Keeps only rows that appear in both DataFrames.

```python
pd.merge(df_5, df_6, on="Names", how="inner")
```

### Outer Merge

Keeps all rows from both DataFrames.

```python
pd.merge(df_5, df_6, on="Names", how="outer")
```

### Left Merge

```python
pd.merge(df_5, df_6, on="Names", how="left")
```

### Right Merge

```python
pd.merge(df_5, df_6, on="Names", how="right")
```
### Screenshot of result
![Merging Output](https://i.postimg.cc/65CSH7Hf/merging-output.png)

---

## 3. Joining DataFrames

Joining combines DataFrames using **indexes**.

```python
df_9.join(df_10, how="inner")
```
### Screenshot of result
![Join Output](https://i.postimg.cc/nrtMzzPZ/join-output.png)

---

## 4. Filtering Data

Filtering allows selection of rows based on conditions.

```python
filtered_df = df[df['Age'] > 30]
```
### Screenshot of result
![Filter Output](https://i.postimg.cc/s27r2cdv/filter-output.png)

---

## 5. Adding and Removing Columns

### Add Column

```python
df['Gender'] = ['Male', 'Female', 'Male']
```

### Remove Column

```python
df.drop('City', axis=1, inplace=True)
```
### Screenshot of result
![Adding and Removing Output](https://i.postimg.cc/Fz2p1jQf/columns-output.png)

---

## 6. Grouping and Aggregation

Grouping helps summarize data.

### Mean Aggregation

```python
grouped_dff = dff.groupby('Age').mean()
```

### Maximum Value

```python
grouped_dff = dff.groupby('Age').max()
```
### Screenshot of result
![Grouping and Aggregation Output](https://i.postimg.cc/pL7sSbSF/aggregation-output.png)

---

## 7. Handling Missing Data

### Check Missing Values

```python
df.isnull()
```

### Drop Missing Values

```python
df.dropna()
```

### Fill Missing Values

```python
df.fillna(0)
```
### Screenshot of result
![Handling-missing data Output](https://i.postimg.cc/HsQHL4qj/missing-data.png)

---

# Numerical Computing with NumPy

## Creating Arrays

```python
import numpy as np

arr1d = np.array([1,2,3,4,5])
arr2d = np.array([[1,2,3],[4,5,6]])
```

---

## Array Attributes

```python
arr2d.shape
arr2d.size
arr2d.dtype
```
### Screenshot of result
![Numpy Array Attributes Output](https://i.postimg.cc/wTty4PsB/Array-Attributes.png)

---

## Array Operations

### Addition

```python
2 + arr2d
```

### Multiplication

```python
4 * arr2d
```
### Screenshot of result
![Numpy Array Operations Output](https://i.postimg.cc/WbPzS3j0/Array-Operations.png)

---

## Aggregation Functions

```python
arr2d.sum()
arr2d.max()
arr2d.min()
```
### Screenshot of result
![Numpy Array Aggeration Output](https://i.postimg.cc/8cZYFcbQ/numpy-aggregations.png)

---

## Array Manipulation

### Reshape

```python
arr2d.reshape(3,2)
```

### Concatenate

```python
np.concatenate([arr1d, arr1d])
```

### Append

```python
np.append(arr1d,[4,5,6])
```
### Screenshot of result
![Numpy Array Manipulation Output](https://i.postimg.cc/K8B5w4gh/Array-manipulation.png)
---

## Broadcasting

Broadcasting allows operations between arrays of different shapes.

```python
a = np.array([1,2,3])
b = 4
print(a + b)
```
### Screenshot of result
![Numpy Array Broadcasting Output](https://i.postimg.cc/jjWnmF1f/Broadcasting-array.png)

---

## Random Number Generation

```python
np.random.rand(3,3)
np.random.randint(0,100,6)
np.random.randn(4,7)
```
### Screenshot of result
![Random Numbers Output](https://i.postimg.cc/C1QPYXMY/randon-numbers.png)

---

# Linear Algebra Operations

### Matrix Addition

```python
A + B
```

### Matrix Multiplication

```python
A @ B
np.matmul(A,B)
np.dot(A,B)
```
### Screenshot of result
![Linear Algebra Output](https://i.postimg.cc/90BB0kCT/linear-algebra.png)

### Transpose

```python
np.transpose(A)
```

### Inverse Matrix

```python
np.linalg.inv(A)
```

### Identity Matrix

```python
np.eye(4)
```

### Determinant

```python
np.linalg.det(B)
```
### Screenshot of result
![Linear Algebra Output](https://i.postimg.cc/RZtNTHJp/Transpose.png)
---

# Data Visualization with Matplotlib

The **Iris dataset** was used for visualization.

```python
from sklearn.datasets import load_iris
import matplotlib.pyplot as plt
```
### Screenshot of result
![Iris Dataset Output](https://i.postimg.cc/4nRN2XMZ/load-iris-dataset.png)

---

## Bar Chart

Used to show frequency of each iris species.

```python
plt.bar(target_names, counts)
```
### Screenshot of result
![Bar Chart Output](https://i.postimg.cc/x1TXbywN/Bar-Chart.png)

---

## Pie Chart

Shows proportion of species.

```python
plt.pie(np.bincount(y), labels=target_names)
```
### Screenshot of result
![Pie Chart Output](https://i.postimg.cc/DwH7yrFY/Pie-Chart.png)

---

## Heatmap

Displays correlation between dataset features.

```python
plt.imshow(corr_matrix)
```
### Screenshot of result
![Heatmap Output](https://i.postimg.cc/VsGp8YzH/Heatmap.png)

---

## Line Plot

Shows trend of sepal length across samples.

```python
plt.plot(X[:,0])
```
### Screenshot of result
![Line Plot Output](https://i.postimg.cc/W3Rrrqm9/Line-Plot.png)

---

## Scatter Plot

Shows relationship between sepal length and sepal width.

```python
plt.scatter(X[y==i,0], X[y==i,1])
```
### Screenshot of result
![Scatter Plot Output](https://i.postimg.cc/gJwSchz5/Scatter-Map.png)


---

## Box Plot

Shows distribution of petal length.

```python
plt.boxplot(X[y == i,2])
```
### Screenshot of result
![Box Plot Output](https://i.postimg.cc/k5NM1VPJ/Box-Plot.png)

---

## Violin Plot

Displays distribution density of petal width.

```python
plt.violinplot(X[y == i,3])
```
### Screenshot of result
![Violin Plot Output](https://i.postimg.cc/BvJfvMk2/Violin-plot.png)

---

## Histogram

Shows frequency distribution.

```python
plt.hist(X[:,0], bins=20)
```
### Screenshot of result
![Histogram Output](https://i.postimg.cc/sXcYrDSJ/Histogram.png)

---

# Key Observations / Lessons Learned

* Pandas makes **data cleaning and manipulation easier** through DataFrames.
* Different **merge techniques** help combine datasets depending on the analysis goal.
* NumPy enables **fast numerical operations and matrix calculations**.
* Broadcasting simplifies mathematical operations across arrays.
* Matplotlib helps transform raw data into **visual insights**.
* Visualization improves understanding of **patterns, distributions, and relationships** in data.

---

# Conclusion

This lab provided hands-on experience with **data manipulation, numerical computing, and visualization in Python**. Using Pandas, NumPy, and Matplotlib together forms a strong foundation for **data analysis, machine learning, and data science workflows**.


