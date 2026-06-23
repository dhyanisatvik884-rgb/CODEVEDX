# Project 1: Data Analysis with Python

## 📋 Project Overview
The objective of this project is to convert raw, unstructured workforce data into clear, accurate, and actionable organizational information. This folder contains the end-to-end data processing pipeline executed within a Jupyter Notebook environment, focusing heavily on rigorous data cleaning, structural validation, and categorical distribution mapping.

Per the internship criteria, this task satisfies the following core milestones:
* **Well-Structured:** Verified explicit dataset coordinates, index integrity, and standard feature attributes.
* **Clean and Accurate:** Implemented strict statistical imputation rules to resolve missing records without discarding rows, keeping data results accurate.
* **Visually Clear:** Rendered high-level categorical trends using clean, optimized, and proportional plots.

---

## 📊 Dataset Structure
The analysis was performed on an internal company tracking dataset (`dataset.csv`) containing the following structural layout:
* **Dimensions:** 50 rows, 7 columns
* **Attributes:** `EmployeeID`, `Name`, `Department`, `Age`, `Salary`, `Experience`, `City`

### Initial Data Quality Audit
An initial structural integrity check revealed a total of **37 missing values (NaN)** distributed across the features:
* `Department`: 5 missing entries
* `Age`: 7 missing entries
* `Salary`: 7 missing entries
* `Experience`: 10 missing entries
* `City`: 8 missing entries

---

## 🛠️ Data Cleaning & Imputation Pipeline
To preserve the overall dataset distribution characteristics and avoid losing useful rows, an explicit imputation methodology was implemented:

1. **Numerical Variables (Age, Salary, Experience):** Missing values were systematically replaced using the column **Mean** (arithmetic average). This fills in the blanks by establishing a solid baseline centered around the overall sample trends.
2. **Categorical Variables (Department, City):** Missing text fields were filled using a distinct string placeholder (`"Unknown"`). This approach ensures that incomplete entries are accounted for transparently without skewing the proportions of identified departments or cities.

*Post-cleaning validation confirmed that the absolute missing value count across all columns dropped successfully to 0.*

---

## 📉 Visual Insights & Trends
Using `matplotlib`, a proportion-accurate **Pie Chart** was built to map out employee distribution by department. 

* Including the explicitly imputed `"Unknown"` workforce segment allowed for a complete 100% distribution view.
* The visual trend clearly demonstrates that the **IT (26.0%)** and **Finance (24.0%)** departments make up the primary share of the company's workforce.

---

## 💻 Environment & Tech Stack
* **Language:** Python
* **Environment:** Jupyter Notebook / JupyterLab (VS Code)
* **Libraries Used:** NumPy, Pandas, Matplotlib
