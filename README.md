# 🏠 Strategic Housing Location Classification with KNN

[![Status](https://img.shields.io/badge/Project-Completed-brightgreen)](https://github.com/Julio-analyst)
[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
![Made With](https://img.shields.io/badge/Made%20with-R-1f78b4?logo=r)
![MCC](https://img.shields.io/badge/MCC-Improved%20(0.05%20→%200.60)-blueviolet)

This project implements a K-Nearest Neighbors (KNN) classifier to predict whether a house is located in a *strategic area*, using property features from Bandar Lampung. The model uses real-world imbalanced data and applies **ROSE resampling** to improve minority class detection.

---

## 📌 Project Summary

| Feature             | Description                                  |
|---------------------|----------------------------------------------|
| Language            | R                                            |
| Algorithm           | K-Nearest Neighbors (KNN)                   |
| Dataset             | Scraped real-estate data from Bandar Lampung |
| Resampling Method   | ROSE Undersampling                          |
| Evaluation Metrics  | Accuracy, Sensitivity, Specificity, F1, MCC |

---

## 📊 Features Used

- Distance to city center (`Jarak`)
- Building area (`Luas Bangunan`)
- Land area (`Luas Tanah`)
- Electricity capacity (`Daya Listrik`)
- Number of bedrooms
- Label: `LokasiStrategis` (Yes/No)

---

## 🔄 Modeling Pipeline

1. **Data Cleaning**
   - Check for missing/duplicate values
2. **Exploratory Data Analysis (EDA)**
   - Visualizations: histogram, scatterplot, boxplot, MCC comparison
3. **Preprocessing**
   - Feature normalization with `scale()`
   - Stratified train/test split
4. **Modeling**
   - KNN with k = 1 to 10
   - Evaluation: Accuracy, F1, MCC, Sensitivity
5. **Resampling**
   - ROSE undersampling to handle class imbalance
   - Re-train and compare metrics

---

## 📈 Key Results

- ✅ **Accuracy**: 78.26% (after resampling)
- ✅ **MCC**: 0.66 (vs 0.17 before resampling)
- ✅ **Sensitivity**: ↑ from 25% to 90%
- ✅ **F1-Score**: ↑ from 0.22 to 0.66

These improvements show the importance of balancing techniques in urban planning and classification tasks with skewed datasets.

---

## 🧠 Visual Examples

| Visual | Description |
|--------|-------------|
| 📊 MCC Comparison | KNN performance with vs. without resampling |
| 🏘️ Decision Boundary | Model separation between strategic and non-strategic |
| 🧩 Accuracy by k | Accuracy for each k from 1 to 10 |

> Visuals available in `visualizations/` folder or the full poster in `POSTER_Kelompok03_KELASRB.png`

---

## 📂 Repository Structure

```bash
lokasi-rumah-knn-classifier/
├── data/
│   └── rumahbalam_kategorik_strategis.csv       # Cleaned dataset
├── scripts/
│   └── CODE_Kelompok03_KELASRB.Rmd              # Full code (R Markdown)
├── visualizations/
│   ├── histogram_boxplot.png
│   ├── mcc_comparison.png
│   ├── decision_boundary_knn.png
│   └── scatter_jarak_luas.png
├── documents/
│   ├── LAPORAN_Kelompok03_KELASRB.docx          # Final report
│   └── POSTER_Kelompok03_KELASRB.png            # Infographic
├── LICENSE                                       # MIT License
├── README.md
├── .gitignore

👥 Authors
Farrel Julio Akbar – @Julio-analyst

Juesi Apridelia Saragih

Fiodora Alysa Juandi

Haikal Fransisko Simbolon
