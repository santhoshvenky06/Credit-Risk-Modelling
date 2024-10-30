# Credit-Risk-Modelling

Credit Risk Modeling Project
This project is dedicated to developing a robust credit risk model that predicts the Probability of Default (PD) and extends into risk assessment by calculating Loss Given Default (LGD) and Exposure at Default (EAD). These three metrics are crucial in estimating Expected Loss (EL), which informs financial institutions of potential credit risks and helps in strategic decision-making.

Project Overview
The project leverages machine learning to model and predict credit risk based on historical data, with these main objectives:

Predict Probability of Default (PD): Using logistic regression, decision tree, and random forest models, this project explores how different algorithms perform in predicting the likelihood of default.
Calculate Loss Given Default (LGD): An industry-average LGD is applied, given the lack of recovery data. For future iterations, having historical recovery rates or loss data by loan grade would enhance this model's accuracy.
Estimate Exposure at Default (EAD): Assumed as the full loan amount since detailed exposure data over time is unavailable. More granular data, like undrawn credit lines, could refine EAD calculations.
Expected Loss (EL) Calculation: Combines PD, LGD, and EAD into an EL estimate, providing a comprehensive view of credit risk.
Methodology
Data Preprocessing: Data was cleaned to remove extreme outliers, standardized using feature scaling, and categorical variables were encoded.
Feature Engineering: Key features included loan amount, interest rate, loan intent, and borrower characteristics (e.g., income, employment length).
Model Training: Three models (logistic regression, decision tree, and random forest) were used to predict PD, with hyperparameter tuning to optimize each.
Risk Metrics Calculation: LGD and EAD were estimated and incorporated to compute Expected Loss, extending the model’s practical utility.
Key Findings
Model Performance: Among the models tested, random forests typically performed the best, yielding up to ~85% accuracy in predicting defaults.
Comprehensive Risk Assessment: By calculating PD, LGD, EAD, and EL, the model offers a holistic view of credit risk, aligning with industry standards.
Shortcomings and Limitations
Data Limitations:
Lack of Recovery Data: LGD is a key metric in credit risk, representing the portion of a loan lost after a borrower defaults. This model assumes a static industry-average LGD due to the absence of detailed recovery data, which limits precision. Access to recovery rates or loss data by loan type or grade would improve this calculation.
Simplistic EAD Calculation: Without detailed exposure data over time or undrawn credit line data, the model assumes EAD is equal to the full loan amount. In reality, some loans might not be fully drawn at default, or revolving credits may have undrawn balances.
Model Limitations:
Limited PD Model Inputs: The dataset lacks some relevant borrower financial health indicators (e.g., credit scores, debt-to-income ratio), which could further improve PD model accuracy.
LGD and EAD Model Assumptions: The use of a static LGD and simplistic EAD could result in a less responsive model to varying loan risk profiles. Ideally, more granular loan and borrower data would allow LGD and EAD to be modeled as functions of borrower and loan characteristics.
Operational Limitations:
Scalability: This model is designed for exploratory analysis. In production, the model would require consistent data updates, retraining, and recalibration to stay relevant with changing credit conditions.
Future Enhancements
Future enhancements could include:

Integrating more borrower-level data (e.g., credit scores, income stability) to refine PD calculations.
Incorporating historical recovery and undrawn exposure data to dynamically model LGD and EAD.
Exploring deep learning approaches or ensemble methods to potentially enhance PD model accuracy further.
