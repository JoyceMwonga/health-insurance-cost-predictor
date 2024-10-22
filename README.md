# Health Insurance Cost Predictor

## 📋 Table of Contents
- [Project Overview](#project-overview)
- [Problem Statement](#problem-statement)
- [Technical Process](#technical-process)
- [Key Findings](#key-findings)
- [Recommendations](#recommendations)
- [Repository Structure](#repository-structure)
- [Installation & Usage](#installation--usage)

## 🎯 Project Overview
- **Domain**: Healthcare
- **Dataset**: [Medical Cost Personal Datasets](https://www.kaggle.com/mirichoi0218/insurance), 1,338 records, 6 features related to personal attributes and medical expenses.
- **Goal**: To predict individual medical insurance costs based on personal attributes such as age, BMI, number of children, smoking habits, and region.
- **Skills Demonstrated**: Data preprocessing, exploratory data analysis (EDA), regression modeling, feature engineering, model evaluation, hyperparameter tuning.

## 💡 Problem Statement

### Business Context
- **Industry Background**: Health insurance companies need to accurately predict insurance premiums to manage risk and ensure profitability.
- **Current Challenges**: High variability in medical costs due to lifestyle factors, making premium calculation complex.
- **Stakeholder Needs**: Insurance companies require a model that predicts medical costs based on customer information to adjust premiums accordingly and reduce potential losses.

### Analysis Objectives
- **Specific Questions**: How can personal factors like age, smoking habits, and BMI influence an individual's medical insurance cost?
- **Expected Business Impact**: Better understanding and prediction of medical costs allow for more accurate premium pricing, reducing risks of loss for insurers.
- **Success Metrics**: Model accuracy measured by R-squared and overall predictive performance.

## 🔧 Technical Process

### Data Collection & Preprocessing
- **Data Sources**: The dataset is sourced from Kaggle, containing demographic and health-related features.
- **Cleaning Steps**: No missing values in the dataset. Outliers were examined but not removed.
- **Feature Engineering**: Feature scaling and encoding for categorical variables were applied (e.g., encoding smoker status, gender).
- **Tools**: Python, Pandas, Scikit-learn for data manipulation and preprocessing.

### Exploratory Data Analysis
- **Initial Findings**: Age, BMI, and smoking habits are strongly correlated with medical insurance costs. Smokers tend to have significantly higher costs than non-smokers.
  ![Heatmap](https://github.com/user-attachments/assets/34fd4173-d369-4b5f-a9d9-f71bddf5716b)
- **Key Variables Identified**: Age, BMI, and smoking status are the most influential factors.
- **Visualizations**: Correlation heatmaps, pair plots, and distribution charts were used to explore relationships between features and the target variable.
  ![AgevsCharges](https://github.com/user-attachments/assets/31755998-bebd-47c9-8139-7ed36d0e3a1c)
  ![BMIvsCharges](https://github.com/user-attachments/assets/9fcdb4e1-6ea0-4bec-a203-3c1bd48866d0)
  ![SmokervsCharges](https://github.com/user-attachments/assets/4d2bade4-ac0f-4cef-82cf-ba2f8e70f0b4)

### Analysis/Modeling
- **Methodology**: A Random Forest Regressor was selected due to its ability to handle non-linear relationships in the data, outperforming simpler models like Linear Regression.
- **Implementation**: The Random Forest model was tuned using GridSearchCV to optimize parameters such as the number of estimators and max depth.
- **Validation**: Cross-validation was performed, and the model achieved an R-squared score of 0.88 on the test data.
- **Challenges**: Some multicollinearity between features, particularly age and BMI, was handled using feature selection and a non-linear model.

### Tools & Technologies Used
- **Programming Languages**: Python
- **Libraries/Frameworks**: Pandas, Numpy, Matplotlib, Seaborn, Scikit-learn
- **Visualization Tools**: Seaborn, Matplotlib
- **Model Persistence**: Pickle for saving the trained model.

## 📊 Key Findings
- **Primary Insights**: The most significant contributors to high medical insurance costs are age, BMI, and smoking status. Smokers incur much higher costs than non-smokers, and older individuals tend to have higher premiums due to increased medical expenses.
- **Business Implications**: Insurance companies can adjust premiums based on these factors to better reflect individual risk.
- **Supporting Visualizations**: Feature importance plots and correlation matrices highlighted the influence of key variables on medical costs.

## 🎖️ Recommendations

### Strategic Actions
- **Wellness Programs**: Encourage wellness initiatives focusing on smoking cessation and healthy weight management to reduce medical expenses.
- **Risk-Based Pricing**: Implement dynamic pricing models based on personal risk factors like smoking and BMI.
- **Feature Expansion**: Collect additional data on pre-existing conditions and healthcare utilization to improve model accuracy further.

### Impact Assessment
- **Potential ROI**: More accurate premium pricing could increase profitability for insurers by better aligning premiums with risk.
- **Implementation Timeline**: A phased approach over 6 months to collect new data and refine the model.
- **Resource Requirements**: Data engineering support, medical professionals for health programs, model deployment resources.
- **Risk Considerations**: Privacy concerns related to health data must be managed carefully, particularly regarding smoking and health-related behavior.
