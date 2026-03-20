# Exploratory Data Analysis (EDA) 

##  Lab Title
**Exploratory Data Analysis on Titanic and House Prices Datasets**

---

##  Objective
The objective of this lab is to:

- Understand the process of Exploratory Data Analysis (EDA)
- Analyze and clean messy datasets
- Identify missing values, patterns, and anomalies
- Perform data preprocessing and transformation
- Create visualizations to gain insights
- Develop data storytelling skills

---

##  Tools Used

- Python
- Pandas
- NumPy
- Seaborn
- Matplotlib
- Jupyter Notebook / Anaconda

---

##  Datasets Used

### 1. Titanic Dataset
- Contains passenger information such as:
  - Age, Sex, Class, Fare, Survival status
- Includes missing values and inconsistencies

### 2. House Prices Dataset
- Contains housing data such as:
  - Location, income, population, house value

---

## Step-by-Step Process: Titanic Dataset

### 1. Loading the Data
- Imported datasets using `pandas.read_csv()`
- Displayed first rows using `.head()`

```python
pd.read_csv(url)
df.head()
```
### Screenshot of result
![Loading Dataset Output](https://i.postimg.cc/Cx5MXwms/Screenshot-2026-03-20-080848.png)

### 2. Initial Data Inspection
- Checked structure using `.info()`
- Viewed statistics using `.describe()`

```python
df.info()
df.describe()
```

### Screenshot of result
![Data Inspection Output](https://i.postimg.cc/HsfjBw3Q/statistical.png)

### 3. Summary Statistics
- Analyzed numerical features (mean, median, std)
- Reviewed categorical features (unique values, frequency)
  
### Screenshot of result
![Statistical Summary Output](https://i.postimg.cc/8kvCsJTm/summary.png)

### 4. Missing Values Analysis
- Used `.isnull().sum()` to detect missing values
- Visualized missing data using heatmaps

```python
df.isnull().sum()
sns.heatmap(df.isnull())
```

### Screenshot of result
![Missing Values Output](https://i.postimg.cc/YSFPQH06/missing-values.png)

### 5. Data Cleaning
- Filled missing values:
  - Median for numerical columns
  - Mode for categorical columns
- Dropped columns with many missing values (e.g., Cabin)

```python
df['column'].fillna(df['column'].median(), inplace=True)
df['column'].fillna(df['column'].mode()[0], inplace=True)
df.drop(columns='column', inplace=True)
```

### Screenshot of result
![Data Cleaning Output](https://i.postimg.cc/W3XwkWGC/data-cleaning.png)

### 6. Data Visualization

- Count plot

### Screenshot of result
![Count Plot Output](https://i.postimg.cc/63YFphTF/count-plot.png)

- Bar plot

### Screenshot of result
![Bar Plot Output](https://i.postimg.cc/k43WtrRT/Bar-Plot.png)

- Histograms

### Screenshot of result
![Histogram Output](https://i.postimg.cc/yNVH6xv1/Age-histogram.png)

- Box plot

### Screenshot of result
![Box Plot Output](https://i.postimg.cc/W4hPqCcv/Boxplot.png)


- Correlation heatmaps

### Screenshot of result
![Heat Map Output](https://i.postimg.cc/fbBJD6jM/heatmap-titanic.png)


## 🔍 Step-by-Step Process: House Prices Dataset

#### 1. Loading the Data

#### Screenshot of result
![Loading Dataset Output](https://i.postimg.cc/8CYgdSRG/house-loading-dataset.png)

#### 2. Initial Data Inspection

#### Screenshot of result
![Data Inspection Output](https://i.postimg.cc/hGLVTDWc/house-prices.png)

#### 3. Summary Statistics

#### Screenshot of result
![Statistical Summary Output](https://i.postimg.cc/SKSx1kYF/house-statistical.png)

#### 4. Missing Values Analysis

#### Screenshot of result
![Missing Values Output](https://i.postimg.cc/RVvCZvGH/house-missing-values.png)

#### 5. Data Cleaning

#### Screenshot of result
![Data Cleaning Output](https://i.postimg.cc/vZ1JQjRK/house-data-cleaning.png)

### Data Visualization for House Prices Dataset

- Count plot

### Screenshot of result
![Count Plot Output](https://i.postimg.cc/vmT4NsDS/house-count-plot.png)

- Bar plot

### Screenshot of result
![Bar Plot Output](https://i.postimg.cc/hGt2ZfLg/house-barplot.png)

- Scatter plot

### Screenshot of result
![Scatter Plot Output](https://i.postimg.cc/tTwFZr7C/scatterplot.png)

- Box plot

### Screenshot of result
![Box Plot Output](https://i.postimg.cc/QMvdYK24/house-boxplot.png)


- Correlation heatmaps

### Screenshot of result
![Heat Map Output](https://i.postimg.cc/wTWycMjZ/house-correlation.png)


---

## Key Observations / Lessons Learned

### Titanic Dataset
- Females had higher survival rates than males
- 1st class passengers had better survival chances
- Missing values in Age and Cabin required handling
- Fare and class influenced survival

### House Prices Dataset
- Median income strongly affects house value
- Missing values in `total_bedrooms` were handled
- Ocean proximity impacts prices
- Correlation heatmap revealed key relationships

---

##  Conclusion

- EDA is a crucial first step in data analysis
- Data cleaning improves accuracy
- Visualization helps uncover patterns
- Better understanding leads to better decisions

---
