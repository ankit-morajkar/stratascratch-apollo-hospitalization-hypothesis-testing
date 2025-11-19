# Apollo Hospitals: Hospitalization Cost Analysis

![Status](https://img.shields.io/badge/Status-Complete-green) ![Tools](https://img.shields.io/badge/Tools-Excel%20%7C%20Statistics-blue)

## 📌 Project Overview
Apollo Hospitals, a pioneer in private healthcare in India, seeks to improve pricing efficiency and resource allocation. This project analyzes **1,338 patient records** to answer critical business questions regarding hospitalization charges.

**Goal:** To identify which variables (Smoking, Viral Load, Severity, Region) are statistically significant predictors of healthcare costs.

## 📂 The Data
The dataset contains anonymized patient-level data including:
* **Target Variable:** Hospitalization Charges ($)
* **Predictors:** Age, Sex, Smoker Status, BMI, Region, Viral Load, Severity Level.

## 📊 Methodology
I utilized **Microsoft Excel (Data Analysis ToolPak)** to perform Descriptive and Inferential Statistics.

**1. Data Cleaning & Univariate Analysis**
* Checked for missing values and distribution shapes.
* Identified that *Hospitalization Charges* are right-skewed, requiring careful interpretation of means.

**2. Hypothesis Testing**
I performed the following statistical tests to validate cost drivers:

| Test | Variables Compared | Hypothesis ($H_0$) | Outcome |
| :--- | :--- | :--- | :--- |
| **Welch's T-Test** | Smoker vs. Charges | Means are equal | **Rejected** ($P \approx 0$) |
| **Pearson Correlation** | Viral Load vs. Charges | No relationship ($r=0$) | **Weak Correlation** ($r=0.19$) |
| **ANOVA Single Factor** | Severity vs. Charges | All group means equal | **Rejected** ($P < 0.05$) |
| **Chi-Square Test** | Region vs. Smoker | Variables are independent | **Failed to Reject** ($P > 0.05$) |

## 🔎 Key Findings

### 1. The "Smoker" Effect
Smoking is the strongest predictor of hospitalization costs.
* **Smokers:** Avg Cost $80,125
* **Non-Smokers:** Avg Cost $21,085
* **Insight:** Smokers cost the hospital **~4x more** than non-smokers.

### 2. Severity Paradox
While severity level significantly impacts costs ($P = 0.0058$), the relationship is non-linear. Surprisingly, the highest severity levels (4 & 5) showed lower average variance, potentially due to sample size limitations ($n=25$).

### 3. Regional Analysis
Smoking habits appear consistent across all four geographic regions (Southwest, Southeast, Northwest, Northeast). There is no statistical evidence to suggest one region requires higher risk premiums based on location alone.

## 💡 Recommendations
Based on the data, I recommend:
1.  **Pricing:** Implement a high-risk premium specifically for smokers.
2.  **Forecasting:** Do not rely on "Viral Load" as a financial predictor; it has low correlation with actual billed amounts.
3.  **Data Collection:** Gather more data on "Severity 4 & 5" patients to validate the cost-drop anomaly.

---
*This project was conducted for educational purposes using Stratascratch datasets.*
