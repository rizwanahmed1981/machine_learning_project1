# End-to-End Data Science Project - Wine Quality Prediction

A production-ready machine learning pipeline for predicting wine quality based on physicochemical properties. This project implements a complete data science workflow from data ingestion to model deployment.

## 📋 Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Project Structure](#project-structure)
- [Installation](#installation)
- [Usage](#usage)
- [ML Pipeline Stages](#ml-pipeline-stages)
- [Configuration](#configuration)
- [Dataset](#dataset)
- [Technologies Used](#technologies-used)
- [Docker Support](#docker-support)
- [License](#license)

## 🎯 Overview

This project demonstrates a production-grade ML pipeline implementation following industry best practices. It automates the entire data science workflow including data ingestion, validation, transformation, and model training with proper logging, configuration management, and artifact tracking.

## ✨ Features

- **Automated ML Pipeline** - End-to-end workflow from raw data to trained models
- **Data Validation** - Ensures data quality before processing
- **Feature Engineering** - Automated data transformation and preprocessing
- **Configuration Management** - YAML-based configuration for easy customization
- **Logging** - Comprehensive logging for monitoring and debugging
- **Modular Architecture** - Clean separation of concerns with reusable components
- **Docker Support** - Containerized deployment for consistency across environments

## 📁 Project Structure

```
machine_learning_project1/
├── src/
│   └── datascience/
│       ├── config/          # Configuration managers
│       ├── components/      # Pipeline components
│       ├── pipeline/        # Pipeline implementations
│       ├── entity/          # Data entities
│       ├── utils/           # Utility functions
│       └── constants/       # Constants
├── config/
│   └── config.yaml          # Main configuration file
├── templates/               # HTML templates for web interface
├── artifacts/               # Pipeline outputs and models
├── logs/                    # Application logs
├── main.py                  # Main entry point
├── app.py                   # Flask web application
├── requirements.txt         # Python dependencies
├── params.yaml              # Model parameters
├── schema.yaml              # Data schema definitions
└── Dockerfile               # Docker configuration
```

## 🚀 Installation

### Prerequisites

- Python 3.8+
- pip
- Git

### Steps

1. **Clone the repository**
   ```bash
   git clone <repository-url>
   cd machine_learning_project1
   ```

2. **Create a virtual environment**
   ```bash
   python -m venv venv
   ```

3. **Activate the virtual environment**
   - Windows:
     ```bash
     venv\Scripts\activate
     ```
   - Linux/Mac:
     ```bash
     source venv/bin/activate
     ```

4. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

## 📖 Usage

### Run the ML Pipeline

Execute the main pipeline:

```bash
python main.py
```

This will run the following stages sequentially:
1. Data Ingestion
2. Data Validation
3. Data Transformation

### Run Individual Stages

You can also run individual pipeline stages by importing and executing them directly in Python.

## 🔧 ML Pipeline Stages

### 1. Data Ingestion
- Downloads dataset from remote URL
- Extracts and stores data in artifacts directory
- Handles zip file extraction

### 2. Data Validation
- Validates data schema and column types
- Checks data quality and integrity
- Generates validation status report

### 3. Data Transformation
- Feature engineering
- Data preprocessing
- Handles missing values
- Data scaling and encoding

### 4. Model Training (Coming Soon)
- Train machine learning models
- Hyperparameter tuning
- Model serialization

### 5. Model Evaluation (Coming Soon)
- Model performance metrics
- MLflow integration for experiment tracking
- Model comparison and selection

## ⚙️ Configuration

### config.yaml
Main configuration file controlling:
- Artifact directories
- Data ingestion URLs
- Data validation paths
- Transformation settings

### schema.yaml
Defines data schema:
- Column names and data types
- Target column specification

### params.yaml
Model hyperparameters and training configurations

## 📊 Dataset

This project uses the **Wine Quality Dataset** containing physicochemical properties of red wine variants. The target variable is wine quality (scored 0-10).

**Features:**
- Fixed acidity
- Volatile acidity
- Citric acid
- Residual sugar
- Chlorides
- Free sulfur dioxide
- Total sulfur dioxide
- Density
- pH
- Sulphates
- Alcohol

**Target:** Quality (int64)

**Source:** [UCI Machine Learning Repository](https://archive.ics.uci.edu/ml/datasets/wine+quality)

## 🛠 Technologies Used

| Technology | Purpose |
|------------|---------|
| Python | Core programming language |
| scikit-learn | Machine learning algorithms |
| pandas | Data manipulation |
| NumPy | Numerical computing |
| Matplotlib | Data visualization |
| MLflow | Experiment tracking |
| Flask | Web application framework |
| PyYAML | Configuration management |
| Joblib | Model serialization |
| Docker | Containerization |

## 🐳 Docker Support

Build and run the application using Docker:

```bash
# Build the Docker image
docker build -t wine-quality-ml .

# Run the container
docker run -p 5000:5000 wine-quality-ml
```

## 📝 Workflow

To customize or extend this project:

1. Update `config.yaml` for paths and URLs
2. Update `schema.yaml` for data schema
3. Update `params.yaml` for model parameters
4. Update entities in `src/datascience/entity/`
5. Update configuration managers in `src/datascience/config/`
6. Update components in `src/datascience/components/`
7. Update pipelines in `src/datascience/pipeline/`
8. Update `main.py` for execution flow

## 📄 License

This project is open source and available for educational purposes.

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## 📧 Contact

For questions or issues, please open an issue in the repository.
