# Machine Learning-Based Phishing Website Detection

A comprehensive cybersecurity machine learning project that evaluates multiple supervised learning algorithms for phishing website detection. This project compares the performance of Logistic Regression, Random Forest, and Multi-Layer Perceptron (Neural Network) models using the same feature-engineered phishing website dataset to identify the most effective approach for automated phishing detection.

The project demonstrates the complete machine learning workflow, including data preprocessing, feature scaling, model training, hyperparameter tuning, cross-validation, performance evaluation, and comparative analysis.

---

# Project Overview

Phishing remains one of the most common attack vectors used to steal credentials, distribute malware, and compromise sensitive information. Traditional blacklist-based detection methods often fail to identify newly created phishing websites, making machine learning a valuable solution for detecting malicious websites based on their characteristics.

This project investigates the effectiveness of multiple supervised machine learning algorithms for phishing website classification and compares their predictive performance using standardized evaluation metrics.

---

# Objectives

The primary objectives of this project were to:

- Develop machine learning models for phishing website detection.
- Compare the performance of multiple classification algorithms.
- Evaluate model accuracy and generalization capability.
- Identify the most effective model for phishing website classification.
- Demonstrate the application of machine learning techniques in cybersecurity.

---

# Dataset

The project uses a structured phishing website dataset consisting of engineered numerical features representing website behavior and characteristics.

Examples of extracted features include:

- External JavaScript references
- Inline scripts
- External resources
- Event handlers
- Library count
- HTML structural characteristics
- Script-based attributes
- Additional engineered website features

Each observation is labeled as either:

- Legitimate Website
- Phishing Website

To comply with licensing and academic restrictions, the original dataset is **not included** in this repository.

---

# Machine Learning Workflow

```
Raw Dataset
      │
      ▼
Data Preprocessing
      │
      ▼
Feature Scaling
      │
      ▼
Train/Test Split
      │
      ▼
Model Training
      │
      ▼
Model Evaluation
      │
      ▼
Performance Comparison
      │
      ▼
Best Model Selection
```

---

# Models Evaluated

## 1. Logistic Regression

Logistic Regression serves as the baseline classification model and provides a simple, interpretable solution for phishing website detection.

Implemented using:

- Feature standardization
- Train/Test split
- Cross-validation
- ROC analysis
- Confusion matrix
- Classification metrics

Approximate Performance

- Accuracy: ~82%
- ROC-AUC: ~0.85

---

## 2. Random Forest

Random Forest is an ensemble learning algorithm that combines multiple decision trees to improve predictive performance and reduce overfitting.

The implementation includes:

- Hyperparameter tuning
- Multiple tree configurations
- Feature importance analysis
- Cross-validation
- ROC analysis
- Confusion matrix

Approximate Performance

- Accuracy: ~92%
- ROC-AUC: ~0.95

This model achieved the best overall performance among all evaluated algorithms.

---

## 3. Multi-Layer Perceptron (Neural Network)

The Multi-Layer Perceptron (MLP) classifier evaluates the use of neural networks for phishing website detection.

Implementation includes:

- Feature scaling
- Neural network training
- Performance evaluation
- ROC analysis
- Confusion matrix

Approximate Performance

- Accuracy: ~86%
- ROC-AUC: ~0.86

---

# Model Comparison

| Model | Approximate Accuracy | ROC-AUC | Summary |
|--------|---------------------:|---------:|---------|
| Logistic Regression | ~82% | ~0.85 | Simple and interpretable baseline model |
| Random Forest | **~92%** | **~0.95** | Best overall performance |
| Neural Network | ~86% | ~0.86 | Effective nonlinear classifier |

---

# Key Findings

- Successfully implemented three supervised machine learning algorithms.
- Compared model performance using standardized evaluation metrics.
- Performed feature scaling and preprocessing for consistent model training.
- Evaluated models using confusion matrices, ROC curves, and cross-validation.
- Identified Random Forest as the highest-performing classifier.
- Demonstrated how machine learning can improve phishing website detection.

---

# Technologies Used

- Python
- Pandas
- NumPy
- Scikit-learn
- Matplotlib
- Jupyter Notebook

---

# Skills Demonstrated

- Machine Learning
- Cybersecurity Analytics
- Phishing Detection
- Data Preprocessing
- Feature Engineering
- Supervised Learning
- Logistic Regression
- Random Forest
- Neural Networks
- Hyperparameter Tuning
- Cross Validation
- ROC Analysis
- Model Evaluation
- Classification Metrics
- Data Visualization
- Python Programming

---

# Repository Contents

```
07-machine-learning-phishing-detection/

│── 01-logistic_regression.ipynb
│── 02-random_forest.ipynb
│── 03-neural_network_and_model_comparison.ipynb
│
│── 01-logistic_regression_notebook.pdf
│── 02-random_forest_notebook.pdf
│── 03-neural_network_notebook.pdf
│
│── Machine_Learning_Phishing_Detection_Report.pdf
│── README.md
```

---

# Practical Security Applications

The techniques demonstrated in this project can be applied to a variety of real-world cybersecurity use cases, including:

- Email security gateways
- Secure web gateways
- Browser-based phishing protection
- Threat intelligence platforms
- Security Operations Centers (SOC)
- Automated phishing detection systems
- Enterprise web filtering
- Security analytics pipelines

---

# Conclusion

This project demonstrates the complete lifecycle of developing and evaluating machine learning models for phishing website detection. By comparing Logistic Regression, Random Forest, and Neural Network classifiers under identical conditions, the study identifies Random Forest as the most effective model for this dataset while highlighting the strengths and trade-offs of each approach.

The project showcases the integration of cybersecurity and machine learning principles to build scalable, data-driven phishing detection solutions suitable for modern enterprise security environments.

---

# Disclaimer

This repository is intended solely for educational and portfolio purposes.

The original phishing dataset is not included due to licensing and academic restrictions. Only the implementation methodology, model development, evaluation, and summarized findings are provided.