🧬 Predicting Metabolic Syndrome Using Machine Learning
This project aims to develop machine learning models for the early prediction of Metabolic Syndrome (MetS)—a cluster of metabolic disorders including hypertension, diabetes, obesity, and dyslipidemia. The study focuses on the Pakistani population, using real-world clinical and lifestyle data to build interpretable models that can support early diagnosis and targeted interventions.


📊 Dataset Overview
Total samples: 502 individuals
MetS prevalence: 56.6%
Source: Private healthcare facilities across five cities in Pakistan
Features: 24 variables covering anthropometric, clinical, lifestyle, dietary, and behavioral factors
Examples: Blood pressure, fasting blood sugar, BMI, triglycerides, HDL, physical activity, sleep hours, stress, and smoking habits


🛠️ Data Preprocessing
- Missing Value Imputation:
Handled ~5.4% missing values using K-Nearest Neighbors (KNN) imputation (k=5)

- Categorical Feature Encoding:
Applied one-hot encoding to categorical features like gender, activity level, sleep duration, and smoking status

- Feature Standardization:
Used z-score normalization to ensure all features were on the same scale

- Train-Test Split:
Performed stratified 70/30 split to preserve MetS distribution across training and testing sets


🤖 Model Training & Evaluation
A total of 15 supervised learning models were trained and evaluated:

Machine Learning Models:
Random Forest, XGBoost, Logistic Regression, SVM, KNN, Gradient Boosting, LightGBM, Decision Tree, Naïve Bayes, LDA, QDA, AdaBoost

Deep Learning Models:
Artificial Neural Networks (ANN), Feedforward Neural Network (FNN), Multilayer Perceptron (MLP)

Evaluation Metrics:
Accuracy, Precision, Recall, F1 Score, ROC-AUC

Models were validated using 5-fold cross-validation

Best Performing Model:
XGBoost with an AUC of 0.934, followed by AdaBoost and Gradient Boosting


📉 Feature Importance Analysis
To enhance model interpretability and identify key diagnostic markers:
Permutation Feature Importance was applied to the trained XGBoost model

Top Predictors:
Systolic Blood Pressure (SBP)
Fasting Blood Sugar (FBS)
Triglycerides (TG)
Obesity (BMI)
HDL cholesterol


🧠 Model Explainability using SHAP
SHAP (SHapley Additive Explanations) was used to visualize feature impacts on predictions
- Findings confirmed that SBP, FBS, TG, and obesity had the most significant positive contribution toward MetS classification
- HDL showed a protective (negative) association
- 

⚖️ Risk Factor Stratification (Odds Ratio Analysis)
Odds ratio (OR) was calculated to assess risk factor strength across:
- Three age groups: 18–44, 45–59, and 60+
- Both genders
- Analysis revealed age- and gender-specific patterns, reinforcing the model’s clinical relevance and supporting personalized intervention strategies
  

✅ Key Findings
- XGBoost showed the highest predictive performance

- Major predictors of MetS include SBP, FBS, TG, obesity, and low HDL

- Integrating clinical, lifestyle, and demographic data improves prediction accuracy

- The study presents one of the first ML-based MetS prediction models tailored to the Pakistani population

📁 Files
MetS_Prediction.ipynb: Full pipeline, from data preprocessing to model training, evaluation, and interpretation

