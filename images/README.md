# 📊 Derivable Judgement: A Statistical Decision-Making Model

> **Inferential statistics on public-health records — hypothesis testing, confidence intervals, z/t/chi-square/ANOVA tests, covariance and correlation to derive judgements about factors affecting diabetes and hypertension.**

[![Python](https://img.shields.io/badge/Python-Analysis-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://www.python.org/)
[![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-F37626?style=for-the-badge&logo=jupyter&logoColor=white)](https://jupyter.org/)
[![SciPy](https://img.shields.io/badge/SciPy-Statistical%20Tests-8CAAE6?style=for-the-badge&logo=scipy&logoColor=white)](https://scipy.org/)
[![Status](https://img.shields.io/badge/Project-Completed-success?style=for-the-badge)]()

---

As a data analyst at a public health research organization, this project uses statistical techniques on a 600-record health dataset (age, weight, gender, region, smoking, exercise, BMI, blood pressure, cholesterol, glucose, diabetes, hypertension) to decide which factors significantly affect disease occurrence.

## 📁 Repository Structure

| File | Description |
|---|---|
| `Derivable_Judgement.ipynb` | Part A theory + Part B practical analysis (code, charts, interpretations) |
| `Derivable_Judgement_Theory.pdf` | Theory document with definitions, formulas and test-selection guide |
| `health_dataset.csv` | 600-record health dataset used throughout |
| `Derivable_Judgement_images` | It contains all the images related to project |
| `README.md` | This file |

## 📊 Dataset

`health_dataset.csv` — 600 rows, 15 columns: `record_id`, `age_group`, `age`, `weight`, `gender`, `region`, `smoking_status`, `exercise_frequency`, `bmi`, `blood_pressure`, `diabetes`, `hypertension`, `cholesterol_level`, `glucose_level`, `visit_date`. Generated programmatically with realistic dependencies (BMI is derived from weight and height; blood pressure, cholesterol and glucose rise with age and BMI; disease risk rises with glucose, blood pressure, age and BMI). Overall prevalence: diabetes 22.8%, hypertension 14.0%. There are no missing values.

## ✅ Tasks Covered

### Part A — Theoretical Foundation
Short conceptual notes on inferential statistics, hypothesis testing and its components, confidence intervals and critical values, p-value, Type I vs Type II errors, the z-test, t-test, chi-square test and ANOVA, covariance, and correlation. The full write-up with formulas is in the theory PDF.

### Part B1 — Formulating Hypotheses
Five hypotheses were framed (all at α = 0.05): **H1** smoking vs diabetes, **H2** blood pressure of smokers vs non-smokers, **H3** BMI of males vs females, **H4** diabetes rate across age groups, **H5** linear relationship between age and BMI.

### Part B2 — Confidence Intervals
95% t-based confidence intervals for key numeric variables, e.g. age 40.83 (39.73–41.92), weight 71.92 kg (70.85–73.00), BMI 25.33 (24.89–25.77), systolic BP 109.59 (108.73–110.44), cholesterol 176.83 (175.21–178.46) and glucose 89.34 (88.37–90.32), shown with a labelled chart. All intervals are narrow (within about ±3% of their means), so the sample means are precise estimates.

### Part B3 & B4 — Critical Values, p-values, z-test and t-test
- **H2 (Welch t-test):** mean BP smokers 110.50 vs non-smokers 109.14; t = 1.237, critical ±1.970, p = 0.2171 → **Fail to reject H₀**.
- **H3 (two-sample z-test, n large):** mean BMI male 27.34 vs female 23.23; z = 9.732, critical ±1.960, p < 0.001 → **Reject H₀**.

### Part B5 — Chi-square Test
Smoking status vs diabetes: χ² = 1.137, df = 2, critical value 5.991, p = 0.5665 → **Fail to reject H₀**. Diabetes prevalence is 24.3% among smokers, 23.3% among non-smokers and 18.8% among former smokers — differences too small to be significant.

### Part B6 — ANOVA
Diabetes rate across five age groups: F = 10.968, df = (4, 595), critical value 2.387, p < 0.001 → **Reject H₀**. Prevalence climbs from 9.8% (18-25) to 53.5% (60+).

### Part B7 — Covariance & Correlation
Covariance and correlation matrices plus a labelled heatmap for age, weight, BMI, BP, cholesterol and glucose. Age vs BMI: covariance −6.11, r = −0.081, p = 0.047 → **Reject H₀**, but the relationship is very weak (r² ≈ 0.7%). Age correlates moderately with cholesterol (0.42), BP (0.37) and glucose (0.34); weight and BMI are strongly correlated (0.85).

### Part B8 — Results & Interpretation
Every test ends with a plain-language Accept/Reject decision, and a final summary table consolidates all five judgements. **Conclusion:** age is the clearest driver of diabetes, and males have a significantly higher BMI than females. Smoking shows no significant link with diabetes or blood pressure, and age vs BMI is only very weakly correlated. These are associations in the sample, not proof of causation.

## 🛠️ How to Run

```bash
pip install pandas numpy matplotlib scipy
jupyter notebook Derivable_Judgement.ipynb
```
## 👨‍💻 Author

**Mukesh kote**

---

## ⭐ Support

Star ⭐ this repo if you like it!

---
**Derivable Judgement** · Mathematics & Advanced Statistics
