# Customer Churn Prediction using Machine Learning

##  Objective
The primary goal of this project is to build and evaluate machine learning models to predict customer churn within a banking dataset. By identifying high-risk customers, businesses can implement proactive retention strategies to minimize revenue loss.

### Project Focus:
* **Comparison:** Evaluating classical models (KNN, Decision Tree, Random Forest, SVM) against advanced Gradient Boosting (XGBoost, LightGBM).
* **Optimization:** Implementing `GridSearchCV` and `RandomizedSearchCV` for hyperparameter tuning.
* **Engineering:** Handling categorical encoding, feature scaling, and data imbalance.
* **Architecture:** Utilizing both Procedural and Object-Oriented Programming (OOP) approaches for model deployment.

---

##  Tools and Technologies
* **Data Handling:** `Pandas`, `NumPy`
* **Visualization:** `Matplotlib`, `Seaborn`
* **Machine Learning:** `Scikit-learn`, `XGBoost`, `LightGBM`
* **Model Persistence:** `Joblib`

---

## Dataset Description
The dataset contains **10,000 customer records** with features representing demographics and banking behavior.

| Feature | Description |
| :--- | :--- |
| **CreditScore** | Customer creditworthiness |
| **Geography** | Location (France, Spain, Germany) |
| **Gender** | Male/Female |
| **Age** | Customer age |
| **Tenure** | Number of years with the bank |
| **Balance** | Account balance |
| **NumOfProducts** | Number of bank products used |
| **HasCrCard** | 1 = Yes, 0 = No |
| **IsActiveMember** | Activity status |
| **EstimatedSalary** | Annual salary |
| **Exited (Target)** | **1 = Churn, 0 = Retained** |

---

##  Methodology

### 1. Data Preprocessing
* **Feature Selection:** Filtered demographic and financial indicators.
* **Encoding:** Applied One-Hot Encoding via `pd.get_dummies(drop_first=True)` to convert categorical variables while avoiding the dummy variable trap.
* **Scaling:** Normalized numerical features using `MinMaxScaler` to ensure models like KNN and SVM perform optimally.

### 2. Model Implementation
We implemented models using two design patterns:
* **Procedural Approach:** Linear flow for quick experimentation and tuning.
* **OOP Approach:** Encapsulated logic within a `ChurnPrediction` class for production-ready, reusable code.

### 3. Hyperparameter Tuning
To move beyond default performance, we utilized:
* **GridSearchCV:** Exhaustive search over a specified parameter grid.
* **RandomizedSearchCV:** Statistical sampling of parameters for faster exploration of large search spaces.

---

##  Results and Observations

### Model Performance Comparison

| Model | Accuracy | AUC Score |
| :--- | :---: | :---: |
| KNN | 0.81 | 0.75 |
| Decision Tree | 0.80 | 0.72 |
| **Random Forest** | **0.86** | **0.87** |
| SVM | 0.85 | 0.83 |

### Gradient Boosting Optimization

| Model | Approach | Accuracy | AUC Score |
| :--- | :--- | :---: | :---: |
| **XGBoost** | Basic | 0.8695 | 0.8502 |
| **XGBoost** | **RandomSearch** | **0.8665** | **0.8788** |
| **LightGBM** | Basic | 0.8635 | 0.8685 |
| **LightGBM** | GridSearch | 0.8635 | 0.8748 |



### Key Insights
1. **Model Efficiency:** `LightGBM` demonstrated significantly faster training times, making it ideal for larger datasets.
2. **Predictive Power:** `XGBoost` combined with `RandomizedSearchCV` yielded the highest **AUC Score (0.8788)**, indicating superior ability to distinguish between churn and retention.
3. **Metric Selection:** While accuracy is high across models, **ROC-AUC** was prioritized to ensure the model handles the slight class imbalance effectively.

---

## Conclusion
Advanced Gradient Boosting algorithms (XGBoost/LightGBM) consistently outperform classical models in this churn prediction task. The project highlights that while Random Forest is a strong baseline, fine-tuned boosting models offer the precision required for high-stakes business decisions.

---

### Screenshots 

![Model Performance Comparison](https://i.postimg.cc/768BRvqT/Screenshot-2026-03-28-222822.png)

![Confusion Matrix: XGBoost with RandomizedSearchCV](https://i.postimg.cc/SQ7yDkkH/Screenshot-2026-03-28-223803.png)

![Classification Metrics by Class](https://i.postimg.cc/xdtvKWqK/Screenshot-2026-03-28-224840.png)



