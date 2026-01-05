# Credit_Card-ML_Pipeline

# 💳 Credit Card Fraud Detection – ML Pipeline

---

##  Project Overview

This project implements a **Machine Learning pipeline** to detect **fraudulent credit card transactions**.

The goal is to take raw transaction data, process it step by step, train ML models, evaluate their performance, and visualize results such as the **ROC Curve**.


---

## 🤖 Models Implemented

The following Machine Learning models are used:

* **Logistic Regression** (baseline model)
* **Random Forest Classifier** (main model)

---

##  Project Structure

```
Credit_Card_ML_Pipeline/
│
├── data/
│   └── creditcard.csv
│
├── src/
│   ├── data_pipeline.py      # Data loading & preprocessing
│   ├── train_model.py        # Model training
│   ├── evaluate_model.py     # Model evaluation
│   └── utils.py              # Helper functions
│
├── models/
│   └── fraud_model.pkl
│
├── plots/
│   └── roc_curve.png
│
├── requirements.txt
├── README.md
└── main.py
```

---

## ⚙️ How the Code Works (Step-by-Step)

### 1️ Credit Card Initialization (Data Loading)

* Loads the credit card dataset from CSV file
* Uses Pandas to read and inspect data

```python
pd.read_csv("creditcard.csv")
```

---

### 2️⃣ Data Preprocessing (ML Pipeline)

Performed inside `data_pipeline.py`:

* Removes duplicate records
* Separates features (X) and target variable (Class)
* Scales numerical features using **StandardScaler**
* Handles imbalanced data using **SMOTE**
* Splits data into training and testing sets

This prepares clean and balanced data for model training.

---

### 3️⃣ Model Training Methods

Implemented in `train_model.py`:

* Trains Logistic Regression and Random Forest models
* Uses training data to learn fraud patterns
* Saves trained model using `joblib`

```python
model.fit(X_train, y_train)
```

---

### 4️⃣ Model Evaluation

Implemented in `evaluate_model.py`:

* Predicts fraud on test data
* Calculates:

  * Accuracy
  * Precision
  * Recall
  * F1-score
  * ROC-AUC score

These metrics are important because fraud datasets are **highly imbalanced**.

---

### 5️⃣ ROC Curve Calculation

* Uses predicted probabilities
* Calculates False Positive Rate (FPR) and True Positive Rate (TPR)

```python
roc_curve(y_test, y_pred_proba)
```

---

### 6️⃣ Final Plot

* Plots the **ROC Curve** using Matplotlib
* Saves the plot as an image file

```python
plt.plot(fpr, tpr)
```

This helps visualize how well the model distinguishes fraud vs non-fraud transactions.

---

## ▶️ How to Run the Project

### Step 1: Clone the Repository

```bash
git clone https://github.com/your-username/Credit_Card_ML_Pipeline.git
cd Credit_Card_ML_Pipeline
```

### Step 2: Install Requirements

```bash
pip install -r requirements.txt
```

### Step 3: Run the Pipeline

```bash
python main.py
```

This will:

* Load data
* Preprocess data
* Train the model
* Evaluate performance
* Generate ROC curve plot

---

##  Results

* Random Forest performs better than Logistic Regression
* High ROC-AUC score (> 0.98)
* Good recall for fraud detection

| Model               | Precision | Recall | ROC-AUC |
| ------------------- | --------- | ------ | ------- |
| Logistic Regression | 0.91      | 0.84   | 0.98    |
| Random Forest       | 0.95      | 0.89   | 0.99    |

---

##  Requirements

All required libraries are listed in `requirements.txt`:

```
pandas
numpy
scikit-learn
imbalanced-learn
matplotlib
seaborn
joblib
```

---

##  Notes

* Dataset is highly imbalanced
* Accuracy alone is not reliable
* Focus is on Recall and ROC-AUC
* Project follows standard ML pipeline structure

---

## Contributing

Contributions are welcome!

Steps:

1. Fork the repository
2. Create a new branch
3. Make changes and commit
4. Open a pull request

---

> “This project implements an end-to-end ML pipeline for credit card fraud detection including preprocessing, model training, evaluation, and ROC curve visualization.”

---
📄 License

This project is licensed under the MIT License.
