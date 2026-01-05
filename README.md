# Credit_Card-ML_Pipeline

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
    <title>Credit Card Fraud Detection | ML Pipeline</title>

    <style>
        body {
            font-family: Arial, Helvetica, sans-serif;
            background-color: #f4f6f8;
            color: #333;
            line-height: 1.6;
            margin: 0;
            padding: 0;
        }

        header {
            background: #0b5ed7;
            color: white;
            padding: 20px;
            text-align: center;
        }

        section {
            background: white;
            margin: 20px auto;
            padding: 20px;
            max-width: 900px;
            border-radius: 6px;
            box-shadow: 0 2px 6px rgba(0,0,0,0.1);
        }

        h2 {
            color: #0b5ed7;
            border-bottom: 2px solid #eee;
            padding-bottom: 5px;
        }

        ul {
            margin-left: 20px;
        }

        code, pre {
            background: #f1f1f1;
            padding: 10px;
            display: block;
            border-radius: 5px;
            overflow-x: auto;
        }

        table {
            width: 100%;
            border-collapse: collapse;
            margin-top: 10px;
        }

        table, th, td {
            border: 1px solid #ccc;
        }

        th {
            background: #e9ecef;
        }

        th, td {
            padding: 10px;
            text-align: center;
        }

        footer {
            text-align: center;
            padding: 15px;
            background: #222;
            color: white;
            margin-top: 30px;
        }
    </style>
</head>
<body>

<header>
    <h1>💳 Credit Card Fraud Detection</h1>
    <p>Machine Learning Pipeline Project</p>
</header>

<section>
    <h2>📌 Project Overview</h2>
    <p>
        This project implements an end-to-end <b>Machine Learning pipeline</b> to detect
        fraudulent credit card transactions. The system loads transaction data,
        preprocesses it, trains ML models, evaluates performance, and visualizes results
        using an ROC curve.
    </p>
</section>

<section>
    <h2>🤖 Models Implemented</h2>
    <ul>
        <li>Logistic Regression (Baseline Model)</li>
        <li>Random Forest Classifier</li>
    </ul>
</section>

<section>
    <h2>📂 Project Structure</h2>
<pre>
Credit_Card_ML_Pipeline/
├── data/
│   └── creditcard.csv
├── src/
│   ├── data_pipeline.py
│   ├── train_model.py
│   ├── evaluate_model.py
├── models/
│   └── fraud_model.pkl
├── plots/
│   └── roc_curve.png
├── main.py
├── requirements.txt
└── README.md
</pre>
</section>

<section>
    <h2>⚙️ How the Code Works</h2>
    <ul>
        <li>Load credit card transaction dataset</li>
        <li>Clean and preprocess data</li>
        <li>Scale features using StandardScaler</li>
        <li>Handle imbalanced data using SMOTE</li>
        <li>Train ML models</li>
        <li>Evaluate using ROC-AUC and other metrics</li>
    </ul>
</section>

<section>
    <h2>🔁 Credit Card Initialization & Preprocessing</h2>
    <p>
        The dataset is loaded from a CSV file using Pandas. Duplicate records are removed,
        features and target labels are separated, and numerical values are scaled.
    </p>
</section>

<section>
    <h2>🏋️ Model Training</h2>
    <p>
        Models are trained using training data. Random Forest is used as the primary model
        because it performs well on imbalanced datasets.
    </p>
</section>

<section>
    <h2>📈 ROC Curve Calculation & Final Plot</h2>
    <p>
        The ROC curve is calculated using predicted probabilities to evaluate model
        performance. The final ROC curve is plotted and saved as an image.
    </p>
</section>

<section>
    <h2>▶️ How to Run the Project</h2>
<pre>
git clone https://github.com/your-username/Credit_Card_ML_Pipeline.git
cd Credit_Card_ML_Pipeline
pip install -r requirements.txt
python main.py
</pre>
</section>

<section>
    <h2>📊 Results</h2>
    <table>
        <tr>
            <th>Model</th>
            <th>Precision</th>
            <th>Recall</th>
            <th>ROC-AUC</th>
        </tr>
        <tr>
            <td>Logistic Regression</td>
            <td>0.91</td>
            <td>0.84</td>
            <td>0.98</td>
        </tr>
        <tr>
            <td>Random Forest</td>
            <td>0.95</td>
            <td>0.89</td>
            <td>0.99</td>
        </tr>
    </table>
</section>

<section>
    <h2>📦 Requirements</h2>
    <ul>
        <li>Python 3.x</li>
        <li>Pandas</li>
        <li>NumPy</li>
        <li>Scikit-learn</li>
        <li>Imbalanced-learn</li>
        <li>Matplotlib</li>
        <li>Joblib</li>
    </ul>
</section>

<section>
    <h2>📝 Notes</h2>
    <ul>
        <li>Dataset is highly imbalanced</li>
        <li>ROC-AUC and Recall are key metrics</li>
        <li>Accuracy alone is not reliable</li>
    </ul>
</section>

<section>
    <h2>🤝 Contributing</h2>
    <p>
        Contributions are welcome! Fork the repository, create a branch,
        make your changes, and submit a pull request.
    </p>
</section>

<footer>
    <p>⭐ Credit Card Fraud Detection ML Pipeline | Fresher-Friendly Project</p>
</footer>

</body>
</html>


