## End to End Machine learning Project

# 🧠 End-to-End Machine Learning Pipeline with Flask Deployment

This project implements a complete machine learning workflow for predicting student performance based on demographic and exam data. It covers everything from data ingestion and transformation, to model training and evaluation, and ends with a production-ready Flask web app for real-time predictions.

---

## 🚀 Project Overview

**Objective**: Predict students' **math scores** using features such as gender, parental education, and other categorical and numerical inputs.

This pipeline simulates a real-world scenario by modularizing every component in a `src/` structure and enables seamless deployment using Flask. It includes:

- Data ingestion from raw `.csv`
- Data cleaning, encoding, and scaling via `Pipeline` and `ColumnTransformer`
- Model selection via `GridSearchCV`
- Evaluation of multiple regression models (XGBoost, CatBoost, RandomForest, etc.)
- Saving models and preprocessors with `pickle`
- Flask-based user interface for prediction

---

## 🧱 Project Architecture

├── app.py # Entry point for Flask app
├── src/
│ ├── components/
│ │ ├── data_ingestion.py # Loads and splits raw CSV into train/test
│ │ ├── data_transformation.py # Encodes + scales data and saves preprocessor
│ │ └── model_trainer.py # Trains multiple models and picks the best
│ ├── pipeline/
│ │ └── predict_pipeline.py # Loads model & preprocessor to make predictions
│ ├── utils.py # Utility functions (save/load, evaluation)
│ ├── logger.py # Custom logging setup
│ └── exception.py # Custom exception class for debugging
├── templates/
│ ├── index.html # Landing page
│ └── home.html # Prediction form
├── artifacts/ # Stores models, transformers, datasets
├── requirements.txt # Dependencies
├── setup.py # Packaging configuration
└── README.md # This file


---

## 📊 ML Models Used

- ✅ Random Forest
- ✅ Gradient Boosting
- ✅ Decision Tree
- ✅ AdaBoost
- ✅ CatBoost
- ✅ XGBoost
- ✅ Linear Regression

Model selection is done using `GridSearchCV`, and the best model is chosen based on **R² score** on the test set.

---

## 🛠️ Core Features

- 🧩 **Modular OOP Structure** — Designed for extensibility and maintainability
- 🧼 **Automated Preprocessing** — Pipelines with imputation, one-hot encoding, scaling
- 🔍 **Model Evaluation** — Multiple algorithms evaluated with proper metrics
- 💾 **Serialization** — Uses `pickle` to store preprocessor and best model
- 🌐 **Web Deployment** — Interactive user interface via Flask
- 🛡️ **Robust Logging & Error Handling** — Full traceability through logs and custom exceptions

---

## 🖥️ How to Run Locally

```bash
# Clone repository
git clone https://github.com/yourusername/ml-student-score-predictor.git
cd ml-student-score-predictor

# Create virtual environment
python -m venv venv
source venv/bin/activate  # For Windows: venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt

# Run the application
python app.py

🌐 Web App Preview
Open http://localhost:5000/predicdata


Enter student information (gender, lunch type, scores, etc.)

View predicted math score instantly

📈 Future Improvements currently working on
Integrate CI/CD pipeline

Add model monitoring with MLflow

Host on cloud (Azure and AWS EC2)
👨‍💻 Author
Mohamed Habib Haj Salah
📫 LinkedIn: www.linkedin.com/in/habib-hajsalah | 📧 hadjsalahmed@gmail.com

