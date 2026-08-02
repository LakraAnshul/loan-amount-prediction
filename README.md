<div align="center">

<img src="https://img.shields.io/badge/💰-LoanCast-10b981?style=for-the-badge&labelColor=0d1117" alt="LoanCast" height="40"/>

# LoanCast: AI-Powered Loan Amount Predictor

**Predict approved loan amounts using Machine Learning and applicant profiling**

<br/>

[![Streamlit App](https://img.shields.io/badge/Streamlit-Live_App-FF4B4B?style=flat-square&logo=streamlit&logoColor=white)](https://loan-amount-prediction-cxudxsgasrs8chpdz2t8rh.streamlit.app/)
&nbsp;&nbsp;
[![Python version](https://img.shields.io/badge/Python-3.10%2B-3776AB?style=flat-square&logo=python&logoColor=white)](https://www.python.org/)
&nbsp;&nbsp;
[![Type of ML](https://img.shields.io/badge/Machine%20Learning-Regression-blue?style=flat-square)](https://scikit-learn.org/)
&nbsp;&nbsp;
[![License](https://img.shields.io/badge/License-MIT-green?style=flat-square)](LICENSE)

<br/>

<a href="https://loan-amount-prediction-cxudxsgasrs8chpdz2t8rh.streamlit.app/">
  <img src="https://img.shields.io/badge/🚀_Try_the_Live_Demo-Click_Here-10b981?style=for-the-badge&labelColor=0d1117" alt="Live Demo" height="35"/>
</a>

<br/><br/>
</div>

---

## 🎯 What is LoanCast?

**LoanCast** is an intelligent regression-based web application that predicts the exact loan amount an applicant is likely to be approved for. By analyzing financial and demographic features such as credit scores, income stability, property values, and co-applicant status, the model provides data-driven financial insights.

> **Key Finding:** Applicants with high credit scores and a reliable co-applicant are significantly more likely to receive larger loan approvals.

---

## ⚡ Key Capabilities

```
┌─────────────────────────────────────────────────────────────────┐
│                                                                 │
│   🧠  Machine Learning   Trained Random Forest Regressor model  │
│   ☁️  AWS Integration    Model weights securely hosted on S3    │
│   🎛️  Custom Pipeline    Automated outlier & missing imputation │
│   📊  Interactive UI     Adjust parameters in real-time         │
│   📈  Data Analytics     Feature importance & RMSE evaluation   │
│                                                                 │
└─────────────────────────────────────────────────────────────────┘
```

---

## 🏗️ Architecture & Pipeline

```
                    ┌──────────────────────┐
                    │   Streamlit Web UI   │
                    │ (loan_amount_app.py) │
                    └──────────┬───────────┘
                               │
            ┌──────────────────▼──────────────────┐
            │        Data Preprocessing           │
            │  (Outliers, Imputation, MinMax)     │
            └──────────────────┬──────────────────┘
                               │
            ┌──────────────────▼──────────────────┐
            │      AWS S3 Bucket (loanamount)     │
            │   (Downloads trained .joblib model) │
            └──────────────────┬──────────────────┘
                               │
                    ┌──────────▼───────────┐
                    │ Random Forest Engine │
                    │ (Predicts USD Amount)│
                    └──────────────────────┘
```

---

## 🔧 Tech Stack

| Component | Technology | Purpose |
|:------|:-----------|:--------|
| **UI Framework** | [Streamlit](https://streamlit.io/) | Interactive web interface |
| **Data Processing** | [Pandas](https://pandas.pydata.org/) / [NumPy](https://numpy.org/) | Data manipulation and linear algebra |
| **Machine Learning** | [scikit-learn](https://scikit-learn.org/) | Pipelines, encoders, and Random Forest |
| **Cloud Storage** | [AWS S3 (boto3)](https://aws.amazon.com/s3/) | Hosting the trained model artifact |
| **Serialization** | [Joblib](https://joblib.readthedocs.io/) | Model saving and loading |

---

## 📊 Model Evaluation

Several regression models were tested during development. **Random Forest** consistently yielded the lowest Root Mean Square Error (RMSE).

| Model | RMSE |
|-------|------|
| **Random Forest (Selected)** | **20791.86** |
| Bagging Regressor | 20780.02 |
| Gradient Boosting | 26974.42 |

### Feature Importance
Based on the analysis:
* **Most Predictive Features**: Requested loan amount, credit score, and presence of a co-applicant.
* **Least Predictive Features**: Expense types and gender.

---

## 🚀 Quick Start

### Prerequisites
- **Python 3.10+** installed
- **pip** package manager

### 1️⃣ Clone & Navigate
```bash
git clone https://github.com/LakraAnshul/loan-amount-prediction.git
cd loan-amount-prediction
```

### 2️⃣ Install Dependencies
```bash
pip install -r requirements.txt
```

### 3️⃣ AWS Credentials (Optional for local run)
The app downloads the trained model from an AWS S3 bucket. You need to configure your AWS secrets in Streamlit.
Create a `.streamlit/secrets.toml` file in your root folder:
```toml
access_key = "YOUR_AWS_ACCESS_KEY"
secret_access_key = "YOUR_AWS_SECRET_KEY"
```

### 4️⃣ Launch the App
```bash
streamlit run loan_amount_app.py
```
The app opens at **`http://localhost:8501`**.

---

## 📂 Repository Structure

```
.
├── assets/                               # Visual assets and images
├── datasets/                             # Train and test datasets
├── .gitignore                            # Ignored files
├── LICENSE                               # MIT License
├── Loan_amount_prediction.ipynb          # Jupyter notebook with EDA & Modeling
├── loan_amount_app.py                    # Main Streamlit application
├── requirements.txt                      # Project dependencies
└── README.md                             # You are here
```

---

## 🤝 Contributing

Contributions, issues, and feature requests are welcome!

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

---

## 📜 License

Distributed under the **MIT License**. See [`LICENSE`](LICENSE) for details.

---

<div align="center">

### 👨‍💻 Author

**Anshul Pratap Lakra**

[![GitHub](https://img.shields.io/badge/GitHub-LakraAnshul-181717?style=flat-square&logo=github)](https://github.com/LakraAnshul)

<sub>Built with 🔥 Streamlit &bull; Scikit-Learn &bull; AWS</sub>

</div>
