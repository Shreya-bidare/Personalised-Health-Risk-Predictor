Personalized Health Risk Predictor

Overview
This project is a Flask-based AI web application that predicts health risks for:
Diabetes
Heart Disease
Lung Cancer
The system integrates four different predictive modeling approaches:
 Machine Learning (Random Forest)
 
 Deep Learning (Keras / TensorFlow)
 
 Quantum Machine Learning (Hybrid models)
 
 Quantum Neural Networks (QNN using PennyLane + PyTorch)
 
If any model detects potential risk, the application dynamically calls the Gemini LLM API to generate evidence-based medical recommendations.

System Architecture
 Backend
Flask-based REST architecture

Model inference pipeline

Gemini API integration

Metrics loading from metrics.json

Prediction Pipeline

Each prediction request:
User inputs medical parameters
All four models (ML, DL, QML, QNN) run in parallel
Risk classification is generated
If risk is detected:
Gemini API is triggered
Personalized medical recommendations are generated
Responses are cached using MD5 hashing for efficiency

Features Used for Prediction

Diabetes

Glucose

BMI

Age

Diabetes Pedigree Function

Heart Disease
Age
Sex
Chest Pain Type
Maximum Heart Rate
ST Depression
Exercise-Induced Angina

Lung Cancer
Age
Gender
Smoking Habit
Coughing
Chest Pain
Shortness of Breath

Key Features
Multi-model prediction (ML + DL + QML + QNN)
Quantum computing integration for healthcare analytics
Gemini-powered medical recommendation system
Model accuracy display from stored evaluation metrics
Dockerized deployment
CI/CD integration using GitHub Actions

Technologies Used
Python
Flask
HTML / CSS
scikit-learn
TensorFlow / Keras
PyTorch
PennyLane
Qiskit
Gemini LLM API
Docker
GitHub Actions
