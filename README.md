# Arjun Pillai

AI Engineer at Hexaware Technologies in Jersey City. I build LLM products end to end: data pipelines, model selection, prompt and evaluation design, and the application on top. Most of my own work is in healthcare and public-interest domains, where a wrong answer can cost someone money or care.

B.A. Data Science, UC Berkeley. Databricks Certified Data Engineer Associate and Generative AI Engineer Associate.

![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)
![PySpark](https://img.shields.io/badge/PySpark-E25A1C?style=flat&logo=apachespark&logoColor=white)
![SQL](https://img.shields.io/badge/SQL-4479A1?style=flat&logo=postgresql&logoColor=white)
![Databricks](https://img.shields.io/badge/Databricks-FF3621?style=flat&logo=databricks&logoColor=white)
![Azure](https://img.shields.io/badge/Azure-0078D4?style=flat&logo=microsoftazure&logoColor=white)
![MLflow](https://img.shields.io/badge/MLflow-0194E2?style=flat&logo=mlflow&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat&logo=fastapi&logoColor=white)
![React](https://img.shields.io/badge/React-20232A?style=flat&logo=react&logoColor=61DAFB)

---

## Projects

### RuralWatch — [github.com/pillaiarjun/ruralwatch](https://github.com/pillaiarjun/ruralwatch)

Predicts which rural US hospitals are at risk of financial distress or closure within one to three years, using public CMS cost report data. Built in response to a December 2025 systematic review in BMC Health Services Research, which examined every published study of rural hospital closures from 2013 to 2024 and found that no ML early-warning system existed. Over 140 rural hospitals have closed since 2010. Every prediction comes with a SHAP waterfall showing which financial ratios drove the score, so a state health department could audit it.

- Bronze, Silver, and Gold Delta Lake pipeline in PySpark, with a star schema in the Gold layer
- 10 engineered financial ratios from CMS cost reports (2011 to 2022), joined with USDA rural codes and the UNC Sheps closure registry
- XGBoost with SMOTE and a temporal train/test split; validation ROC-AUC 0.8789
- Kafka producer and consumer simulating quarterly CMS updates
- FastAPI endpoint and Streamlit risk dashboard

`PySpark` `Delta Lake` `XGBoost` `MLflow` `SHAP` `Kafka` `FastAPI` `Streamlit`

### RecidivAI — [github.com/pillaiarjun/recidivai](https://github.com/pillaiarjun/recidivai)

Transparent, auditable recidivism risk model on the ProPublica COMPAS dataset. ProPublica's 2016 investigation found that a widely used black-box algorithm was twice as likely to wrongly flag Black defendants as high risk. This project is the auditable alternative: every prediction includes a SHAP explanation of which features moved the score and by how much, alongside a fairness analysis across racial groups and a discussion of the Chouldechova impossibility result.

- Bronze, Silver, and Gold Delta Lake pipeline in PySpark
- Logistic regression, random forest, and gradient boosting, tracked and versioned in MLflow
- SHAP LinearExplainer for per-prediction explanations
- FastAPI endpoint and Streamlit dashboard

`PySpark` `Delta Lake` `MLflow` `SHAP` `Scikit-learn` `FastAPI` `Streamlit`

### Block Watch — [github.com/pillaiarjun/Blockwatch](https://github.com/pillaiarjun/Blockwatch)

Point it at one NYC DOT traffic camera and it tells you, in plain English, what is happening on that block right now. An object detection model counts vehicles and pedestrians in each frame, the app keeps a minute-by-minute history of those counts, and Gemini narrates the trend once a minute on a live dashboard. Built at AI Tinkerers NYC Vision Hack v.2.

`Python` `Flask` `Gemini` `Object detection`

### Vet Benefits Help (private, pre-launch)

Free tool that helps U.S. veterans, especially those with less-than-honorable discharges, understand which of roughly 50 federal VA benefit programs they may qualify for and what to do next. Instead of a binary eligibility verdict, which only the VA can give, it returns probabilistic scoring, a plain-English narrative grounded in published VA policy, and personalized next steps. The character-of-discharge scorer is calibrated through a Databricks pipeline with model weights in MLflow. The repo stays private until VA validation and accredited-attorney legal review are complete.

`Python` `FastAPI` `React` `PostgreSQL` `Databricks` `MLflow` `Claude API`

---

## Connect

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=flat&logo=linkedin&logoColor=white)](https://linkedin.com/in/arjunpillai008)
[![Email](https://img.shields.io/badge/Email-EA4335?style=flat&logo=gmail&logoColor=white)](mailto:arjun.pillai@berkeley.edu)
