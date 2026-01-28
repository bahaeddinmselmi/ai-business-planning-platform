# 🏭 AI Integrated Business Planning (IBP) Platform

> An open-source, AI-native **Supply Chain Planning Engine**. Features probabilistic forecasting, inventory optimization, and scenario simulation.

[![FastAPI](https://img.shields.io/badge/FastAPI-0.109-009688.svg?style=flat&logo=fastapi&logoColor=white)](https://fastapi.tiangolo.com)
[![Python](https://img.shields.io/badge/Python-3.10%2B-blue)](https://python.org)
[![MLOps](https://img.shields.io/badge/MLOps-Ready-orange)](https://mlflow.org)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

## 📖 Overview

**IBP AI** is a modular SaaS skeleton for modern supply chain management. It moves beyond static spreadsheets to offer a dynamic, ML-driven control tower for planners.

Unlike traditional ERPs, this platform is built **AI-first**, integrating probabilistic models (DeepAR, Prophet, XGBoost) directly into the planning logic.

### 🚀 Core Capabilities
*   **Probabilistic Forecasting**: Predict demand with confidence intervals (P10, P50, P90) using ensemble methods.
*   **Inventory Optimization**: Dynamic safety stock calculations and reorder point suggestions.
*   **Scenario Planning**: Simulate "what-if" events (e.g., *Supplier X fails*, *Demand spikes 40%*).
*   **Explainable AI**: Understand *why* a forecast changed (SHAP values for demand drivers).
*   **API-First Design**: Fully decoupled backend ready for React/Streamlit frontends.

## 🏗️ Architecture

The system is designed as a Microservice-ready Monolith:
*   **Backend**: FastAPI, Pydantic, Pandas.
*   **ML Engine**: Scikit-learn, Prophet (extensible to PyTorch/TensorFlow).
*   **Data Layer**: CSV Stubs (Production ready for PostgreSQL/Snowflake).

## ⚡ Quick Start

### 1. Installation
```bash
git clone https://github.com/bahaeddinmselmi/ai-business-planning-platform.git
cd ai-business-planning-platform
pip install -r requirements.txt
```

### 2. Run the API
```bash
uvicorn backend.app.main:app --reload
```

### 3. Explore
Open Swagger UI at `http://localhost:8000/docs` to test endpoints:
*   `POST /api/v1/forecast`: Generate demand predictions.
*   `POST /api/v1/plan/generate`: Run the specialized supply planning solver.

## 🤝 Roadmap
- [ ] Integration with real ERP (SAP/Odoo) connectors.
- [ ] Reinforcement Learning for inventory policies.
- [ ] Graph Neural Networks for supply chain mapping.

## 📄 License
MIT
