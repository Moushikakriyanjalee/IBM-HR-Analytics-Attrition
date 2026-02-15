# Strategic Analysis of Employee Attrition using IBM HR Analytics Employee Attrition & Performance Dataset

![Python](https://img.shields.io/badge/Python-Data%20Analysis-blue)
---

## 📌 Project Overview
In today’s competitive business environment, employees are a company's most valuable asset. However, employee attrition remains a critical financial and operational challenge.

This project analyzes the **IBM HR Analytics Employee Attrition & Performance** dataset to identify the root causes of employee turnover. The analysis reveals an overall attrition rate of **16.12%**, meaning roughly 1 in 6 employees left during the period analyzed.

**The Objective:** To use Python-based data analytics to determine if factors such as **lower income**, **excessive overtime**, and **specific job roles** are statistically linked to higher turnover, and to provide actionable recommendations for HR retention strategies.
---

## 📂 Data Set

### Data Source
* **Dataset:** IBM HR Analytics Employee Attrition & Performance.
* **Size:** 1,470 rows and 35 features.
* **Content:** Demographic, operational, and sentimental data points.
---

## ⚙️ Methodology 

### 01.Data Preprocessing:
To ensure accuracy, the following cleaning steps were performed:
* **Removed Redundant Columns:** `StandardHours`, `Over18`, and `EmployeeCount` were dropped as they contained zero variance.
* **Encoding:** Categorical variables (`Attrition`, `OverTime`, `Gender`) were converted to binary formats (1/0) for statistical testing.
* **Missing Value Check:** Confirmed the dataset had no null values; no imputation was required.

### 02.Exploratory Data Analysis (EDA): 
* Visualizing distributions of age, income, and department.

### 03.Statistical Validation:
* Using Pearson Correlation matrices and Independent T-Tests to separate random noise from meaningful patterns.
---

## 🔍 Key Findings

### 1. The "Burnout" Signal (Overtime)
Analysis identifies **Overtime** as the strongest behavioral predictor of attrition. Employees who are asked to work extra hours leave at a disproportionately higher rate than those with standard workloads.


### 2. Lower Income Drivers
There is a strong inverse relationship between income and retention.
* **Leavers:** Heavily concentrated in the **$2,500–$5,000** monthly income bracket.
* **Stayers:** Evenly distributed across higher income ranges.


### 3. Demographic Risks
Attrition is noticeably higher among:
* **Young Employees:** Ages 25–30.
* **Entry-Level Roles:** Sales Representatives and Laboratory Technicians.

---

## 📊 Statistical Validation

To prove these patterns were not random, statistical hypothesis testing was conducted.

### Correlation Matrix Analysis
* **Overtime (r = 0.25):** The strongest positive correlation. Working overtime is the single biggest statistical predictor of quitting.
* **Monthly Income (r = -0.16):** Confirms that higher pay reduces the likelihood of turnover.
* **Total Working Years (r = -0.13):** Employees with more experience are less likely to resign.

### Independent T-Test (The Income Check)
An Independent Samples T-Test was performed to answer: *"Is the salary difference between leavers and stayers statistically significant?"*

* **Result:** The p-value is significantly lower than 0.05.
* **Conclusion:** The Null Hypothesis is rejected. The salary gap is statistically significant and a driver of attrition.

---

## 💡 Recommendations for Decision-Making

Based on the data, the following strategic actions are recommended:

1.  **Reduce Overtime:** Immediate audit of departments with high overtime. It is more cost-effective to hire additional staff than to absorb the recruitment costs of replacing burned-out employees.
2.  **Fix Pay Gaps:** Conduct market salary adjustments for high-risk roles (Sales Reps, Lab Techs) currently earning between $2,500–$5,000.
3.  **Support Young Talent:** Implement mentorship programs and clear career pathing for employees aged 25–30 to improve retention of future leaders.

---

## 🛠 Tools Used
* **Python:** Primary analysis language.
* **Pandas:** Data manipulation and cleaning.
* **Seaborn/Matplotlib:** Data visualization.
* **SciPy:** Statistical hypothesis testing (T-Test).

---
## How to Run the Project

### Prerequisites
To run this analysis locally, you will need the following installed:
* **Python 3.8+**
* **Jupyter Notebook** (or access to Google Colab)
* **Python Libraries:**
    * `pandas`
    * `numpy`
    * `matplotlib`
    * `seaborn`
    * `scipy`
    * `kagglehub` (for downloading the dataset automatically)

### 2. Steps to Execute

#### Option A: Running in Google Colab (Recommended)
1.  **Download** the `IBM_HR_Analysis.ipynb` file from this repository.
2.  Upload the file to **[Google Colab](https://colab.research.google.com/)**.
3.  The notebook includes a cell to install necessary libraries (`!pip install kagglehub`). Run this first.
4.  Go to **Runtime** > **Run all** to execute the full analysis.

#### Option B: Running Locally
1.  **Clone the Repository:**
    ```bash
    git clone https://github.com/Moushikakriyanjalee/IBM-HR-Analytics-Attrition.git
    cd IBM-HR-Analytics-Attrition
    ```
2.  **Install Dependencies:**
    ```bash
    pip install pandas numpy matplotlib seaborn scipy kagglehub
    ```
3.  **Launch the Notebook:**
    ```bash
    jupyter notebook IBM_HR_Analysis.ipynb
    ```
4.  **Execute:**
    Click **Kernel** > **Restart & Run All** to generate the charts and statistical results.



