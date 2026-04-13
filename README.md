📌 Credit Card Fraud Detection using Machine Learning & Deep Learning
🧠 Project Overview

This project aims to detect fraudulent credit card transactions using multiple machine learning, deep learning, and anomaly detection techniques.
Due to the highly imbalanced nature of the dataset, different strategies such as SMOTE, class weighting, and anomaly detection were applied to improve model performance.

🎯 Problem Statement

Credit card fraud is a major financial risk. Fraudulent transactions are rare compared to legitimate ones, making detection challenging.

This project focuses on:

Identifying fraudulent transactions
Handling class imbalance
Comparing multiple modeling approaches
📊 Dataset
Source: Credit Card Fraud Dataset
Features: 30 numerical features (PCA-transformed: V1–V28, Time, Amount)
Target:
0 → Legitimate transaction
1 → Fraudulent transaction
⚙️ Workflow
1️⃣ Data Preprocessing
Loaded dataset using Pandas
Handled missing values using dropna()
Removed duplicates
Exploratory Data Analysis (EDA)
Class distribution
Boxplots for outlier detection
Correlation heatmap
2️⃣ Feature Engineering
Feature scaling using RobustScaler
Outlier detection using IQR method
Correlation analysis with target variable
3️⃣ Handling Imbalanced Data

Since fraud cases are extremely rare:

SMOTE (Synthetic Minority Over-sampling Technique) was applied
Class weighting was used in Random Forest
Stratified splitting was used for fair evaluation
🤖 Models Used
🔹 1. Gaussian Naive Bayes
Baseline probabilistic model
Achieved high accuracy (~98%)
Good performance but weak on minority class
🔹 2. SMOTE + Naive Bayes
Improved balance between classes
Better recall for fraud detection
More stable performance
🔹 3. Random Forest Classifier
Used with class_weight='balanced'
Strong performance on imbalanced data
Better recall for fraud class compared to baseline models
🔹 4. Gaussian Anomaly Detection Model
Based on multivariate Gaussian distribution
Trained only on normal transactions
Detects anomalies using probability threshold
Tuned epsilon for best F1-score
🔹 5. Deep Learning Model (TensorFlow)

Architecture:

Input Layer (30 features)
Dense layers: 70 → 50 → 30 → 10
Output layer: Sigmoid activation
Optimizer: Adam
Loss: Binary Crossentropy
Trained for 100 epochs

✔ Achieved very high accuracy (~99%+)

📈 Evaluation Metrics

Models were evaluated using:

Accuracy
Precision
Recall
F1-score
Confusion Matrix

Special focus on:

Fraud class recall (important for real-world usage)
📊 Key Results
Strong imbalance handling significantly improved recall
Random Forest and Neural Network performed best overall
Anomaly Detection worked well for rare fraud cases
SMOTE improved minority class detection

🧪 Technologies Used
Python
Pandas, NumPy
Matplotlib, Seaborn
Scikit-learn
Imbalanced-learn (SMOTE)
TensorFlow / Keras
SciPy
🚀 Future Improvements
Try XGBoost / LightGBM for better performance
Hyperparameter tuning (GridSearch / Optuna)
Deploy model using Flask or Streamlit
Add real-time fraud detection API
Improve deep learning architecture with regularization
👩‍💻 Author

Mai Kamal
AI & Data Science Student
Machine Learning & Deep Learning Enthusiast
