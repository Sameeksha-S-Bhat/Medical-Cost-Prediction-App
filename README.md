# 🏥 Medical Insurance Cost Predictor

A machine learning project that predicts medical insurance costs based on personal health and demographic details — deployed as a live interactive web application using Streamlit.

🔗 **Live App:** [Click here to use the app](https://medical-cost-prediction-app-pdiaewrtyknc5hapnvw7mb.streamlit.app/)

---

## 📊 Overview

Healthcare costs vary greatly across individuals based on factors like age, BMI, smoking status, and lifestyle. By leveraging historical data and regression techniques, this project predicts insurance charges — helping individuals and insurance providers make data-informed decisions.

The model achieves **R² = 0.84 on test data** and is deployed as an interactive web app where users can input their details and receive real-time cost predictions.

---

## 🚀 Live Demo

Try the deployed app here:
**[https://medical-cost-prediction-app-pdiaewrtyknc5hapnvw7mb.streamlit.app/](https://medical-cost-prediction-app-pdiaewrtyknc5hapnvw7mb.streamlit.app/)**

---

## 📂 Dataset

- **Source:** Medical Cost Personal Dataset
- **Size:** 1,338 records (after duplicate removal)
- **Target variable:** Medical insurance charges (INR)

### Features Used

| Feature | Description |
|---------|-------------|
| Age | Age of the individual |
| Sex | Gender (male/female) |
| BMI | Body Mass Index |
| Children | Number of dependent children |
| Smoker | Smoking status (yes/no) |
| Region | Geographic region (northeast, northwest, southeast, southwest) |

---

## 🔍 Methodology

### 1. Data Preprocessing
- Verified no missing values
- Identified and removed duplicate rows
- Label encoding for binary features (sex, smoker)
- One-hot encoding for region column

### 2. Outlier Handling
- Detected outliers using IQR method across all numerical columns
- Applied capping for BMI and charges columns only
- Binary and categorical encoded columns excluded from outlier treatment — skewness in these is not meaningful

### 3. Feature Analysis
- Correlation heatmap revealed smoker status, age, and BMI as the strongest predictors
- Distribution plots and skewness analysis performed on all numerical features

### 4. Model Performance

| Metric | Score |
|--------|-------|
| R² (Training) | 0.9657 |
| R² (Testing) | 0.8365 |
| RMSE | ₹4,370.67 |

> Normalization was intentionally skipped — Random Forest is a tree-based model unaffected by feature scaling.

### 5. Deployment
- Trained model serialized using `pickle`
- Interactive web app built with Streamlit
- Deployed publicly on Streamlit Cloud with a live shareable link

---

## 🚀 Features

- 📈 Real-time insurance cost prediction based on user inputs
- 🧠 Trained ML model using RandomForestRegressor
- 📊 EDA and feature correlation visualizations in Jupyter Notebook
- 💻 Clean Streamlit web interface with two-column layout
- ✅ Deployed via Streamlit Cloud — accessible from any device

---

## 🛠️ Tech Stack

- **Python**
- **Pandas, NumPy** — Data processing
- **Matplotlib, Seaborn** — Data visualization
- **Scikit-learn** — Machine learning model and preprocessing
- **Streamlit** — Web application
- **Streamlit Cloud** — Deployment

---

## 🗂️ Project Structure

```
├── Medical_Cost_App.py           # Streamlit web app
├── medical_model.pkl             # Trained Random Forest model
├── Medical cost analysis.ipynb   # EDA and model training notebook
├── Medical cost Dataset.csv      # Dataset
├── requirements.txt              # Required packages
└── README.md                     # Project documentation
```

---

## ⚙️ Installation

1. Clone the repository
```bash
git clone https://github.com/Sameeksha-S-Bhat/Medical-Cost-Prediction-App.git
```

2. Install dependencies
```bash
pip install -r requirements.txt
```

3. Run the Streamlit app
```bash
streamlit run Medical_Cost_App.py
```

---

## 🧪 How to Use

1. Open the app via the live link or run locally
2. Enter your details:
   - Age
   - Gender
   - BMI (Body Mass Index)
   - Number of Children
   - Smoking Status
   - Geographic Region
3. Click **💰 Predict Medical Cost**
4. The app instantly displays your estimated insurance cost in INR

---

## 📈 Key Learnings

- Normalization is not always necessary — tree-based models are scale-invariant
- Smoking status is the dominant predictor of medical charges, significantly outweighing other features
- IQR outlier treatment must be applied selectively — binary and categorical columns should be excluded
- Deploying an ML model end-to-end requires thinking beyond accuracy — input validation, UI design, and real-time inference all matter

---

## 👩‍💻 Author

**Sameeksha S. Bhat**
B.E. Artificial Intelligence and Data Science, NMIT Bangalore
[GitHub](https://github.com/Sameeksha-S-Bhat) | [LinkedIn](https://linkedin.com/in/sameeksha-s-bhat-2a7341336)

---
## 📄 License
This project is licensed under the MIT License.
