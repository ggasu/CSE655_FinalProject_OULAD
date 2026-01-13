# 🎓 Explainable Student Risk Prediction (OULAD)

**CSE655 – Deep Learning Final Project**  
**Author:** Gamze Suiçmez  

This project presents an **explainable deep learning system** that predicts whether a student is *at-risk* or *successful* by analyzing demographic data, virtual learning behavior, and temporal exam performance.  
The goal is to enable **early, transparent, and data-driven academic intervention**.

---

## 📊 Dataset

The model is built on the **OULAD – Open University Learning Analytics Dataset**, which includes:

• Student demographics  
• Virtual Learning Environment (VLE) activity  
• Assessment and exam scores  

---

## 🧠 Model

The architecture is an **Attention-based Bidirectional LSTM** designed to capture learning behavior over time.

| Component | Description |
|----------|-------------|
| Input | 22 features (static + temporal) |
| BiLSTM | Captures learning dynamics |
| Attention | Focuses on critical exam periods |
| BatchNorm + Dropout | Training stabilization & regularization |
| Dense (Sigmoid) | Risk probability output |

---

## 📈 Performance

| Metric | Score |
|-------|------|
| Accuracy | **0.84** |
| ROC-AUC | **0.91** |
| F1 (At-Risk) | **0.79** |
| F1 (Success) | **0.87** |

The model successfully identifies students at risk **before final failure occurs**.

---

## 🔍 Explainability

Model decisions are interpreted using **SHAP (Shapley Additive Explanations)**, providing:

• Global feature importance  
• Individual student explanations  
• Early vs late exam influence analysis  
• Transparent decision reasoning  

---

## 📂 Repository Structure

```text
CSE655_FinalProject_OULAD/
│
├── data/        # OULAD dataset files
├── notebooks/   # Training & evaluation notebooks
├── requirements.txt
├── README.md
└── .gitignore

---

## 🗂 File Descriptions

| File / Folder | Description |
|---------------|------------|
| data/ | OULAD dataset files |
| notebooks/01_Data_Preprocessing.ipynb | Main training & evaluation notebook |
| requirements.txt | Required Python libraries |
| README.md | Project documentation |

---

## 🖥 Hardware Requirements

• CPU is sufficient  
• GPU is recommended but not mandatory  
• Minimum RAM: 8 GB  

---

## 🚀 Training & Inference Steps

1. Install dependencies:
pip install -r requirements.txt

2. Download the dataset and place into `data/`

3. Run:
notebooks/01_Data_Preprocessing.ipynb

This notebook performs preprocessing, training, evaluation, and SHAP explainability.


