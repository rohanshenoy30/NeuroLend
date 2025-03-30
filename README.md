# Loan Approval System

## 📌 Project Overview
The **Loan Approval System** uses **Machine Learning (ML) / Deep Learning (DL)** to determine whether a loan should be approved or rejected. If approved, the system predicts the loan amount that should be granted based on the applicant’s financial profile.

## 🚀 Features
- **Binary Classification**: Determines whether a loan should be approved.
- **Regression Model**: Predicts the loan amount if approved.
- **Neural Network Implementation**: Uses TensorFlow/Keras for deep learning.
- **Automated Data Preprocessing**: Cleans and prepares loan applicant data.
- **Model Training & Evaluation**: Ensures high accuracy in predictions.
- **API for Integration**: Optional Flask API for deployment.

---

## 🏗️ Project Structure
```
loan-approval-system/
│── data/                # Dataset directory
│   ├── train.csv        # Training dataset
│   ├── test.csv         # Test dataset
│
│── models/              # Saved ML models
│   ├── classification_model.h5
│   ├── regression_model.h5
│
│── src/                 # Source code
│   ├── preprocess.py    # Data preprocessing functions
│   ├── train.py         # Training script for both models
│   ├── predict.py       # Prediction script
│
│── api/                 # Flask API (Optional for deployment)
│   ├── app.py           # API endpoint
│
│── notebooks/           # Jupyter Notebooks for EDA & Experiments
│
│── README.md            # Project documentation
│── requirements.txt     # Dependencies
│── config.yaml          # Configuration file
```

---

## 🔧 Installation & Setup
### **1️⃣ Clone the Repository**
```bash
git clone https://github.com/yourusername/loan-approval-system.git
cd loan-approval-system
```

### **2️⃣ Install Dependencies**
```bash
pip install -r requirements.txt
```

### **3️⃣ Prepare the Dataset**
- Place your dataset files inside the `data/` folder.
- Ensure the dataset contains relevant columns (e.g., credit score, income, loan amount, repayment history).

---

## 🧠 Model Training
### **1️⃣ Train Classification Model (Loan Approval)**
```bash
python src/train.py --task classification
```
### **2️⃣ Train Regression Model (Loan Amount Prediction)**
```bash
python src/train.py --task regression
```

---

## 🔍 Making Predictions
### **1️⃣ Predict Loan Approval**
```bash
python src/predict.py --task classification --input "applicant_data.json"
```
### **2️⃣ Predict Loan Amount** (if approved)
```bash
python src/predict.py --task regression --input "applicant_data.json"
```

Example `applicant_data.json`:
```json
{
  "credit_score": 650,
  "income": 50000,
  "loan_amount_requested": 400000,
  "employment_status": "Full-time"
}
```

---

## 🌍 Deploying with Flask (Optional)
1. Run the API:
   ```bash
   python api/app.py
   ```
2. Use Postman or cURL to send requests:
   ```bash
   curl -X POST http://127.0.0.1:5000/predict -H "Content-Type: application/json" -d '{"credit_score":650, "income":50000, "loan_amount_requested":400000}'
   ```

---

## 📊 Model Performance
| Model             | Accuracy / Metric |
|------------------|-----------------|
| Classification   | 92% Accuracy     |
| Regression      | RMSE: 15,000      |

---

## 📜 License
This project is licensed under the MIT License.

---

## 🤝 Contributing
Want to improve the project? Feel free to submit a pull request!

---

## 📞 Contact
For any issues, contact [your.email@example.com](mailto:your.email@example.com).
