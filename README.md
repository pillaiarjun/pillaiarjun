# Arjun Pillai

Data scientist building end-to-end systems — from cloud pipelines to production LLM applications.
B.A. Data Science, UC Berkeley · U.S. Permanent Resident

![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)
![PySpark](https://img.shields.io/badge/PySpark-E25A1C?style=flat&logo=apachespark&logoColor=white)
![SQL](https://img.shields.io/badge/SQL-4479A1?style=flat&logo=postgresql&logoColor=white)
![AWS](https://img.shields.io/badge/AWS-232F3E?style=flat&logo=amazonaws&logoColor=white)
![Databricks](https://img.shields.io/badge/Databricks-FF3621?style=flat&logo=databricks&logoColor=white)
![Snowflake](https://img.shields.io/badge/Snowflake-29B5E8?style=flat&logo=snowflake&logoColor=white)
![MLflow](https://img.shields.io/badge/MLflow-0194E2?style=flat&logo=mlflow&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat&logo=fastapi&logoColor=white)

---

## Featured projects

### 🏥 ClaimDelta — [app.claimdelta.com](https://app.claimdelta.com)

HIPAA-compliant B2B SaaS platform that automates detection and recovery of payer underpayments for independent medical practices. Targets a $150K–$360K annual revenue leak caused by insurers underpaying on contracted rates — a problem most practices never detect because they lack the tooling to audit every claim against their contract.

Built the full stack from scratch:
- **Parser**: Deterministic X12 835 ERA parser handling three major clearinghouse dialects (Availity, Waystar, Change Healthcare)
- **AI layer**: LLM-powered extraction of payer contract fee schedules, joined against ERA data to generate ranked underpayment worklists
- **Backend**: FastAPI + PostgreSQL on AWS (S3, RDS, EC2) with end-to-end HIPAA compliance — encryption at rest, IAM isolation, automated PHI deletion
- **Frontend**: React SPA with Stripe billing and SendGrid magic-link authentication

`Python` `FastAPI` `PostgreSQL` `React` `AWS` `Stripe` `LLM` `HIPAA`

---

### 🏨 RuralWatch — [github.com/pillaiarjun/ruralwatch](https://github.com/pillaiarjun/ruralwatch)

End-to-end ML pipeline that predicts which rural US hospitals are at risk of financial distress or permanent closure within 1–3 years, using publicly available CMS cost report data. Built in direct response to a December 2025 systematic review in BMC Health Services Research that examined every published study of rural hospital closures from 2013–2024 and explicitly called for an AI-driven early warning system — finding that no such system yet existed.

Over 140 rural hospitals have permanently closed since 2010. RuralWatch makes every prediction auditable: each at-risk hospital gets a SHAP waterfall explanation showing which financial ratios drove its risk score, transparent enough for state health department use.

Architecture:
- **Data**: Bronze → Silver → Gold Medallion pipeline in Delta Lake via PySpark; star schema (fact + 4 dimension tables) in Gold layer
- **Features**: 10 engineered financial ratios from CMS cost reports (2011–2022), joined with USDA rural codes and UNC Sheps closure registry
- **Model**: XGBoost with SMOTE and temporal train/test split — Val ROC-AUC 0.8789
- **Streaming**: Kafka producer/consumer simulating quarterly CMS updates
- **Serving**: FastAPI endpoint + Streamlit risk monitor dashboard

`PySpark` `Delta Lake` `XGBoost` `MLflow` `SHAP` `Kafka` `FastAPI` `Streamlit`

---

### ⚖️ RecidivAI — [github.com/pillaiarjun/recidivai](https://github.com/pillaiarjun/recidivai)

Transparent, auditable ML pipeline for violent recidivism risk prediction built on the ProPublica COMPAS dataset. A direct response to ProPublica's 2016 investigation finding that a widely-used black-box algorithm was twice as likely to incorrectly flag Black defendants as high-risk.

Every prediction includes a SHAP waterfall explanation showing exactly which features drove the score and by how much. Includes explicit fairness analysis across racial groups and a discussion of the Chouldechova impossibility result.

Architecture:
- **Data**: Bronze → Silver → Gold Medallion pipeline in Delta Lake via PySpark
- **Models**: Logistic Regression, Random Forest, GBM — tracked and versioned in MLflow
- **Explainability**: SHAP LinearExplainer for per-prediction transparency
- **Serving**: FastAPI REST endpoint + Streamlit dashboard

`PySpark` `Delta Lake` `MLflow` `SHAP` `Scikit-learn` `FastAPI` `Streamlit`

---

## Connect

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=flat&logo=linkedin&logoColor=white)](https://linkedin.com/in/arjunpillai008)
[![Email](https://img.shields.io/badge/Email-EA4335?style=flat&logo=gmail&logoColor=white)](mailto:arjun.pillai@berkeley.edu)
[![ClaimDelta](https://img.shields.io/badge/ClaimDelta-009688?style=flat&logo=googlechrome&logoColor=white)](https://app.claimdelta.com)
