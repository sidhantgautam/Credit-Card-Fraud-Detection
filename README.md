# 🛡️ Credit Card Fraud Detection (Logistic Regression)

This project implements a **Credit Card Fraud Detection System** using **Logistic Regression** in Python.  
The dataset used is highly imbalanced (≈ 284,315 normal vs 492 fraudulent transactions).  
To address this, **under-sampling** was applied to balance the classes, followed by model training and evaluation.

---

## 📂 Project Overview

Fraudulent transactions are rare but critical to detect.  
The project workflow includes:

1. **Data Preprocessing**  
   - Loaded dataset with 284,807 transactions.  
   - Checked for null values (none found).  
   - Separated **legit** vs **fraudulent** transactions.  

2. **Handling Imbalance (Under-Sampling)**  
   - Selected 492 normal transactions to match 492 fraudulent ones.  
   - Created a balanced dataset of **984 transactions (492 legit + 492 fraud)**.  

3. **Feature & Target Split**  
   - Features: All columns except `Class`.  
   - Target: `Class` (0 = Legit, 1 = Fraud).  

4. **Train-Test Split**  
   - 80% training data, 20% testing data.  
   - Stratified split to maintain class balance.  

5. **Model Training (Logistic Regression)**  
   - Trained with `LogisticRegression` from scikit-learn.  
   - Encountered convergence warning → could be fixed with scaling or higher iterations.  

6. **Evaluation Metrics**  
   - Accuracy on Training Data → **94.9%**  
   - Accuracy on Test Data → **91.3%**

---

## ⚙️ Tech Stack

- **Python 3.12**
- **Libraries**:  
  - NumPy  
  - Pandas  
  - scikit-learn  

---

## 📊 Results

- Logistic Regression achieved **91% accuracy on test data**.  
- Fraud detection improved significantly after **balancing the dataset**.  
- This confirms the importance of handling class imbalance in fraud detection systems.

---

## 🚀 Future Improvements

- Try **SMOTE (Synthetic Minority Oversampling)** for better data balancing.  
- Experiment with **Random Forest, XGBoost, and Neural Networks**.  
- Use **ROC-AUC, Precision-Recall, and F1 Score** for more reliable evaluation (since accuracy alone can be misleading on imbalanced data).  

---

## 📁 How to Run

```bash
# Clone the repository
git clone https://github.com/aditipariharr/Credit-Card-Fraud-Detection.git

cd credit-card-fraud-detection

# Install dependencies
pip install -r requirements.txt

# Run Jupyter Notebook or Python script
jupyter notebook fraud_detection.ipynb
# OR
python fraud_detection.py
```

---

## 📌 Dataset

The dataset used is from [Kaggle - Credit Card Fraud Detection](https://www.kaggle.com/mlg-ulb/creditcardfraud).  

