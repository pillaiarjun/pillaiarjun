# Arjun Pillai

Data scientist building end-to-end systems, from cloud pipelines to production LLM applications.
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
[![ClaimDelta](https://img.shields.io/badge/ClaimDelta-009688?style=flat&logo=googlechrome&logoColor=white)](https://app.claimdelta.com)## 

<!--
**pillaiarjun/pillaiarjun** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- 🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
-->
