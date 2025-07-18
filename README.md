# Edge vs Cloud: Can AI Agent Deployment Be Predicted?

This project explores whether the deployment environment of an autonomous AI agent (Edge or Cloud) can be predicted based on its performance metrics, architecture, and task types. The dataset used is a 2025-ready collection featuring over 4,000 AI agents with rich features including multimodal capabilities, latency, execution performance, and bias detection.

---

## Project Objective

> **Can we predict if an AI agent will be deployed on the edge or in the cloud using its performance characteristics and architecture type?**

---

## Model Pipeline

- **Preprocessing:**
  - Categorical Encoding (`OneHotEncoder`)
  - Numeric Scaling (`StandardScaler`)
  - Boolean conversion (`TRUE`/`FALSE` → `1`/`0`)
- **Model:**
  - `RandomForestClassifier`
  - Tuned with `GridSearchCV`
- **Evaluation:**
  - Confusion Matrix
  - Classification Report
  - Feature Importance Analysis

---

## Results

| Metric       | Score |
|--------------|-------|
| Accuracy     | 80.6% |
| Precision (Edge) | 95% |
| Recall (Edge)    | 66% |
| F1 Score (Edge)  | 78% |

 **Conclusion**: The model is very good at confidently detecting Edge agents, but slightly conservative (some edge agents are misclassified as cloud).

---

## Files in This Repo

| File                        | Description                            |
|-----------------------------|----------------------------------------|
| `edge_vs_cloud_classifier.py` | Main ML pipeline script               |
| `ai_agent_dataset.csv`      | AI agent performance dataset (if small)|
| `requirements.txt`          | Python dependencies                    |
| `README.md`                 | Project overview                       |

---

## Installation

```bash
pip install -r requirements.txt
python edge_vs_cloud_classifier.py
