# 📊 Derivable Judgement: A Statistical Decision-Making Model

> **Inferential statistics on public-health records — hypothesis testing, confidence intervals, z/t/chi-square/ANOVA tests, covariance and correlation to derive judgements about factors affecting diabetes and hypertension.**

[![Python](https://img.shields.io/badge/Python-Analysis-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://www.python.org/)
[![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-F37626?style=for-the-badge&logo=jupyter&logoColor=white)](https://jupyter.org/)
[![SciPy](https://img.shields.io/badge/SciPy-Statistical%20Tests-8CAAE6?style=for-the-badge&logo=scipy&logoColor=white)](https://scipy.org/)
[![Status](https://img.shields.io/badge/Project-Completed-success?style=for-the-badge)]()

---

As a data analyst at a public health research organization, this project uses statistical techniques on a 500-record health dataset (age, weight, gender, region, smoking, exercise, BMI, blood pressure, cholesterol, glucose, diabetes, hypertension) to decide which factors significantly affect disease occurrence.

## 📁 Repository Structure

| File | Description |
|---|---|
| `Derivable_Judgement.ipynb` | Part A theory + Part B practical analysis (code, charts, interpretations) |
| `Derivable_Judgement_Theory.pdf` | Theory document with definitions, formulas and test-selection guide |
| `health_dataset.csv` | 500-record health dataset used throughout |
| `Derivable_Judgement_images` | It contains all the images related to project |
| `README.md` | This file |

## 📊 Dataset

`health_dataset.csv` — 500 rows, 15 columns: `record_id`, `age_group`, `age`, `weight`, `gender`, `region`, `smoking_status`, `exercise_frequency`, `bmi`, `blood_pressure`, `diabetes`, `hypertension`, `cholesterol_level`, `glucose_level`, `visit_date`. Generated programmatically with realistic dependencies (disease risk rises with age, BMI and smoking). Overall prevalence: diabetes 21.8%, hypertension 15.0%.

## ✅ Tasks Covered

### Part A — Theoretical Foundation
Short conceptual notes on inferential statistics, hypothesis testing and its components, confidence intervals and critical values, p-value, Type I vs Type II errors, the z-test, t-test, chi-square test and ANOVA, covariance, and correlation. The full write-up with formulas is in the theory PDF.

### Part B1 — Formulating Hypotheses
Five hypotheses were framed (all at α = 0.05): **H1** smoking vs diabetes, **H2** blood pressure of smokers vs non-smokers, **H3** BMI of males vs females, **H4** diabetes rate across age groups, **H5** linear relationship between age and BMI.

### Part B2 — Confidence Intervals
95% t-based confidence intervals for key numeric variables, e.g. age 40.40 (39.16–41.64), weight 71.83 kg (70.68–72.98), BMI 25.11 (24.71–25.51), systolic BP 109.55 (108.60–110.51), cholesterol 177.09 (174.92–179.27) and glucose 89.47 (88.32–90.62), shown with a labelled chart.

### Part B3 & B4 — Critical Values, p-values, z-test and t-test
- **H2 (Welch t-test):** mean BP smokers 111.76 vs non-smokers 108.66; t = 2.557, critical ±1.971, p = 0.0112 → **Reject H₀**.
- **H3 (two-sample z-test, n large):** mean BMI male 25.51 vs female 24.82; z = 1.696, critical ±1.960, p = 0.0899 → **Fail to reject H₀**.

### Part B5 — Chi-square Test
Smoking status vs diabetes: χ² = 12.337, df = 2, critical value 5.991, p = 0.0021 → **Reject H₀**. Diabetes prevalence is 33.3% among smokers vs 18.3% among non-smokers.

### Part B6 — ANOVA
Diabetes rate across five age groups: F = 8.163, df = (4, 495), critical value 2.390, p < 0.001 → **Reject H₀**. Prevalence climbs from 6.6% (18-25) to 44.2% (60+).

### Part B7 — Covariance & Correlation
Covariance and correlation matrices plus a labelled heatmap for age, weight, BMI, BP, cholesterol and glucose. Age vs BMI: covariance 4.63, r = 0.073, p = 0.104 → **Fail to reject H₀** (no significant linear relationship).

### Part B8 — Results & Interpretation
Every test ends with a plain-language Accept/Reject decision, and a final summary table consolidates all five judgements. **Conclusion:** smoking and age are the clearest drivers of disease occurrence; gender shows no significant BMI difference.

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
