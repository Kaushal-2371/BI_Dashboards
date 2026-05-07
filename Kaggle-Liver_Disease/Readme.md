# 🫀 Liver Disease Prediction — Exploratory Data Analysis

> Analyzing clinical biomarkers to identify patterns and risk factors associated with liver disease using the ILPD (Indian Liver Patient Dataset).
> 💟 [Kaggle Official Dataset Page](https://www.kaggle.com/datasets/shauryasrivastava01/liver-patient-dataset/data)..<br>
> 💟 [Kaggle Contribution](https://www.kaggle.com/code/kaushalsahu123/liver-patient-complete-ml-pipeline-analysis)..

---

## 📊 Dashboard Preview

<table>
  <tr>
    <td><img src="https://github.com/Kaushal-2371/BI_Dashboards/blob/main/Kaggle-Liver_Disease/Dash_pic/Patient_Analysis.png" width="400"/></td>
    <td><img src="https://github.com/Kaushal-2371/BI_Dashboards/blob/main/Kaggle-Liver_Disease/Dash_pic/Disease_Analysis.png" width="400"/></td>
    
  </tr>
</table>

---

## 📁 Dataset Overview

| Property | Details |
|---|---|
| **Source** | Kaggle — Liver Patient Dataset |
| **Records** | 583 patients |
| **Features** | 11 clinical attributes |
| **Target** | Liver Disease / No Liver Disease |
| **Origin** | North East Andhra Pradesh, India |

---

## 🧬 Feature Descriptions

| Column | Full Name | Description |
|---|---|---|
| `Age` | Age | Age of the patient |
| `Gender` | Gender | Male / Female |
| `TB` | Total Bilirubin | Bilirubin level in blood (mg/dL) |
| `DB` | Direct Bilirubin | Conjugated bilirubin (mg/dL) |
| `Alkphos` | Alkaline Phosphatase | Liver enzyme level (IU/L) |
| `Sgpt` | SGPT (ALT) | Alanine aminotransferase — liver damage marker |
| `Sgot` | SGOT (AST) | Aspartate aminotransferase — liver/heart damage marker |
| `TP` | Total Proteins | Total protein in blood (g/dL) |
| `ALB` | Albumin | Albumin protein level (g/dL) |
| `A/G Ratio` | Albumin/Globulin Ratio | Protein balance indicator |
| `Selector` | Target Label | `Liver Disease` or `No Liver Disease` |

---

## 📈 Key Statistics

- **416** patients diagnosed with Liver Disease (~71%)
- **167** patients with No Liver Disease (~29%)
- **Age range:** 4 – 90 years
- **Gender split:** Predominantly male patients

---

## 🔬 Analysis Highlights

- **Bilirubin levels** (Total & Direct) are significantly elevated in liver disease patients
- **Enzyme levels** (SGPT, SGOT, Alkaline Phosphatase) show strong positive correlation with disease
- **Albumin & A/G Ratio** tend to be lower in patients with liver disease, indicating protein synthesis impairment
- Several **duplicate records** are present in the dataset and were handled during preprocessing

---

## 📂 Project Structure

```
Kaggle-Liver_Disease/
│
├── DAX_Measures.xlsx            # All DAX measures used
│
├── Dashboard_Print.pdf          # PDF copy of Report
├── Dash_pic/                    # Images for Readme.md
│   └── Disease_Analysis.png
|   └── Patient_Analysis.png
│
├── Liver_Dashboard.pbix         # PowerBI Report File
|
├── liver_patient_dataset.csv    # Liver Dataset
└── README.md
```

---

## 📌 Notes

- The dataset contains **class imbalance** — consider oversampling (SMOTE) or weighted models for classification tasks.
- Missing values exist in the `A/G Ratio` column and were imputed with the column median.
- Duplicate rows were dropped before modeling.

---

## 📄 License

This project is for educational and research purposes. Dataset sourced from [Kaggle](https://www.kaggle.com/).

---

## 🙋 Author

**Kaushal Sahu**
[Kaggle](https://www.kaggle.com/kaushalsahu123) · [LinkedIn](https://www.linkedin.com/in/kaushal-sahu/)
