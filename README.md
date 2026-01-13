🎯 Objective

To develop an interpretable AI system that can:

Predict student failure risk early

Identify critical learning patterns

Support data-driven educational intervention strategies

🗂 Dataset

OULAD – Open University Learning Analytics Dataset

Includes:

Student demographics

Virtual Learning Environment (VLE) activity

Assessment and exam scores

🏗 Model Architecture
Layer	Description
Input	22 features (static + temporal)
BiLSTM	Captures bidirectional learning dynamics
Attention	Highlights critical assessment moments
BatchNorm	Stabilizes training
Dropout	Prevents overfitting
Dense (Sigmoid)	Risk probability output
📈 Results
Metric	Score
Accuracy	0.84
ROC-AUC	0.91
F1 (At-Risk)	0.79
F1 (Success)	0.87

The model successfully identifies students at risk before final failure occurs.

🔍 Explainability (XAI)

SHAP (Shapley Additive Explanations) is used for:

Global feature importance

Individual student explanation

Early vs late exam influence comparison

Transparent decision interpretation

📂 Repository Structure
CSE655_FinalProject_OULAD/
│
├── data/           # OULAD dataset files
├── notebooks/      # Training & evaluation notebooks
├── requirements.txt
├── README.md
└── .gitignore

⚙ Installation
pip install -r requirements.txt

▶ Usage

Run the main notebook:

notebooks/01_Data_Preprocessing.ipynb


Includes preprocessing, training, evaluation and SHAP explainability.

⭐ Key Contributions

Attention-based temporal modeling

Explainable student risk prediction

Interpretable educational analytics pipeline

📚 References

Lundberg & Lee (2017) – SHAP

Graves & Schmidhuber (2005) – BiLSTM

OULAD – Open University Learning Analytics Dataset
