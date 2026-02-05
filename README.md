# House Prices Project
This project predicts house prices using Kaggle dataset.


  Project Progress Summary (So Far)
  Project: House Prices – Advanced Regression Techniques (Kaggle)

  Phase 0 – Setup
Created a GitHub repository for the project
Set up a Jupyter notebook and README
Downloaded and loaded train.csv and test.csv
Kept train and test datasets separate from the start

  Phase 1 – Initial Data Exploration
Identified SalePrice as the target variable
Separated numeric and categorical features
Inspected dataset shape and column types
Analyzed missing values and identified columns with missing data

  Noted early challenges:
Many missing values
Many categorical features
Data that looks clean at first glance but hides complexity

  Phase 2 – Baseline Model
Built an initial baseline using:
Numeric features only
Linear Regression
Handled missing values initially by dropping rows with missing data
Removed identifier columns (e.g., Id) to avoid leakage
Trained and evaluated the model using a train/test split
Observed that performance looked reasonable but might be misleading
Cross-Validation (Reality Check)
Introduced 5-fold cross-validation using RMSE

  Learned that:
Single train/test splits can give overly optimistic results
Model performance varied significantly across folds
Observed that the baseline model is noisy
Realized earlier results were likely influenced by a lucky split

  Conclusion:
Cross-validation is necessary to judge model stability
Improvements must be larger than natural CV variance to be meaningful

  Key Lessons So Far
A working model does not mean a trustworthy model
Missing data is part of the real problem, not something to ignore
Linear regression can survive on strong numeric signals but hides weaknesses
Cross-validation changes how model performance should be interpreted
Data science is about making defensible decisions, not perfect ones
