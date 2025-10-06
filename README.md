# 🚗 Vehicle Insurance Data Pipeline — End-to-End MLOps Project

Welcome to this **MLOps project**, built to showcase how a complete **Machine Learning pipeline** can manage and deploy **vehicle insurance data** in a real-world setup.

This project highlights my ability to combine **Machine Learning, MLOps, and Cloud Deployment** into one seamless workflow — covering everything from data ingestion to automated CI/CD on AWS.

Follow along to explore how this project handles data, builds models, deploys APIs, and automates workflows with precision.

---

## 📁 Project Setup and Structure

### 🧩 Step 1: Create Project Template

Run `template.py` to generate the full folder structure, including all placeholders for data, components, and configuration files.

### ⚙️ Step 2: Package Management

Set up local imports and dependencies using `setup.py` and `pyproject.toml`.
📘 Tip: You can learn more about these in `crashcourse.txt`.

### 🧠 Step 3: Virtual Environment & Dependencies

Create and activate your environment:

```bash
conda create -n vehicle python=3.10 -y
conda activate vehicle
pip install -r requirements.txt
```

Verify local packages:

```bash
pip list
```

---

## 📊 MongoDB Setup & Data Management

### ☁️ Step 4: Configure MongoDB Atlas

* Create a free **M0 cluster** in MongoDB Atlas
* Allow access from all IPs (0.0.0.0/0)
* Retrieve your connection string and update credentials

### 💾 Step 5: Push Data to MongoDB

* Add dataset to the `notebook/` folder
* Use `mongoDB_demo.ipynb` to push and verify data in Atlas

---

## 🧩 Logging, Exception Handling & EDA

### 🪵 Step 6: Logging & Exception Handling

Implement and test modules for logging and exception handling via `demo.py`.

### 📈 Step 7: Exploratory Data Analysis (EDA)

Perform feature engineering and data cleaning for the insurance dataset.

---

## 📥 Data Ingestion

### ⚡ Step 8: Build Data Ingestion Pipeline

* Configure MongoDB connections in `configuration.mongo_db_connections.py`
* Implement components in `data_access` and `components.data_ingestion.py`
* Update entities in `config_entity.py` & `artifact_entity.py`

Run demo:

```bash
export MONGODB_URL="your_mongo_url"
python demo.py
```

---

## 🔍 Data Validation, Transformation & Model Training

### ✅ Step 9: Data Validation

Define schema in `config/schema.yaml` and validate using `utils.main_utils.py`.

### 🔄 Step 10: Data Transformation

Transform raw data and create `estimator.py` in `entity` folder.

### 🧠 Step 11: Model Training

Train and evaluate models in `components.model_trainer.py`.

---

## 🌐 AWS Setup for Deployment

### ☁️ Step 12: Configure AWS

* Create an IAM user with **AdministratorAccess**
* Set credentials as environment variables

```bash
export AWS_ACCESS_KEY_ID="YOUR_KEY"
export AWS_SECRET_ACCESS_KEY="YOUR_SECRET"
```

* Create an S3 bucket for storing trained models

### 📦 Step 13: Model Evaluation & S3 Integration

Upload and retrieve models via `src.aws_storage` and `entity/s3_estimator.py`.

---

## 🚀 Model Deployment & API Integration

### 🧩 Step 14: Model Pusher + Prediction Pipeline

* Deploy trained model via `FastAPI` (`app.py`)
* Build REST endpoints for prediction and health check

### 💻 Step 15: Add Web UI

Include static templates and front-end integration for demo visualization.

---

## 🔄 CI/CD Setup (Docker + GitHub Actions + AWS)

### 🐳 Step 16: Docker & GitHub Actions

* Add `Dockerfile` and `.dockerignore`
* Set GitHub secrets for AWS credentials

  * `AWS_ACCESS_KEY_ID`
  * `AWS_SECRET_ACCESS_KEY`
  * `AWS_DEFAULT_REGION`
  * `ECR_REPO`

### ☁️ Step 17: AWS EC2 + ECR Deployment

* Launch EC2 instance
* Install Docker and connect as **self-hosted runner**
* Open port `5080` for access
* Visit:

  ```
  http://<your_public_ip>:5080
  ```

---

## 🎯 Workflow Summary

```
Data Ingestion ➜ Data Validation ➜ Data Transformation
➜ Model Training ➜ Model Evaluation ➜ Model Deployment
➜ CI/CD Automation (GitHub Actions, Docker, AWS)
```

---

## 💡 Future Enhancements

* Add **model explainability (SHAP/LIME)**
* Integrate **Grafana dashboards**
* Deploy to **AWS SageMaker / GCP Vertex AI**
* Extend to **real-time streaming pipelines**

---

## 👨‍💻 About the Author

Hi 👋 I’m **Shah Meer Nawaz**, a **Machine Learning Engineer** currently pursuing my **Master’s in Artificial Intelligence**.
I specialize in **Deep Learning, Computer Vision, NLP, Generative AI, and MLOps** — turning research models into production-grade AI systems.

📩 Let’s collaborate — whether you’re building a prototype or scaling your next AI product.


