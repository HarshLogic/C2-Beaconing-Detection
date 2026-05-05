# 🛡️ C2 Beaconing Detection & Blast Radius Analysis

![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)  
![XGBoost](https://img.shields.io/badge/XGBoost-Enabled-orange.svg)  
![NetworkX](https://img.shields.io/badge/NetworkX-Graph_Theory-lightgrey.svg)  
![Machine Learning](https://img.shields.io/badge/Machine_Learning-Scikit_Learn-yellow.svg)

An advanced, data-driven cybersecurity framework designed to detect stealthy Command and Control (C2) beaconing in network traffic and visualize threat propagation using Machine Learning and Graph Theory.

---

## 📖 Overview

Modern cyber adversaries continuously evolve, using polymorphic malware and low-and-slow C2 beaconing to bypass traditional signature-based Intrusion Detection Systems (IDS).

This project introduces a **behavioral anomaly detection approach**, analyzing subtle network deviations such as:

- Inter-arrival time (IAT) variance  
- DNS entropy  
- Communication patterns  

Beyond classification, the system implements **Breadth-First Search (BFS)** graph logic to construct an interactive **Blast Radius**, mapping lateral movement and visualizing infection spread. This provides Security Operations Center (SOC) teams with actionable threat intelligence.

---

## ✨ Key Features

- **Behavioral ML Detection**  
  Uses XGBoost and Random Forest ensemble models to classify malicious traffic and generate risk scores.

- **Graph-Based Visualization**  
  NetworkX-powered topology mapping with color-coded nodes:
  - 🔴 Primary infected node  
  - 🟠 Tier 1 (direct connections)  
  - 🟡 Tier 2 (lateral movement risks)

- **Automated Data Pipeline**  
  - Median imputation  
  - Noise filtering (multicast/broadcast removal)  
  - MinMax scaling  

- **Dimensionality Reduction**  
  PCA transforms high-dimensional telemetry into 2D space for cluster visualization.

---

## 📊 Dataset & Model Performance

- Synthetic dataset: **25,000 network flows**  
- ~10% malicious (simulated botnet traffic)

### Model Results

| Model | Accuracy | Precision | Recall | F1-Score | Log Loss |
|------|---------|----------|--------|---------|---------|
| SVC | 83.00% | 89.69% | 78.38% | 83.65% | 0.3542 |
| Random Forest | 88.50% | 92.31% | 86.49% | 89.30% | 0.2810 |
| **XGBoost** | **89.50%** | **93.27%** | **87.39%** | **90.23%** | **0.2588** |

> XGBoost also achieved the lowest regression errors (MSE, RMSE, MAE) for risk scoring.

---

## 🚀 Getting Started

### Prerequisites

Ensure Python 3.8+ is installed.

```bash
pip install pandas numpy scikit-learn matplotlib seaborn networkx xgboost

```
### 🤝 Contributing

Contributions, issues, and feature requests are welcome.
Feel free to open a pull request or raise an issue.

### 📄 License

This project is licensed under the MIT License.
