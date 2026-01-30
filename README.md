<div align="center">

<img src="https://readme-typing-svg.herokuapp.com?font=Fira+Code&weight=600&size=30&duration=3000&pause=1000&color=E32E2E&center=true&vCenter=true&width=600&lines=Bank+Customer+Churn+Prediction;Artificial+Neural+Networks+(ANN);99.7%25+Model+Accuracy;Deep+Learning+Classification" alt="Typing SVG" />

<p>
    <img src="https://img.shields.io/badge/Python-3.8%2B-blue?style=for-the-badge&logo=python&logoColor=white" />
    <img src="https://img.shields.io/badge/Deep%20Learning-TensorFlow-orange?style=for-the-badge&logo=tensorflow&logoColor=white" />
    <img src="https://img.shields.io/badge/API-Keras-D00000?style=for-the-badge&logo=keras&logoColor=white" />
    <img src="https://img.shields.io/badge/Data-Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white" />
    <img src="https://img.shields.io/badge/Visualization-Seaborn-success?style=for-the-badge&logo=seaborn&logoColor=white" />
</p>

<h3>🚀 A High-Precision Deep Learning model to predict customer attrition.</h3>

</div>

---

## 📌 Project Overview
Customer retention is vital for the banking industry. This project utilizes an **Artificial Neural Network (ANN)** to predict whether a customer will leave the bank (Churn) or stay (Retain) based on their demographic and financial data.

The model analyzes patterns in credit scores, account balances, and activity levels to identify at-risk customers with **near-perfect accuracy**.

---

## 📂 The Dataset
**Source:** `Customer-Churn-Records.csv`

| Feature | Description |
| :--- | :--- |
| **CreditScore** | The customer's credit score. |
| **Geography** | The country of residence (France, Spain, Germany). |
| **Gender** | Male or Female. |
| **Age** | Customer's age. |
| **Tenure** | How many years they have been a client. |
| **Balance** | Current account balance. |
| **NumOfProducts** | Number of bank products used (e.g., savings, credit card). |
| **HasCrCard** | Whether they hold a credit card (1=Yes, 0=No). |
| **IsActiveMember** | Activity status (1=Active, 0=Inactive). |
| **EstimatedSalary** | Annual estimated salary. |
| **Exited (Target)** | **1 = Churn (Left)**, **0 = Retained (Stayed)**. |

> *Note: Irrelevant columns like `RowNumber`, `CustomerId`, and `Surname` were dropped during preprocessing.*

---

## 🏆 Model Performance
The ANN model achieved exceptional results on the test set:

| 🧠 Metric | 📊 Score |
| :--- | :--- |
| **Accuracy** | **99.7%** |
| **Precision (Class 0 - Retained)** | **1.00** |
| **Precision (Class 1 - Churned)** | **0.99** |
| **F1-Score** | **0.99** |

---

## ⚙️ How It Works (Workflow)

### 1️⃣ Data Preprocessing
* **Cleaning:** Removed non-predictive columns (`RowNumber`, `Surname`).
* **Encoding:** Converted categorical data (`Geography`, `Gender`) into numbers using **One-Hot Encoding**.
* **Scaling:** Applied **StandardScaler** to normalize numerical features (`Balance`, `Salary`, `Age`) for faster convergence.

### 2️⃣ Neural Network Architecture (ANN)
Built using the **Keras Sequential API**:
* **Input Layer:** Matches the feature set size.
* **Hidden Layers:**
    * **Dense Layers:** Using `ReLU` activation for pattern recognition.
    * **BatchNormalization:** Applied to stabilize and speed up learning.
    * **Dropout:** Randomly ignores neurons during training to prevent overfitting.
* **Output Layer:** Single neuron with **Sigmoid Activation** (outputs probability between 0 and 1).

### 3️⃣ Training
* **Optimizer:** Adam
* **Loss Function:** Binary Crossentropy
* **Validation:** Used a validation split to monitor performance during training.

---

## 🚀 How to Run Locally

```bash
# 1. Clone the repository
git clone [https://github.com/YOUR_USERNAME/Bank-Customer-Churn-Prediction.git](https://github.com/YOUR_USERNAME/Bank-Customer-Churn-Prediction.git)

# 2. Navigate to the project directory
cd Bank-Customer-Churn-Prediction

# 3. Install dependencies
pip install pandas numpy tensorflow keras scikit-learn matplotlib seaborn

# 4. Run the Jupyter Notebook
jupyter notebook "Churn_Prediction_ANN.ipynb"
