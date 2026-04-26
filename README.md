# Churn-Prediction-Model

📌 Project Overview

This project builds a machine learning model to predict customer churn using historical customer data. The goal is to identify customers who are likely to leave, enabling businesses to take preventive actions.

🎯 Objective

Predict customer churn (Yes/No → 1/0)
Analyze customer behavior patterns
Improve model performance using multiple algorithms

📂 Dataset

File used: Churn.xlsx
Loaded using Pandas:
df = pd.read_excel("Churn.xlsx")

🔑 Features include:

Customer demographics
Subscription services
Monthly & total charges
Tenure
Churn (Target variable)

⚙️ Technologies Used

Python 🐍
Pandas
NumPy
Scikit-learn
Seaborn
Matplotlib
Joblib

🔄 Project Workflow

1. Data Understanding
Viewed dataset using .head()
Checked statistics using .describe()
Verified missing values using .isnull().sum()
Checked data types

2. Data Preprocessing
Handled missing values
Converted categorical variables
Feature scaling applied using StandardScaler

3. Model Building
✅ Logistic Regression Model
Trained using scaled data
Used for baseline prediction

🌲 Random Forest Model
Applied for improved accuracy
Captures non-linear relationships

4. Model Evaluation
Confusion Matrix
Precision
Recall
F1 Score

📊 Confusion matrix visualization:

sns.heatmap(lr_cm, annot=True, fmt='d', cmap="Blues")

📈 Results

Compared Logistic Regression & Random Forest
Evaluated performance using classification metrics
Focused on improving recall (important for churn detection)

💾 Model Saving

Models are saved for future use:
import joblib

joblib.dump(lr_model, "Churn_Prediction_Model.pkl")
joblib.dump(scaler, "scaler.pkl")

🚀 How to Run the Project

1.Clone repository:
2.Install dependencies:
pip install pandas numpy scikit-learn matplotlib seaborn joblib
3. Run Jupyter Notebook:
4.Open:
Churn Prediction Model.ipynb

🧪 Testing with New Data
Load saved model using joblib
Apply same preprocessing (scaling)
Use:
model.predict(new_data)

📊 Future Improvements

Hyperparameter tuning (GridSearchCV)
Try advanced models (XGBoost, LightGBM)
Handle class imbalance (SMOTE)
Deploy using Streamlit or Flask

📌 Key Learnings

Data preprocessing is critical for model performance
Recall is more important than accuracy in churn problems
Visualization helps understand model performance clearly

👨‍💻 Author

Afrith Basha
