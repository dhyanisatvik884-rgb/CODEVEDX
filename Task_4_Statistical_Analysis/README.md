# Project 4: Statistical Analysis using Python

## 📋 Project Overview
The objective of this project is to apply mathematical and statistical techniques to interpret data, validate underlying assumptions, and execute empirical hypothesis testing. Rather than merely calculating surface-level numbers, this phase builds a scientific validation layer to mathematically prove whether observed workplace trends are genuinely real or simply products of random sampling variation.

Per the internship criteria, this task satisfies the following core milestones:
* **Accurate:** Executed precise scientific computation engines to handle standard errors and test distributions accurately.
* **Hypothesis-Based:** Defined strict Null ($H_0$) and Alternative ($H_1$) criteria before performing computations to establish clear mathematical boundaries.
* **Result-Oriented & Well-Explained:** Integrated programmatic logical filters directly within execution blocks to dynamically evaluate significance markers against established alpha thresholds ($\alpha = 0.05$).

---

## 📊 Dataset Structure
The analysis was performed on the cleaned workforce tracking dataset (`dataset.csv`), leveraging the median-imputed values from previous milestones to ensure optimal data alignment across columns:
* **Dimensions:** 50 rows, 7 columns
* **Target Analytical Attributes:** `Department`, `Salary`, `Experience`

---

## 🛠️ Data Cleaning & Imputation Pipeline
To preserve the overall dataset distribution characteristics and avoid losing useful rows, an explicit imputation methodology was implemented:

1. **Numerical Variables (Age, Salary, Experience):** Missing values were systematically replaced using the column **Median**. This fills in the blanks by establishing a solid baseline centered around the overall sample trends.
2. **Categorical Variables (Department, City):** Missing text fields were filled using a distinct string placeholder (`"UNKNOWN"`). This approach ensures that incomplete entries are accounted for transparently without skewing the proportions of identified departments or cities.

*Post-cleaning validation confirmed that the absolute missing value count across all columns dropped successfully to 0.*

---

## 📉 Visual Insights & Trends
By avoiding manual textual interpretations, the project successfully deployed algorithmic validation rules inside the Jupyter Notebook cells to output clear, automated data storytelling outcomes:

* **Departmental Pay Variance:** The system computed a **t-Statistic of 2.9248** and a **p-Value of 0.0084**. Because the probability value sits safely below the significance threshold ($p < 0.05$), the system automatically rejected the Null Hypothesis, proving that the IT department operates on a significantly distinct salary scale compared to HR.
* **Tenure Scale Significance:** The system computed a **Pearson Correlation Coefficient ($r$) of 0.6774** paired with a critical **p-Value of 6.5457e-08**. This nearly 0 probability value confirms that the positive scaling trend between a professional's experience matrix and their compensation layer is highly stable and verified by mathematical science.

---

## 💻 Environment & Tech Stack
* **Language:** Python
* **Environment:** Jupyter Notebook / JupyterLab (VS Code)
* **Libraries Used:** Pandas, SciPy (`scipy.stats`)