# Production-Grade Breast Cancer Prediction Pipeline

[![Python](https://img.shields.io/badge/Python-3.10%2B-blue.svg)](https://www.python.org/)
[![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-1.2%2B-orange.svg)](https://scikit-learn.org/)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)
[![SDG 3](https://img.shields.io/badge/SDG-3%20Good%20Health%20%26%20Well--Being-E5243B.svg)](https://sdgs.un.org/goals/goal3)

An end-to-end, leak-free Machine Learning classification pipeline developed for the **AICTE | IBM SkillsBuild Machine Learning & Applied AI Internship 2026**.

---

## 📌 Project Overview

Early and accurate diagnosis of breast cancer is critical for improving patient outcomes. This project provides an enterprise-ready, object-oriented Machine Learning pipeline that classifies fine-needle aspirate (FNA) digitized cell nuclear features as either **Malignant (0)** or **Benign (1)**.

Built around **Sustainable Development Goal 3 (Good Health and Well-being)**, the pipeline emphasizes diagnostic rigor, data leakage prevention, model explainability, and reproducible software engineering standards.

### Key Highlights
- **Object-Oriented Lifecycle:** Encapsulated inside `BreastCancerPipeline` to maintain state across execution phases.
- **Data Leakage Mitigation:** Preprocessing (`StandardScaler`) is encapsulated within `sklearn.pipeline.Pipeline` objects to prevent information leakage across cross-validation folds.
- **Unbiased Evaluation:** Employs nested cross-validation (5 outer folds, 3 inner folds) to eliminate hyperparameter optimization bias.
- **Explainable AI (XAI):** Implements Permutation Feature Importance for transparent feature attribution.
- **Automated Artifact Export:** Exports model binaries (`.joblib`), standardized metric logs (`.json`), and run logs (`.log`).

---

## 📊 Dataset

The project utilizes the **Wisconsin Breast Cancer Diagnostic Dataset** loaded directly via `sklearn.datasets`:
- **Instances:** 569 samples (212 Malignant, 357 Benign)
- **Features:** 30 numeric cell nucleus characteristics (radius, texture, perimeter, area, smoothness, etc.)
- **Class Balance:** 62.7% Benign, 37.3% Malignant

---

## 🛠️ Repository Structure

```text
.
├── Breast_Cancer_ML_Pipeline.ipynb   # Main Google Colab / Jupyter Notebook
├── breast_cancer_model.joblib        # Serialized trained model pipeline artifact
├── breast_cancer_report.json         # Standardized evaluation metrics report
├── pipeline.log                      # Complete execution logs
├── Concept_Note.pdf                  # Internship Concept Note & Lean Canvas
└── README.md                         # Project documentation
