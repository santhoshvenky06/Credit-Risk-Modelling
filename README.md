Credit Risk Modeling Project
This project develops a robust credit risk model to predict the Probability of Default (PD) and extends into risk assessment by calculating Loss Given Default (LGD) and Exposure at Default (EAD). These metrics are crucial in estimating Expected Loss (EL), helping financial institutions assess potential credit risks and make informed decisions.

Project Overview
The project leverages machine learning to model and predict credit risk based on historical data, with these main objectives:

Predict Probability of Default (PD): Using logistic regression, decision tree, and random forest models to predict the likelihood of default.
Calculate Loss Given Default (LGD): An industry-average LGD is applied due to a lack of recovery data. Future improvements would benefit from historical recovery rates or loss data by loan grade.
Estimate Exposure at Default (EAD): EAD is assumed as the full loan amount due to limited exposure data. More granular data, such as undrawn credit lines, could refine EAD.
Expected Loss (EL) Calculation: Combining PD, LGD, and EAD into an EL estimate provides a comprehensive view of credit risk.
Methodology
Data Preprocessing: Data was cleaned, standardized, and categorical variables were encoded.
Feature Engineering: Key features included loan amount, interest rate, loan intent, and borrower characteristics (e.g., income, employment length).
Model Training: Three models (logistic regression, decision tree, and random forest) were used to predict PD, with hyperparameter tuning to optimize each.
Risk Metrics Calculation: LGD and EAD were estimated and used to compute Expected Loss, enhancing the model’s risk assessment capabilities.
Key Findings
Model Performance: Random forests performed the best, yielding up to ~85% accuracy in predicting defaults.
Comprehensive Risk Assessment: The model calculates PD, LGD, EAD, and EL, aligning with industry-standard risk metrics.
Shortcomings and Limitations
Data Limitations
Lack of Recovery Data: The model assumes a static industry-average LGD due to missing recovery data, limiting precision. Access to recovery rates by loan type would improve accuracy.
Simplistic EAD Calculation: Without detailed exposure data or undrawn credit line information, the model assumes EAD equals the full loan amount. In practice, undrawn balances could alter EAD.
Model Limitations
Limited PD Model Inputs: The dataset lacks important borrower indicators (e.g., credit scores, debt-to-income ratio) that could improve PD accuracy.
LGD and EAD Model Assumptions: Using static LGD and EAD values could result in a less responsive model to loan risk variations. More granular loan and borrower data would allow LGD and EAD to be dynamic.
Operational Limitations
Scalability: The model is for exploratory analysis. In production, it would need regular updates, retraining, and recalibration.
Future Enhancements
Adding more borrower data (e.g., credit scores, income stability) to improve PD predictions.
Including historical recovery and exposure data to dynamically model LGD and EAD.
Testing ensemble methods or deep learning approaches to further enhance PD model accuracy.
This project establishes a foundational framework for credit risk assessment, which can be improved with additional data and modeling techniques. The README details the methodology, limitations, and potential improvements to encourage further development.
