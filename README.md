## Project Progress Summary

This project explores the Kaggle **House Prices** dataset with a focus on building a clean, realistic machine learning workflow rather than leaderboard optimization.

### What Has Been Done

- Built a **baseline Linear Regression** model
- Evaluated models using **K-Fold Cross-Validation (RMSE)**
- Implemented a full **scikit-learn Pipeline** to prevent data leakage
- Handled missing values in a principled way:
  - Numeric features → median or zero (when absence is meaningful)
  - Categorical features → `"None"` for non-existent attributes, mode otherwise
- Applied **One-Hot Encoding** for categorical variables
- Added **Ridge Regression** and tuned the regularization parameter (`alpha`)
- Extracted and analyzed model coefficients
- Learned correct interpretation of coefficients using **reference categories**

### Key Observations

- Coefficients in one-hot encoded linear models are **relative to a reference category**
- Sparse categorical features lead to unstable and unintuitive coefficients
- Regularization reduces variance but does not fix model expressiveness

### Conclusion

Even with proper preprocessing, encoding, regularization, and evaluation,  
**Linear Regression performs poorly on this dataset (~34k RMSE)**.

This indicates a **model mismatch**, not an implementation issue.

➡️ Linear models are not suitable for this problem.  
➡️ The next step is to explore **more expressive, non-linear models** (e.g. tree-based methods).
