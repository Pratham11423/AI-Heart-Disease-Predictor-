# CardioSense AI — Heart Disease Risk Engine

> A clinical-grade machine learning dashboard that translates raw patient data into actionable cardiovascular risk intelligence.

---

## What It Does

CardioSense AI ingests standard clinical parameters — age, cholesterol levels, resting blood pressure, chest pain type, and more — and runs them through a trained KNN classification model to output a calibrated risk probability. The result is displayed as an interactive gauge, paired with a contextual recommendation panel styled after real hospital decision-support interfaces.

This isn't a toy demo. It's built to reflect what production ML looks like in healthcare settings: clean data pipelines, serialized models, and a UI that a clinician could actually navigate.

---

## Under the Hood

**Model:** K-Nearest Neighbors (KNN) Classifier  
**Preprocessing:** StandardScaler normalization + One-Hot Encoding for categorical features  
**Output:** Binary classification (High Risk / Low Risk) with continuous probability scores  
**Visualization:** Plotly-powered gauge chart — probability rendered at a glance, not buried in a table

The pipeline is saved across three serialized artifacts (`KNN_heart.pkl`, `scaler.pkl`, `columns.pkl`), making inference stateless and fast at runtime.

---

## Feature Highlights

- Real-time risk probability gauge (0–100%)
- Patient input panel via Streamlit sidebar — no form reloads
- Recommendation card that adapts based on predicted risk tier
- Dark glassmorphism UI for a modern clinical aesthetic
- Fully deployable — no external database or API dependencies

---

## Stack

| Layer | Tool |
|---|---|
| Language | Python 3 |
| App Framework | Streamlit |
| ML Library | Scikit-learn |
| Charting | Plotly |
| Data Handling | Pandas |
| Model Persistence | Joblib |

---

## Repository Layout

```
CardioSense-AI/
│
├── app.py               # Streamlit entry point — UI + inference logic
├── KNN_heart.pkl        # Serialized KNN classifier
├── scaler.pkl           # Fitted StandardScaler
├── columns.pkl          # Expected feature schema
├── requirements.txt     # Pinned dependencies
└── README.md
```

---

## Local Setup

```bash
# 1. Clone
git clone https://github.com/YOUR_USERNAME/CardioSense-AI.git
cd CardioSense-AI

# 2. Install dependencies
pip install -r requirements.txt

# 3. Launch
streamlit run app.py
```

The app opens at `http://localhost:8501` by default.

---

## Live Demo

Deployed on Streamlit Cloud — no installation required.

**[Open Live App](https://ai-heart-disease-risk-predictor-app-ml-dashboard-01.streamlit.app)**

---

## The Problem This Addresses

Cardiovascular disease is the leading cause of death worldwide. Clinical decision-support tools that surface risk early — before symptoms become critical — can change patient outcomes. CardioSense AI is a proof-of-concept for exactly that: a fast, interpretable, ML-driven triage layer that augments clinical judgment rather than replacing it.

Key engineering themes demonstrated:

- End-to-end ML pipeline from raw features to deployed inference
- Model serialization and production-ready artifact management
- UI/UX design choices informed by real clinical workflows
- Probability calibration over binary threshold prediction

---

## Author

**Anmol Dhiman** — AI & Machine Learning Developer

Building systems at the intersection of data science and real-world impact.

---

*Found this useful? Star the repo and reach out — always open to collaboration.*
