# Agile Nexus AI Platform

AI-Powered Sprint Management System with Predictive Analytics

## Project Information

- **Project Name:** Agile Nexus AI Platform
- **Version:** 2.0.0
- **Author:** ROOBA B, PRANEETA R, SADHANA G
- **Institution:** M. Kumarasamy College of Engineering
- **Course:** Agile Methodology
- **Submission Date:** 05.10.2025

## Overview

Agile Nexus uses three AI/ML models to predict sprint failures, optimize team productivity, and manage dependencies:

1. **Sprint Health Predictor** - Random Forest + XGBoost (0-100% risk prediction)
2. **Productivity Heatmap AI** - K-Means + SVR (productivity zone optimization)
3. **Dependency Tracker** - Graph Neural Networks (cascade risk analysis)

## Architecture
Data Sources (Calendar/Slack/GitHub)
↓
ETL Pipeline (Data Extraction)
↓
Feature Engineering & Processing
↓
AI/ML Models (3 models)
↓
REST API Layer (20+ endpoints)
↓
Interactive Dashboard

## Technology Stack

- **Backend:** Python 3.10, Flask 2.3.3
- **Database:** PostgreSQL 17
- **ML/AI:** scikit-learn 1.3.0, XGBoost 1.7.6, NetworkX 3.1
- **Data Processing:** Pandas 2.1.0, NumPy 1.24.3
- **Frontend:** HTML5, CSS3, JavaScript
- **APIs:** Google Calendar API, Slack SDK, GitHub API

## Features

- Real-time sprint failure prediction (0-100% risk score)
- Productivity zone optimization with K-Means clustering
- Dependency cascade analysis using Graph Neural Networks
- Role-based access control (Team Leader vs Team Member)
- Interactive dashboard with live data visualization
- Automated ETL pipeline for data collection
- Model training and retraining capabilities
- Historical data analysis and trending

## Installation

### Prerequisites
- Python 3.10+
- PostgreSQL 17
- 4GB RAM minimum
- 10GB disk space

### Setup Steps

1. **Create Virtual Environment**
python -m venv venv
venv\Scripts\activate  # Windows
source venv/bin/activate  # Mac/Linux

Install Dependencies
cd backend
pip install -r requirements.txt

Setup Database
psql -U postgres -h localhost

CREATE DATABASE agile_nexus;
CREATE USER agile_user WITH PASSWORD '[YOUR_PASSWORD]';
GRANT ALL PRIVILEGES ON DATABASE agile_nexus TO agile_user;

CREATE DATABASE agile_timeseries;
GRANT ALL PRIVILEGES ON DATABASE agile_timeseries TO agile_user;
\q

Run Application
cd backend
python app.py

Access Dashboard
Open dashboard.html in browser

Demo Credentials

Team Leader: leader / leader123
Team Member: member / member123

API Endpoints
Core Endpoints

GET / - API status
GET /api-status - System health
GET /run-etl - Extract data
GET /run-processing - Process data
GET /train-all-models - Train all models
GET /run-full-pipeline - Full pipeline

Model Testing

GET /test-sprint-model
GET /test-productivity-model
GET /test-dependency-model

Predictions

GET /predict-sprint-risk
GET /predict-productivity
GET /analyze-dependencies

Project Structure
agile-nexus/
├── backend/
│   ├── app.py
│   ├── config.py
│   ├── models.py
│   ├── requirements.txt
│   ├── etl_pipeline/
│   ├── processing/
│   └── ml_models/
├── frontend/
│   └── dashboard/
├── data/
├── dashboard.html
└── README.md
