CSE655 Final Project – Explainable Student Risk Prediction (OULAD)
Project Overview

This project presents an explainable deep learning system for predicting student academic risk using the Open University Learning Analytics Dataset (OULAD).
The main objective is to identify students who are likely to fail or withdraw early in the semester and to provide transparent explanations for each prediction.

The system combines Bidirectional LSTM networks with an Attention mechanism and SHAP-based explainability to create an interpretable and reliable educational risk prediction framework.

Motivation

Early identification of at-risk students enables timely academic intervention and academic success improvement.
However, most deep learning models operate as black boxes and do not provide explanations for their predictions.

This project focuses on:

• Accurate early risk prediction
• Explainable artificial intelligence
• Transparent and trustworthy decision support systems

Dataset

The Open University Learning Analytics Dataset (OULAD) is used in this project.
It contains demographic features, virtual learning environment interactions, assessment results, and final academic outcomes.

Target labels:

Label	Meaning
1	Success (Pass / Distinction)
0	At-Risk (Fail / Withdraw)
Model Architecture

The prediction model is based on:

Bidirectional LSTM layers

Custom Attention layer

Batch Normalization

Dropout regularization

Sigmoid output layer

The attention mechanism enables the model to focus on the most influential temporal assessment moments.

Explainability

SHAP (SHapley Additive Explanations) is used to explain model predictions.
This allows:

• Feature importance analysis
• Individual student explanation
• Early vs late exam importance comparison
• Transparent decision interpretation

Results
Metric	Score
Accuracy	0.84
ROC-AUC	0.91
F1 (At-Risk)	0.79
F1 (Success)	0.87
Repository Structure
CSE655_FinalProject_OULAD/
│
├── data/
├── notebooks/
├── requirements.txt
├── README.md
└── .gitignore

Installation
pip install -r requirements.txt

Usage

Open and run:

notebooks/01_Data_Preprocessing.ipynb


This notebook includes preprocessing, training, evaluation, and explainability steps.

Key Contributions

Attention-based temporal modeling

Explainable student risk prediction

Interpretable educational analytics pipeline

References

Lundberg & Lee (2017) – SHAP
Graves & Schmidhuber (2005) – Bidirectional LSTM
OULAD Dataset – Open University Learning Analytics Dataset
