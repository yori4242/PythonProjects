# SBA Loan Default Prediction

## Project Overview

This project focuses on predicting the default risk of Small Business Administration (SBA) loans using machine learning techniques. The goal is to develop a model that can accurately assess the likelihood of a loan defaulting, which can be invaluable for financial institutions and policymakers in making informed lending decisions.

## Dataset

The dataset used in this project is "SBA_loans_project_2.zip", which contains historical data on SBA loans, including various features such as loan amount, borrower information, and loan status.

## Methodology

1. **Data Preprocessing**: 
   - Handling missing values
   - Converting currency strings to float values
   - Encoding categorical variables
   - Target encoding for ZIP codes

2. **Feature Engineering**:
   - Created new features like job change and approval ratios

3. **Model Development**:
   - Utilized LightGBM, a gradient boosting framework
   - Split data into training and test sets
   - Trained the model with binary classification objective

4. **Model Evaluation**:
   - Used binary log loss as the evaluation metric
   - Implemented early stopping to prevent overfitting

5. **Feature Importance Analysis**:
   - Calculated feature importance using LightGBM's built-in method
   - Utilized SHAP (SHapley Additive exPlanations) values for interpretable machine learning

## Key Findings

1. The model's performance metrics are not explicitly stated in the provided document, but the analysis of feature importance and SHAP values provides valuable insights into loan default prediction.

2. Key predictors of loan default, based on SHAP values, include:
   - ZIP_encoded (encoded ZIP code)
   - UrbanRural (whether the area is urban or rural)
   - FranchiseCode
   - A feature engineered for this project: gross_approval_ratio

3. SHAP analysis revealed that:
   - The loan's business and financial characteristics related to Bank, BankState, and NAICS (North American Industry Classification System) are significant predictors.
   - These features provide crucial information about the lender, the borrower's location, and the type of business, which can impact the borrower's ability to repay the loan.
   - Banks and BankState may indicate the lender's familiarity with the local market, while NAICS provides information about the borrower's industry and potential success in that area.

4. The importance of ZIP code as a predictor suggests that the wealth and economic conditions of different areas play a significant role in loan default risk.

5. The urban/rural distinction is also a major contributor, likely reflecting differences in economic opportunities and credit status between urban and rural areas.

6. Some engineered features, particularly 'gross_approval_ratio', have shown to be important predictors, demonstrating the value of feature engineering in this project.

These findings highlight the complex interplay of geographic, economic, and business-specific factors in determining the risk of SBA loan defaults. They provide valuable insights for lenders and policymakers in assessing and managing loan risks.

## Relevance and Potential Impact

1. **Risk Assessment**: This model can help lenders more accurately assess the risk associated with SBA loans, potentially leading to better lending decisions and reduced default rates.

2. **Policy Insights**: Policymakers can use the insights from this model to design more effective loan programs and target support to businesses that are most likely to succeed.

3. **Economic Impact**: By improving the allocation of loans to businesses with higher chances of success, this model could contribute to economic growth and job creation.

4. **Fairness in Lending**: The feature importance analysis can help identify any potential biases in lending practices, promoting more equitable access to capital.

## Future Work

- Explore more advanced feature engineering techniques
- Experiment with ensemble methods to potentially improve model performance
- Conduct a more in-depth analysis of the model's performance across different business sectors or geographic regions

## Dependencies

- pandas
- scikit-learn
- category_encoders
- LightGBM
- SHAP


## Contributors

Iori Koh
