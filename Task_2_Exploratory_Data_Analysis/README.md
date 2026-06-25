# Employee Data Analysis - Task 2: Exploratory Data Analysis (EDA)

## Project Overview
This repository contains the second phase of the Employee Data Lifecycle project. Following the successful data imputation and cleaning in Task 1, this phase focuses on **Exploratory Data Analysis (EDA)**. The objective is to leverage descriptive statistics, univariate visual distributions, bivariate trend analysis, and multivariate correlations to uncover structural workforce insights, identify senior leadership tiers, and evaluate departmental compensation variations.

---

## Technical Stack & Libraries
* **Language:** Python
* **Environment:** Jupyter Notebook
* **Data Manipulation:** `pandas`
* **Data Visualization:** `seaborn`

---

## Core Analysis & Methodology

### 1. Data Integrity Validation & Summary
Before charting visual trends, a structural overview was verified via descriptive statistics (`df.describe()`). Missing data gaps in the raw dataset were handled through targeted baseline imputation strategies (imputing numerical boundaries via `.median()` values and categorical boundaries via an `"UNKNOWN"` string literal). This process normalized the dataset size to 50 structurally sound employee entries.

### 2. Outlier Profiling (Univariate Distribution)
To satisfy rigorous data audit standards, targeted **Box Plots** were executed on key independent numerical axes:

* **Salary Outliers:** The distribution highlights a localized group of high-income outliers earning above $115,000. While statistically flagged as anomalies against the core distribution range ($64,250 to $83,750), they reflect realistic senior tier thresholds rather than mechanical logging bugs.
* **Age & Experience Outliers:** Age distributions cluster densely between 28 and 35, with specific outliers reaching ages 45–46. Concurrently, a severe experience outlier is isolated at 20 years. These insights validate the structural presence of a long-tenured operational leadership team.

### 3. Structural Trends (Bivariate Interaction)
To trace organizational growth and operational rules, multiple variables were paired to study corporate behaviors:

* **Experience vs. Salary (Scatter Plot):** Confirms a strong, direct positive correlation. Pay structures ascend linearly with job tenure. The plot exposes a vertical stack at 7.0 years and a flat horizontal shelf at $70,000, illustrating how central median data imputation shifts scatter plot geometry.
* **Department vs. Salary (Bar Chart):** The Finance division dominates average salary allocations, pushing near $100,000, while IT follows as the second highest paying vertical (~$78,000). Marketing and HR operate inside uniform, localized baseline pay brackets ($65,000 to $68,000).

### 4. Correlation Mechanics (Multivariate Assessment)
A specialized **Correlation Matrix Heatmap** was plotted using the `coolwarm` gradient scale to isolate key structural coefficients ($r$):

* **Age vs. Experience ($r = 0.79$):** Evaluated as the strongest linear relationship in the matrix, indicating that age naturally scales with professional tenure inside this firm.
* **Age & Experience vs. Salary ($r = 0.75$ and $0.68$):** Confirms that corporate compensation scaling laws heavily prize chronological experience and age profiles over alternate variances.

---

## Key Strategic Conclusions
1. **Tenure Predicts Earning Power:** There are zero signs of erratic pay scales. Compensation tracks reliably with age and experience.
2. **Finance & IT Are Capital Intensive:** Operational budget allocations are highly weighted toward Finance and Engineering/IT talent relative to administrative structures.
3. **Imputation Artifact Aware:** Analysts reviewing the data frames must stay aware of the artificial data clumping at 7.0 years of experience and $70,000 salary caused by median cleaning choices before running downstream prediction models.

---

## How to Run the Notebook
1. Clone this repository to your local directory.
2. Ensure you have the required dependencies installed:
   ```bash
   pip install pandas seaborn matplotlib
