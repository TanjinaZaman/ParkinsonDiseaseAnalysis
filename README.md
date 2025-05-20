# ParkinsonDiseaseAnalysis

# Parkinson’s Disease Voice Dataset Overview

This repository documents the structure and characteristics of a biomedical dataset used for **Parkinson’s disease classification** based on voice recordings. The dataset contains rich voice signal features and serves as a benchmark for developing and evaluating machine learning models.

---

## 📊 Dataset Summary

- **Samples**: 756 individual voice recordings  
- **Features**: 755 total columns  
  - 753 input features  
  - 1 target column (`class`)  
  - 1 identifier (`id`)

---

## 🧬 Data Composition

### 🧠 Target Column

- **`class`**  
  - `1` = Parkinson’s Disease  
  - `0` = Healthy  
  - Parkinson’s patients comprise ~74.6% of the dataset

### 🔣 Feature Types

- **Numerical Features**: Most features (float64)
- **Categorical/ID Features**: `id`, `gender`, `class` (int64)

### 🧑 Demographics
- **`gender`**: 0 = Female, 1 = Male  
- **`id`**: Unique identifier for each recording

---

## 🧪 Biomedical Voice Measurements

These features reflect pitch irregularity, signal complexity, and vocal fold health — crucial for Parkinson's detection.

| Feature               | Description |
|-----------------------|-------------|
| `PPE`                | Pitch Period Entropy — higher in Parkinson’s due to irregular pitch |
| `DFA`                | Detrended Fluctuation Analysis — reflects signal complexity |
| `RPDE`               | Recurrence Period Density Entropy — measures signal unpredictability |
| `numPulses`          | Count of vocal fold pulses |
| `meanPeriodPulses`   | Avg time between pulses |
| `stdDevPeriodPulses` | Std deviation in pulse period — higher in unstable voices |
| `locPctJitter`       | Pitch variation between cycles — elevated in Parkinson’s |

---

## 🧵 Feature Groups

| Group Name                       | Feature Count |
|----------------------------------|---------------|
| Wavelet Energy & Entropy         | 432           |
| Deterministic / Approx Entropy   | 180           |
| MFCC & Log Energy Features       | 82            |
| Traditional Voice Measures       | 17            |
| VFER / IMF Features              | 13            |
| Formants & Bandwidths            | 8             |
| Misc / Other                     | 7             |
| Glottal & Harmonicity Features   | 6             |
| GNE Features                     | 6             |
| Demographics                     | 2             |
| Higher-Order Energy Features     | 2             |

---

## 🔍 Subgroup Summaries

### 🔸 Deterministic & Approximate Entropy

| Subgroup              | Feature Count |
|----------------------|----------------|
| Det_Entropy_Shannon  | 20 |
| Det_Entropy_Log      | 20 |
| Det_TKEO_Mean        | 20 |
| Det_TKEO_Std         | 20 |
| App_Entropy_Shannon  | 20 |
| App_Entropy_Log      | 20 |
| App_TKEO_Mean        | 20 |
| App_TKEO_Std         | 20 |
| Ed_Coef              | 10 |
| Ed2_Coef             | 10 |

### 🔸 TQWT (Wavelet-Based Features)

| Subgroup                 | Feature Count |
|--------------------------|---------------|
| TQWT_Energy              | 36 |
| TQWT_Entropy_Shannon     | 36 |
| TQWT_Entropy_Log         | 36 |
| TQWT_TKEO_Mean           | 36 |
| TQWT_TKEO_Std            | 36 |
| TQWT_Stat_Median         | 36 |
| TQWT_Stat_Mean           | 36 |
| TQWT_Stat_Std            | 36 |
| TQWT_Stat_Min            | 36 |
| TQWT_Stat_Max            | 36 |
| TQWT_Stat_Skewness       | 36 |
| TQWT_Stat_Kurtosis       | 36 |

### 🔸 MFCC & Log Energy Features

| Subgroup           | Feature Count |
|--------------------|---------------|
| MFCC_Delta_Mean    | 25 |
| MFCC_Delta_Std     | 25 |
| MFCC_Mean          | 13 |
| MFCC_Std           | 13 |
| Log_Energy_Mean    | 1  |
| Log_Energy_Std     | 1  |

---

## 📉 Dimensionality Reduction

- **Original features**: 753 input features  
- **Reduced features**: 93 (after selection for modeling)

---

## 📌 Usage Notes

This dataset is ideal for:
- Feature selection and dimensionality reduction research
- Binary classification tasks (Parkinson's vs Healthy)
- Testing ensemble and deep learning models on imbalanced datasets

---

## 📎 License

Usage of this dataset should respect original data sources (UCI repository or associated publication if applicable).

---

