# 🛡️ Financial Fraud Analysis: Behavioral Patterns & ML Detection

### 📌 Project Overview
This project provides a comprehensive analysis of fraudulent behavior within a dataset of **7.5 million financial transactions**. The goal is to move beyond simple detection and understand the specific strategies used by fraud cells.

---

### ⚙️ Technical Implementation
* **Memory Management:** To handle 7.5M records on a local machine (working directory: `transactions_project`), the pipeline uses chunk-based processing.
* **Optimization:** Data is serialized into **Apache Parquet** format, reducing loading times from minutes to seconds while preserving data types.
* **Automation:** Integrated with the **Kaggle API** for seamless data ingestion and reproducibility.

---

### 📊 Machine Learning & Insights
* **Model:** An **XGBoost** classifier achieving a stable **89.3% Recall**, ensuring high sensitivity to fraudulent events.
* **Explainability:** **SHAP** values are used to interpret model decisions, highlighting "distance from home" and "transaction velocity" as top risk factors.
* **Behavioral Clustering:** Applied **K-Means** to segment detected fraud into "Criminal Personas." This revealed a specific cluster of **Local Fraud** (high-value attacks occurring near the victim's home), suggesting skimming or social engineering.

---

### 🧪 Key Features Engineered
1. **Geographical Velocity:** Unique countries visited per hour to detect automated account takeovers.
2. **Economic Normalization:** All amounts converted to **USD** for consistent behavioral analysis across regions.
3. **Activity Bursts:** Detection of high-frequency transaction windows (velocity) typical for bot-driven attacks.

---
*Developed as part of a fraud detection research series.*
