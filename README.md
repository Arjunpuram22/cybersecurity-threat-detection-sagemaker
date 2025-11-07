# 🛡️ Cybersecurity Threat Detection System using Amazon SageMaker

An end-to-end **machine learning pipeline** that detects cybersecurity threats from network traffic data using **Amazon SageMaker**.  
This project covers the entire lifecycle — from **data preprocessing** to **automated retraining** with **SageMaker Pipelines** and **EventBridge**.

---

## 🚀 Highlights
- Achieved **95%+ accuracy** using **XGBoost** on the UNSW-NB15 dataset  
- Fully automated **ML workflow** using SageMaker Pipelines  
- Real-time **threat detection endpoint** deployed on SageMaker  
- **EventBridge automation** for scheduled retraining  
- Clean, modular repo with Jupyter notebooks and result screenshots  

---
---

## 🧱 Architecture Diagram

The following diagram illustrates the end-to-end **Cybersecurity Threat Detection Pipeline** built on AWS:

![Cybersecurity Threat Detection Pipeline](screenshots/architecture2.png)

**Workflow Summary:**
1. **Amazon S3** – Collects raw network logs.  
2. **AWS Lambda** – Processes and transforms logs into structured datasets.  
3. **Amazon S3** – Stores the processed dataset.  
4. **Amazon SageMaker** – Trains the XGBoost model using pipelines.  
5. **AWS IAM** – Manages access and permissions.  
6. **Amazon CloudWatch** – Logs metrics and monitors endpoint activity.  
7. **SageMaker Endpoint** – Deployed model for real-time threat detection.  

---
---

## ⚙️ Project Phases

This project was developed in **four main phases**, following a complete ML lifecycle using **Amazon SageMaker**.

---

### 🧹 Phase 1 — Data Preprocessing
**Notebook:** `notebooks/data_preprocessing.ipynb`

- Loaded the **UNSW-NB15 dataset** from S3.
- Cleaned missing data and removed unnecessary columns.
- Encoded categorical variables and normalized numerical features.
- Saved processed dataset back to S3 for training.

**Output Location (S3):**
