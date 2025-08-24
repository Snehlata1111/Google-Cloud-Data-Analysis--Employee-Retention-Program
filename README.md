# GCP Churn Analysis

## Overview
This project performs **employee churn analysis** using Google Cloud Platform (GCP) services. Employee churn (attrition) can have a significant impact on an organization’s productivity and costs. This project aims to predict which employees are likely to leave the company, understand key factors influencing churn, and provide actionable insights to HR teams.  

The project encompasses **data extraction, preprocessing, exploratory data analysis (EDA), feature engineering, machine learning model training, evaluation, and visualization**. It is designed to be modular, reproducible, and scalable using GCP services.

## Project Objectives
- Predict employee churn using historical HR data.  
- Identify key factors influencing employee attrition.  
- Provide actionable insights for HR decision-making.  
- Demonstrate integration of Python-based machine learning pipelines with GCP services like BigQuery.  
- Maintain a reproducible workflow with clear documentation and reporting.

## Data Source
Datasets are stored in **Google BigQuery**:  

- `tbl_hr_data`: Historical employee data including features like satisfaction level, last evaluation, number of projects, time spent at the company, average monthly hours, and salary. 
- [`tbl_hr_data`](https://console.cloud.google.com/bigquery?project=<your-gcp-project>&d=<dataset>&t=tbl_hr_data) — Historical employee data.  

 
- `tbl_new_employees`: New employee records used for prediction and evaluation.  
- [`tbl_new_employees`](https://console.cloud.google.com/bigquery?project=<your-gcp-project>&d=<dataset>&t=tbl_new_employees) — New employee records.  

The project connects to GCP using the [`google-cloud-bigquery`](https://pypi.org/project/google-cloud-bigquery/) Python library.


The data is accessed programmatically via the `google-cloud-bigquery` Python library, allowing dynamic querying, preprocessing, and uploading predictions back to BigQuery.

## Technologies Used
- **Programming Language**: Python 3.x  
- **Data Analysis & Visualization**: Pandas, NumPy, Matplotlib, Seaborn  
- **Machine Learning**: Scikit-learn (Logistic Regression, Random Forest, Gradient Boosting, etc.)  
- **Cloud Platform**: Google Cloud Platform (BigQuery, Cloud Storage)  
- **Development Environment**: Jupyter Notebook, VS Code / PyCharm  
- **Version Control**: Git and GitHub  

## Project Structure



## Setup & Usage
To run this project, follow these steps (all in one go, no numbered steps): clone the repository, create a virtual environment, install dependencies, configure GCP credentials, and execute scripts for preprocessing, training, and evaluation.  

```bash
git clone [https://github.com/<your-username>/GCP-Churn-Analysis.git](https://github.com/Snehlata1111/Google-Cloud-Data-Analysis--Employee-Retention-Program.git)
cd GCP-Churn-Analysis
python -m venv venv
source venv/bin/activate       # Linux/Mac
venv\Scripts\activate          # Windows
pip install -r requirements.txt
export GOOGLE_APPLICATION_CREDENTIALS="path/to/your/service-account.json"
python src/preprocess_data.py
python src/train_model.py
python src/evaluate_model.py
