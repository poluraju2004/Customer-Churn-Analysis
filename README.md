# Customer Churn Analysis

## 📌 Project Overview

Customer Churn Analysis is a data analytics project that analyzes customer information to understand **why customers leave a service**.

The project uses **Python, Pandas, NumPy, Matplotlib, and Seaborn** to clean the dataset, perform exploratory data analysis (EDA), identify churn patterns, and create meaningful visualizations.

The main objective is to identify customer characteristics and service factors that are associated with customer churn.

---

## 🎯 Objectives

* Analyze customer churn behavior.
* Clean and prepare the customer dataset.
* Perform exploratory data analysis using Pandas and NumPy.
* Analyze numerical and categorical variables.
* Calculate important statistical measures.
* Identify patterns between customer characteristics and churn.
* Create meaningful visualizations.
* Generate business insights that can help reduce customer churn.

---

## 🛠️ Technologies Used

* **Python**
* **Pandas** – Data cleaning and DataFrame analysis
* **NumPy** – Numerical and statistical operations
* **Matplotlib** – Data visualization
* **Seaborn** – Statistical visualization
* **Jupyter Notebook** – Development and analysis environment
* **Git & GitHub** – Version control and project hosting

---

## 📂 Dataset

The project uses a **Customer Churn dataset** containing customer demographic, service, contract, payment, tenure, and billing information.

Important columns include:

* `SeniorCitizen`
* `tenure`
* `MonthlyCharges`
* `Total_Charges`
* `Churn`
* `Contract`
* `InternetService`
* `PaymentMethod`
* `gender`
* `Partner`
* `Dependents`
* `PhoneService`
* `TechSupport`
* `OnlineSecurity`
* `OnlineBackup`
* `DeviceProtection`
* `StreamingTV`
* `StreamingMovies`

The dataset contains approximately **7,043 customer records**.

---

## 🔄 Project Workflow

```text
Dataset
   ↓
Data Loading
   ↓
Data Inspection
   ↓
Data Cleaning
   ↓
Data Type Conversion
   ↓
NumPy Numerical Analysis
   ↓
Pandas Data Analysis
   ↓
Exploratory Data Analysis
   ↓
Matplotlib & Seaborn Visualization
   ↓
Churn Pattern Analysis
   ↓
Business Insights
```

---

## 🧹 Data Cleaning

The following data-cleaning operations were performed:

* Checked dataset shape.
* Checked column names.
* Checked missing values.
* Checked duplicate records.
* Converted `Total_Charges` into numeric format.
* Handled missing values.
* Converted the `Churn` variable into numerical form where required.
* Verified numerical and categorical data types.

Example:

```python
df["Total_Charges"] = pd.to_numeric(
    df["Total_Charges"],
    errors="coerce"
)
```

---

## 📊 Pandas Analysis

Pandas was used for:

* `head()`
* `tail()`
* `info()`
* `describe()`
* `shape`
* `columns`
* `isnull()`
* `duplicated()`
* `value_counts()`
* `groupby()`
* `pivot_table()`
* `nlargest()`
* `nsmallest()`
* `filter()`
* Sorting
* Data filtering

Example:

```python
df.groupby("Contract")["Churn"].mean()
```

---

## 🔢 NumPy Analysis

NumPy was used for numerical calculations and statistical analysis.

Operations include:

```python
np.array()
np.mean()
np.median()
np.min()
np.max()
np.sum()
np.std()
np.var()
np.percentile()
np.unique()
np.where()
np.argmax()
np.argmin()
np.isnan()
np.nanmean()
np.nanmedian()
np.nanmin()
np.nanmax()
np.count_nonzero()
```

Example:

```python
churn_rate = np.mean(df["Churn"]) * 100
```

---

## 📈 Data Visualization

The project uses **Matplotlib and Seaborn** to visualize customer churn patterns.

### Main Visualizations

1. Customer Churn Distribution
2. Customer Churn Percentage
3. Senior Citizen Distribution
4. Tenure Distribution
5. Monthly Charges Distribution
6. Tenure by Churn
7. Monthly Charges by Churn
8. Senior Citizen vs Churn
9. Tenure vs Monthly Charges
10. Churn Rate by Tenure
11. Correlation Heatmap
12. Churn by Gender
13. Churn by Contract
14. Churn by Internet Service
15. Churn by Payment Method
16. Churn by Partner
17. Churn by Dependents
18. Monthly Charges by Contract
19. Tenure by Contract

---

## 📊 Example Visualization Code

### Churn Distribution

```python
sns.countplot(
    data=df,
    x="Churn"
)

plt.title("Customer Churn Distribution")
plt.xlabel("Churn")
plt.ylabel("Number of Customers")

plt.show()
```

### Churn by Contract

```python
sns.countplot(
    data=df,
    x="Contract",
    hue="Churn"
)

plt.title("Churn by Contract Type")
plt.xlabel("Contract")
plt.ylabel("Number of Customers")

plt.show()
```

### Monthly Charges by Churn

```python
sns.boxplot(
    data=df,
    x="Churn",
    y="MonthlyCharges"
)

plt.title("Monthly Charges by Churn")
plt.xlabel("Churn")
plt.ylabel("Monthly Charges")

plt.show()
```

---

## 🔍 Key Analysis Questions

The project attempts to answer questions such as:

* What percentage of customers have churned?
* Which contract type has the highest churn?
* Does customer tenure affect churn?
* Do customers with higher monthly charges churn more?
* Does Internet Service type affect churn?
* Which payment method has higher churn?
* Does senior citizen status affect churn?
* Does having technical support affect churn?
* Does having a partner or dependents affect churn?
* Which customer groups are more likely to churn?

---

## 💡 Key Insights

The analysis can help identify patterns such as:

* Customers with shorter tenure may have a higher likelihood of churn.
* Month-to-month customers can show higher churn compared with customers on longer contracts.
* Monthly charges can differ between churned and non-churned customers.
* Certain payment methods and service combinations may be associated with higher churn.
* Customer demographics and additional services can provide useful churn-related patterns.

> The exact conclusions should be updated based on the final results generated from the dataset.

---

## 📁 Project Structure

```text
Customer-Churn-Analysis/
│
├── Customer_Churn_Analysis.ipynb
│
├── customer_churn_Cleaned_dataset.csv
│
├── graphs/
│   ├── churn_bar.png
│   ├── churn_pie.png
│   ├── tenure_histogram.png
│   ├── monthly_charges_histogram.png
│   ├── tenure_vs_churn.png
│   ├── monthly_charges_vs_churn.png
│   ├── churn_by_gender.png
│   ├── churn_by_contract.png
│   ├── churn_by_internet_service.png
│   ├── churn_by_payment_method.png
│   └── correlation_heatmap.png
│
├── README.md
│
└── requirements.txt
```

---

## 📦 Requirements

Create a `requirements.txt` file:

```text
pandas
numpy
matplotlib
seaborn
jupyter
```

Install the required libraries:

```bash
pip install -r requirements.txt
```

---

## ▶️ How to Run the Project

### 1. Clone the repository

```bash
git clone YOUR_GITHUB_REPOSITORY_URL
```

### 2. Open the project

```bash
cd Customer-Churn-Analysis
```

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

### 4. Start Jupyter Notebook

```bash
jupyter notebook
```

### 5. Open

```text
Customer_Churn_Analysis.ipynb
```

Run the notebook cells from top to bottom.

---

## 🚀 Future Improvements

The project can be extended by adding:

* Machine Learning churn prediction.
* Logistic Regression.
* Decision Tree.
* Random Forest.
* Customer churn probability.
* Feature engineering.
* Model evaluation.
* Confusion matrix.
* ROC-AUC analysis.
* Interactive dashboards using Power BI or Streamlit.
* Customer segmentation.

---

## 👨‍💻 Author

**Poluraju**

B.Tech – Computer Science and Engineering (Data Science)

GitHub: `https://github.com/poluraju2004`

---

## ⭐ Conclusion

Customer Churn Analysis demonstrates the complete data-analysis workflow, including **data cleaning, numerical analysis, exploratory data analysis, and visualization**.

The project provides insights into customer behavior and identifies factors that may contribute to customer churn, helping businesses develop strategies to improve customer retention.
