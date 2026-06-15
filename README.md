[![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/12Shreya8/nhanes-body-measurement-analysis/blob/main/capstone(1).ipynb)

# 📊 NHANES Body Measurement Analysis

A statistical data analysis project exploring multidimensional body measurement data from the **National Health and Nutrition Examination Survey (NHANES) 2020** dataset — comparing male and female anthropometric patterns using NumPy and SciPy.

---

## 📌 Problem Statement

Understanding how body measurements differ across biological sex and how key indicators like BMI, waist-to-height ratio, and waist-to-hip ratio relate to each other is critical for population health research. This project performs a full numerical and visual analysis of NHANES 2020 data to uncover these patterns.

---

## 📊 Dataset

- **Source:** [NHANES 2020 · gagolews/teaching-data](https://github.com/gagolews/teaching-data)
- **Loaded directly via URL** — no local CSV needed
- **Features:** 7 body measurements per participant
- **Groups:** Adult males and adult females (separate datasets)

| Column | Measurement |
|---|---|
| 1 | Weight (kg) |
| 2 | Standing height (cm) |
| 3 | Upper arm length (cm) |
| 4 | Upper leg length (cm) |
| 5 | Arm circumference (cm) |
| 6 | Hip circumference (cm) |
| 7 | Waist circumference (cm) |

---

## 🔍 Analysis Pipeline

```
Load datasets via URL (male + female)
        │
        ▼
Matrix Construction (NumPy arrays)
        │
        ▼
Weight Distribution — Histograms
        │
        ▼
Weight Comparison — Boxplots
        │
        ▼
Summary Statistics (Mean, Median, Std, Skewness)
        │
        ▼
BMI Computation + Column Augmentation
        │
        ▼
Z-Score Standardisation
        │
        ▼
Correlation Analysis (Pearson + Spearman)
        │
        ▼
Scatterplot Matrix (Height, Weight, Waist, Hip, BMI)
        │
        ▼
Ratio-Based Measures (WtH + WHR)
        │
        ▼
Extreme BMI Analysis
```

---

## 📈 Key Findings

- **Male participants** have higher median body weight and greater dispersion than females
- Both distributions show **mild right skewness** — small number of high-weight individuals
- **Weight, waist, hip circumference, and BMI** are strongly positively correlated
- **Height shows weak correlation with BMI** — body girth is a stronger driver than stature
- **Waist-to-height and waist-to-hip ratios** differ notably between sexes, reflecting differences in fat distribution patterns
- Standardised z-scores reveal that individuals with extreme BMI values show consistent patterns across multiple body measurements

---

## 🛠️ Tech Stack

![Python](https://img.shields.io/badge/Python-3.10-blue?logo=python)
![NumPy](https://img.shields.io/badge/NumPy-Numerical-blue?logo=numpy)
![SciPy](https://img.shields.io/badge/SciPy-Statistics-8CAAE6?logo=scipy)
![Matplotlib](https://img.shields.io/badge/Matplotlib-Visualization-orange)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange?logo=jupyter)

- **Data:** `numpy.genfromtxt` (direct URL loading)
- **Statistics:** `scipy.stats` — skewness, z-scores, Pearson, Spearman
- **Visualization:** `matplotlib.pyplot` — histograms, boxplots, scatterplot matrix

---

## 🚀 How to Run

**Option A — Run in Colab (recommended, no setup needed):**

Click the badge at the top ↑

**Option B — Run locally:**

```bash
git clone https://github.com/12Shreya8/nhanes-body-measurement-analysis.git
cd nhanes-body-measurement-analysis
pip install numpy scipy matplotlib
jupyter notebook "capstone(1).ipynb"
```

No dataset download needed — data loads automatically from the web.

---

## 🗂️ Repository Structure

```
nhanes-body-measurement-analysis/
│
├── capstone(1).ipynb     # Full analysis notebook with outputs
└── README.md
```

---

## 🔮 Future Work

- Extend BMI computation to male participants
- Add multivariate regression to predict BMI from body measurements
- Interactive dashboard with Streamlit or Plotly
- Include additional NHANES survey years for longitudinal analysis

---

## 👩‍💻 Author

**Shreya** — CS Engineering student with a focus on AI/ML & Data Science  
[GitHub](https://github.com/12Shreya8)         · [LinkedIn](https://linkedin.com/in/shreya-yergol)
