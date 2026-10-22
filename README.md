# End- to-End Model Monitoring using Airflow and Docker

1.

## Overview
Let’s consider you have developed a machine learning model with high accuracy by using the raw data. The next step is to put this highly accurate model into production by fetching the data in daily batches. But the model in prediction can fail without any warning. Due to the same keeping, an eye on the model’s prediction power becomes necessary. Also, in the real world, data can change due to various factors affecting prediction accuracy. In production, taking a major to prevent such changing behavior of model and data is important to serve the business problem over time. In this project, we will build an end-to-end pipeline to monitor any changes in the model's predictive power or degradation of data, commonly known as Model and Drift Monitoring. The model is built to classify whether or not a loan is to be given or rejected based on data fetched from PostgreSQL. This project also demonstrates the orchestration of ML pipelines using Docker and Airflow.

## Approach
1. Extracting Data from PostgreSQL
2. Data Preprocessing a. Train-Test split b. Encoding Categorical Variables c. Imputing Missing Values

d. Rescaling the Data e. Feature Engineering
3. Model Training and Evaluation a. Random Forest b. Gradient Boosting
4. Model Monitoring a. Concept Drift b. Data Drift c. Model Drift
5. Orchestration with Airflow

Note:
1. Kindly follow the readme.md file for running the code
2. This project requires the data to be present in postgres server. The data is available in code>main>dags>data>raw location. Kindly upload the data and provide the appropriate credentials in code>main>dags>creds.json file.

## Tech stack
➔ Language: Python ➔ Libraries: pandas, numpy, matplotlib, scikit-learn, deepchecks, sqlalchemy, psycopg2-binary ➔ Services: Airflow, Docker, PostgreSQL

## How to run
```bash
pip install -r code (1)/docker-airflow-run/requirements.txt
python code (1)/docker-airflow-run/dags/app.py
python code (1)/docker-airflow-run/dags/src/train.py
```
Notebooks: [`EDA.ipynb`](code%20(1)/local/notebooks/EDA.ipynb), [`lab01 - data collection.ipynb`](code%20(1)/local/notebooks/lab01%20-%20data%20collection.ipynb), [`lab02 - preprocess.ipynb`](code%20(1)/local/notebooks/lab02%20-%20preprocess.ipynb), [`lab03 - training.ipynb`](code%20(1)/local/notebooks/lab03%20-%20training.ipynb)

## Project structure
```
.gitignore
README.md
code (1)/
  docker-airflow-run/
    airflow.sh
    dags/
    docker-compose.yaml
    readme.md
    requirements.txt
  local/
    dags/
    notebooks/
    readme.md
```

## Credits
Based on a ProjectPro guided project.
