# CardioCare Platform

> Modernizing an academic cardiac risk prediction research prototype into a production-style healthcare platform.

![Python](https://img.shields.io/badge/Python-3.12-blue)
![FastAPI](https://img.shields.io/badge/FastAPI-Backend-009688)
![React](https://img.shields.io/badge/React-Frontend-61DAFB)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6)
![Docker](https://img.shields.io/badge/Docker-Containerized-2496ED)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-Database-336791)
![Random Forest](https://img.shields.io/badge/ML-Random%20Forest-green)

---

## Overview

CardioCare Platform is a production-style healthcare web application that predicts cardiac disease risk from patient information while providing patient management and doctor workflows.

This project is the second iteration of my undergraduate research project.

Instead of redesigning the machine learning model, the goal of this version is to modernize the surrounding software architecture using current backend and frontend engineering practices.

---

## Project Evolution

### Version 1 — Academic Research Prototype

Developed during my undergraduate studies.

**Focus**

- Machine Learning Research
- Text-based Cardiac Risk Prediction
- Model Training & Evaluation

**Technologies**

- Google Colab
- PySpark
- Word2Vec
- Random Forest
- Python

---

 Original Repository

https://github.com/smahasr/Text-Based-Risk-Preidiction

---

### Version 2 — CardioCare Platform (Current)

This repository transforms the original research into a production-style application.

Modernization includes

- Modern React frontend
- FastAPI backend
- REST APIs
- PostgreSQL
- Docker
- Authentication
- Professional folder structure
- Responsive UI
- Patient & Doctor workflows

The original trained Random Forest model is preserved as the prediction engine.

---

# Features

## Patient

- User Registration
- Login
- Patient Dashboard
- Cardiac Risk Assessment
- Prediction History
- Nearby Hospital Recommendations
- Nearby Cardiologist Recommendations

---

## Doctor

- Doctor Dashboard
- View Assigned Patients
- Review Patient Predictions
- Patient History
- Consultation Notes

---

## Administrator

- User Management
- Doctor Management
- Hospital Management
- Prediction Statistics
- System Monitoring

---

## Machine Learning

- Existing Random Forest Model
- Feature Engineering Pipeline
- REST Prediction API
- Prediction History

---

# System Architecture

```text
                                    ┌────────────────────┐
                                    │      Patient       │
                                    └─────────┬──────────┘
                                              │
                                              ▼
                             ┌──────────────────────────────┐
                             │     React + TypeScript UI    │
                             │                              │
                             │ • Patient Portal             │
                             │ • Doctor Portal              │
                             │ • Admin Dashboard            │
                             └──────────────┬───────────────┘
                                            │ REST API
                                            ▼
                         ┌────────────────────────────────────┐
                         │           FastAPI Backend          │
                         │                                    │
                         │ Authentication                     │
                         │ Patient Management                 │
                         │ Doctor Management                  │
                         │ Prediction Service                 │
                         │ Hospital Recommendation            │
                         └──────────────┬─────────────────────┘
                                        │
                  ┌─────────────────────┼────────────────────┐
                  │                     │                    │
                  ▼                     ▼                    ▼
         ┌────────────────┐   ┌────────────────┐   ┌────────────────┐
         │ PostgreSQL DB  │   │ ML Prediction  │   │ Recommendation │
         │                │   │ Engine         │   │ Service         │
         │ Patients       │   │                │   │ Hospitals       │
         │ Doctors        │   │ Random Forest  │   │ Doctors         │
         │ Predictions    │   │ (.pkl Model)   │   │                │
         └────────────────┘   └────────────────┘   └────────────────┘
```

---

# Project Structure

```text
cardiocare-platform/

├── frontend/
│   ├── public/
│   ├── src/
│   │   ├── components/
│   │   ├── pages/
│   │   ├── layouts/
│   │   ├── services/
│   │   ├── hooks/
│   │   ├── routes/
│   │   └── App.tsx
│   └── Dockerfile
│
├── backend/
│   ├── app/
│   │   ├── api/
│   │   ├── auth/
│   │   ├── models/
│   │   ├── schemas/
│   │   ├── services/
│   │   ├── repositories/
│   │   ├── database/
│   │   └── main.py
│   └── Dockerfile
│
├── ml/
│   ├── model/
│   │   └── random_forest.pkl
│   ├── preprocessing/
│   ├── feature_engineering/
│   ├── inference/
│   └── prediction_service.py
│
├── database/
├── docs/
├── tests/
├── infra/
├── docker-compose.yml
├── README.md
└── LICENSE
```

---

# Technology Stack

| Category | Technologies |
|-----------|--------------|
| Frontend | React, TypeScript, Tailwind CSS, shadcn/ui |
| Backend | FastAPI, Python, SQLAlchemy, Pydantic |
| Machine Learning | Scikit-learn, Random Forest |
| Database | PostgreSQL |
| Authentication | JWT |
| API | REST API |
| Containerization | Docker, Docker Compose |
| Version Control | Git, GitHub |

---

# Prediction Workflow

```text
Patient

↓

Login

↓

Enter Patient Information

↓

Submit Symptoms

↓

Backend Validation

↓

Feature Engineering

↓

Random Forest Model

↓

Risk Prediction

↓

Save Prediction

↓

Display Results

↓

Doctor Review

↓

Prediction History
```

---

# 📸 Application Preview

> Screenshots will be added as development progresses.

- Login
- Patient Dashboard
- Doctor Dashboard
- Prediction Page
- Admin Dashboard
- Reports

---

#  Running Locally

```bash
git clone https://github.com/smahasr/cardiocare-platform.git

cd cardiocare-platform

docker compose up --build
```

---

# Roadmap

### Version 2.0

- Production-style architecture
- React frontend
- FastAPI backend
- Docker deployment
- Existing Random Forest integration

### Version 2.1

- Enhanced UI
- Better analytics
- Improved reports

### Version 3.0

- AI-powered explanation of predictions
- LLM integration
- Medical report upload
- Voice symptom input
- Clinical note generation

---

#  Engineering Highlights

- Modernized an academic ML research project into a production-style application.
- Preserved the original trained Random Forest model while redesigning the application architecture.
- Refactored notebook-based code into modular backend services.
- Designed role-based healthcare workflows for Patients, Doctors, and Administrators.
- Built with clean project structure and Docker-first development principles.

---

# ⚠ Disclaimer

This project is intended for educational and portfolio purposes.

The cardiac risk predictions generated by the application are based on an existing research model and should **not** be used as a substitute for professional medical advice or clinical diagnosis.

---

# 📄 License

MIT License
