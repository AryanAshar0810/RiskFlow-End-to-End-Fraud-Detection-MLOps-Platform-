# 💳 Fraud Detection MLOps Pipeline

An end-to-end fraud detection system built with production-grade MLOps practices. Includes automated pipelines, model version control, and deployment-ready architecture.

## 🏗️ System Architecture


**Architecture Highlights:**
- **Modular Pipelines**: Each stage is separated for maintainability and easier testing.
- **MLflow Integration**: Centralized experiment tracking and model registry management.
- **Docker & Kubernetes**: Containerized deployment ensuring consistency across environments.
- **Flask REST API**: Lightweight and production-ready serving interface.
- **Automated Retraining**: Continuous model updates driven by performance metrics.

## 🛠️ Technology Stack

- **Machine Learning**: scikit-learn, pandas, numpy  
- **MLOps Tools**: MLflow (experiment tracking), DVC (data versioning), BentoML (serving)  
- **Infrastructure**: Docker, Kubernetes, Flask  
- **Development Environment**: Python 3.10, Jupyter notebooks  

## 🚀 Quick Start

### Prerequisites
- Python 3.10 or higher
- Docker (optional, for containerized deployment)

## 🔄 MLOps Pipeline

1. Data Management: Track and version datasets with DVC, including automated preprocessing.
2. Model Development: Monitor experiments with MLflow, perform cross-validation, and optimize hyperparameters.
3. Validation & Testing: Run automated tests and evaluate model performance using key metrics.
4. Deployment: Containerize models with Docker and orchestrate using Kubernetes with CI/CD integration.
5. Monitoring: Detect data drift, track model performance, and trigger automated retraining.
6. Production Serving: Expose a REST API with health checks and load balancing for reliable serving.

### Setup
```bash
git clone <repository-url>
cd fraud-detection-mlops
pip install -r requirements.txt
```

### 🎯 Serve Model
```bash
# One-command solution: retrain + serve
python retrain_and_serve.py
# Web interface at http://localhost:3000
```

### 📊 Run EDA Analysis
```bash
# Execute all EDA notebooks
./run_eda_simple.sh

# Or run individual notebooks
jupyter notebook notebooks/
```


## 📊 EDA Notebooks

**Design Choice:** Conducted thorough exploratory data analysis to serve as the foundation of the MLOps pipeline, bridging critical gaps in typical data science workflows.

### 📈 01_exploration.ipynb
- **Objective**: Perform full data profiling and statistical examination
- **Key Findings**: Severe class imbalance (577:1), PCA feature patterns, correlation structure insights
- **Implementation**: Automated execution with detailed and comprehensive visualizations

### 🎯 02_baseline_model.ipynb
- **Objective**: Set baseline performance for fraud detection models
- **Models Used**: Logistic Regression, Random Forest with class balancing techniques
- **Evaluation Metrics**: AUC-ROC, Precision-Recall curves, feature importance analysis
- **Implementation**: Cross-validation with statistical significance testing

### 🔬 03_experiments.ipynb
- **Objective**: Explore advanced modeling techniques to improve predictive performance
- **Methods**: SMOTE oversampling, XGBoost, LightGBM, hyperparameter tuning
- **Implementation**: Modular design for easy experimentation and model comparison

## 📁 Project Structure

```
fraud-detection-mlops/
├── 📊 data/                    # Data management
│   ├── raw/                    # Raw transaction data
│   └── processed/              # Preprocessed features
├── 📓 notebooks/               # EDA and experimentation
│   ├── 01_exploration.ipynb    # Data profiling & analysis
│   ├── 02_baseline_model.ipynb # Baseline model development
│   └── 03_experiments.ipynb    # Advanced techniques
├── 🤖 models/                  # Trained models & artifacts
├── 🔧 src/                     # Source code
│   ├── data/                   # Data processing scripts
│   └── models/                 # ML model code
├── 🔄 pipelines/               # MLOps pipelines
│   ├── training_pipeline.py    # Automated training
│   ├── deployment_pipeline.py  # Deployment automation
│   └── monitoring_pipeline.py  # Performance monitoring
├── 🐳 infra/                   # Infrastructure as code
│   ├── docker/                 # Container definitions
│   └── k8s/                    # Kubernetes manifests
├── 🧪 tests/                   # Test suites
├── 📈 mlruns/                  # MLflow experiment logs
├── 🔄 mlartifacts/             # MLflow model artifacts
└── 📋 requirements.txt         # Python dependencies

## 🎯 Key Features

- **🔄 Continuous Training**: Automatically retrains models as new data becomes available  
- **📊 Experiment Tracking**: Maintains full lineage from raw data through predictions  
- **🔍 Data Validation**: Performs automated quality checks and drift detection  
- **🚀 One-Click Deployment**: Production-ready deployment via Docker and Kubernetes  
- **📈 Performance Monitoring**: Tracks model health in real time  
- **🔒 Production Ready**: Secure, scalable, and robust architecture
