# 🛡️ IoT Network Intrusion and Anomaly Detection Pipeline

This project implements an end-to-end Machine Learning pipeline to detect cyber attacks and anomalous network traffic in IoT (Internet of Things) environments. 

Developed as a preliminary research and data analysis project for Senior Capstone preparation.

---

## 📌 Problem & Motivation
IoT devices typically have constrained computational resources, making them prime targets for malicious network activity (e.g., DDoS, injection attacks). This project aims to analyze network telemetry patterns and deploy a lightweight, highly accurate machine learning model to classify normal vs. malicious traffic in real time.

---

## 📊 Dataset Attribution
•⁠  ⁠*Dataset:* IoT Telemetry & Intrusion Detection Dataset
•⁠  ⁠*Source:* Mendeley Data (Academic Open Repository)
•⁠  ⁠*Structure:* ~405,000 network/sensor records with balanced binary labels (Normal: ⁠ 0 ⁠, Attack: ⁠ 1 ⁠).

---

## 🔍 Exploratory Data Analysis (EDA)

### 1. Class Distribution
The dataset is balanced, ensuring unbiased training across both normal and attack scenarios.

![Class Distribution](trafik_dagilimi.png)

### 2. Feature Correlations
Analysis of sensor readings and network metrics to understand inter-variable dependencies and indicators of malicious activity.

![Correlation Heatmap](korelasyon_haritasi.png)

---

## ⚙️ Methodology & Architecture

1.⁠ ⁠*Preprocessing:* Feature selection on numerical network and telemetry metrics, drop zero-variance/redundant indicators.
2.⁠ ⁠*Train/Test Split:* Stratified 80/20 split (⁠ stratify=y ⁠) ensuring balanced class ratios in evaluation.
3.⁠ ⁠*Model:* ⁠ RandomForestClassifier ⁠ (100 estimators) trained with parallel processing (⁠ n_jobs=-1 ⁠).

---

## 📈 Evaluation & Results

The model achieved exceptional classification performance on the unseen test set (81,037 samples):

| Metric | Normal (0) | Attack (1) | Overall |
| :--- | :--- | :--- | :--- |
| *Precision* | 1.00 | 1.00 | 1.00 |
| *Recall* | 1.00 | 1.00 | 1.00 |
| *F1-Score* | 1.00 | 1.00 | 1.00 |
| *Accuracy* | - | - | *100%* |

### Confusion Matrix
The confusion matrix verifies virtually zero false-positives and false-negatives across over 81,000 test cases:

![Confusion Matrix](confusion_matrix.png)

---

## 🛠️ Tech Stack
•⁠  ⁠*Language:* Python 3.x
•⁠  ⁠*Environment:* Google Colab
•⁠  ⁠*Libraries:* Pandas, NumPy, Matplotlib, Seaborn, Scikit-Learn

---

## 👥 Contributors
•⁠  ⁠Afra Ordulu
•⁠  ⁠Nilüfer Öden
