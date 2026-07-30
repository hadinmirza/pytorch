# 🔥 PyTorch Exploration and Telco Customer Churn Prediction

## 📌 Project Overview

This project explores the fundamentals of **PyTorch** and demonstrates how to build a complete deep learning pipeline for a real-world binary classification problem.

The project begins by introducing PyTorch tensors, tensor operations, automatic differentiation (Autograd), and neural network fundamentals. These concepts are then applied to the **Telco Customer Churn** dataset by building, training, and evaluating a Multi-Layer Perceptron (MLP) for predicting customer churn.

The project was completed as part of the **Devsinc AI/ML Internship (Day 7 Assignment)** to gain practical experience with PyTorch and understand how deep learning models compare with traditional machine learning algorithms on structured tabular data.

---

# 🎯 Problem Statement

Telecommunication companies frequently lose customers due to contract expiration, pricing, service quality, and customer satisfaction issues.

The objective of this project is to build a deep learning model capable of predicting whether a customer is likely to churn based on customer demographics, account information, and subscribed services.

---

# ❓Business Question

**Can a PyTorch-based neural network accurately predict customer churn, and how does its performance compare with a classical Machine Learning model?**

---

# 📊 Problem Type

**Binary Classification**

The target variable (`Churn`) contains two classes:

* **Yes** → Customer will churn
* **No** → Customer will remain

---

# 📂 Dataset Information

* **Source:** Kaggle
* **Domain:** Telecommunications

Dataset Size

* **7,043 Customers**
* **26 Features** (after feature engineering)

The dataset contains customer demographic information, account details, subscribed services, billing information, and engineered features created during previous preprocessing.

---

# 🎯 Target Variable

```text
Churn
```

The goal is to predict whether a customer will leave the company.

---

# 🛠 Project Workflow

### 1. PyTorch Fundamentals

The notebook begins with an introduction to PyTorch and covers:

* Creating tensors
* Tensor dimensions
* Tensor properties
* Tensor operations
* Matrix multiplication
* CPU device
* Automatic differentiation (Autograd)

---

### 2. Data Loading

The cleaned Telco Customer Churn dataset created during previous assignments was loaded into the notebook.

---

### 3. Feature Preparation

The dataset was prepared by:

* Separating features and target
* Identifying categorical and numerical features
* One-Hot Encoding categorical variables
* Standardizing numerical features
* Splitting the dataset into training and testing sets

---

### 4. Tensor Conversion

The processed dataset was converted into PyTorch tensors (`float32`) to make it compatible with neural network training.

---

### 5. Data Loading with DataLoader

PyTorch's `TensorDataset` and `DataLoader` were used to efficiently create mini-batches for training.

---

### 6. Neural Network Architecture

A Multi-Layer Perceptron (MLP) was implemented using PyTorch.

Architecture:

```text
Input Layer
      │
      ▼
Linear (64)
      │
    ReLU
      │
      ▼
Linear (32)
      │
    ReLU
      │
      ▼
Linear (1)
```

The output layer produces a single logit which is converted into a probability using the Sigmoid function during evaluation.

---

### 7. Model Training

The model was trained using:

* **Loss Function:** BCEWithLogitsLoss
* **Optimizer:** Adam
* **Learning Rate:** 0.001
* **Epochs:** 30
* **Batch Size:** 32

---

### 8. Model Evaluation

The trained model was evaluated using the unseen testing dataset.

Evaluation Metrics:

* Accuracy
* Precision
* Recall
* F1-Score
* ROC-AUC
* Confusion Matrix
* Classification Report

---

# 📈 Results

## PyTorch Neural Network

| Metric    |      Value |
| --------- | ---------: |
| Accuracy  | **77.93%** |
| Precision | **59.24%** |
| Recall    | **54.01%** |
| F1-Score  | **56.50%** |
| ROC-AUC   | **0.8111** |

Confusion Matrix

```text
[[896 139]
 [172 202]]
```

The neural network successfully learned meaningful patterns from the dataset and achieved stable performance throughout training.

---

# 📊 Model Comparison

| Metric    | Logistic Regression | PyTorch Neural Network |
| --------- | ------------------: | ---------------------: |
| Accuracy  |          **80.41%** |                 77.93% |
| Precision |          **66.44%** |                 59.24% |
| Recall    |              52.94% |             **54.01%** |
| F1-Score  |          **58.93%** |                 56.50% |
| ROC-AUC   |          **0.8416** |                 0.8111 |

The comparison demonstrates that although the neural network successfully learned the dataset, the previously developed Logistic Regression model achieved better overall performance on this structured tabular dataset.

---

# 📁 Project Structure

```text
PyTorch-Telco-Churn
│
├── data
│   └── fully_featured_telco_customer_churn.csv
│
├── notebooks
│   └── pytorch.ipynb
│
├── README.md
├── requirements.txt
└── .gitignore
```

---

# 💻 Technologies Used

* Python
* PyTorch
* Pandas
* NumPy
* Scikit-learn
* Jupyter Notebook
* Git
* GitHub

---

# 📚 What I Learned

Through this project, I gained practical experience with:

* PyTorch fundamentals
* Tensor creation and manipulation
* Tensor properties and dimensions
* Matrix operations
* Automatic Differentiation (Autograd)
* Neural network architecture
* Building models using `nn.Module`
* TensorDataset and DataLoader
* Binary Cross Entropy Loss
* Adam Optimizer
* Model training using backpropagation
* Deep learning model evaluation
* Comparing deep learning with classical machine learning models

---

# ⚠ Challenges Faced

Some challenges encountered during this project included:

* Understanding how tensors differ from traditional NumPy arrays.
* Learning the concept of Automatic Differentiation (Autograd).
* Understanding the complete PyTorch training workflow, including forward propagation, backpropagation, and optimizer updates.
* Preparing structured tabular data for neural network training.
* Interpreting why the neural network did not outperform Logistic Regression on this dataset.
* Understanding that lower training loss does not always translate into better performance on unseen data due to overfitting.

---

# 🔮 Future Improvements

Possible improvements include:

* Hyperparameter tuning using different learning rates.
* Experimenting with deeper neural network architectures.
* Applying Dropout and Batch Normalization.
* Performing k-fold cross-validation.
* Using learning rate schedulers.
* Comparing results with advanced models such as XGBoost, LightGBM, and CatBoost.
* Deploying the trained model as a web application.

---

# 📝 Daily Progress

### Topics Covered

* Introduction to PyTorch
* Tensor Fundamentals
* Automatic Differentiation
* Neural Networks
* DataLoader
* Model Training
* Model Evaluation
* Deep Learning Workflow

### Deliverables Completed

* PyTorch exploration notebook
* Neural network implementation
* Telco churn prediction model
* Model evaluation
* Comparison with Logistic Regression
* GitHub version control using feature branches and pull requests

---

# 👨‍💻 Author

**Muhammad Hadin Mirza**

Computer Engineering Student

Information Technology University (ITU)

Devsinc AI/ML Summer Internship 2026

This project was developed for learning purposes and demonstrates the practical implementation of PyTorch fundamentals and deep learning for binary classification.
