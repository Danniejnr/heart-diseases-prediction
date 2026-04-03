# Heart Disease Prediction

Predicting heart disease using ML models with UCI dataset — from data cleaning to exploratory analysis.

## Day 1
- Dataset loaded and cleaned
- Target variable converted to binary
- Ready for exploratory data analysis

## Day 2
- Performed exploratory data analysis (EDA)
- Visualized distributions using histograms and boxplots
- Built correlation matrix to identify key features
- Key features identified: thal, ca, oldpeak
- Observed negative relationship with thalach

### Day 3: First ML Model
- Built first Logistic Regression model.
- Applied feature selection to pick key variables.
- Performed evaluation to check accuracy and other metrics.
- Learned how features impact model performance.

## Day 4
- Implemented a Decision Tree model for comparison.
- Evaluated model performance against Logistic Regression.
- Achieved ~75% accuracy with Decision Tree.
- Observed lower performance compared to Logistic Regression (~90%).
- Identified overfitting as a likely cause.
- Learned that increased model complexity does not guarantee better results.

  ## Day 5

- Tuned Decision Tree model to reduce overfitting (max_depth=3).
- Improved accuracy from 75% to ~80%.
- Observed better generalization after limiting model complexity.
- Compared results with Logistic Regression (90%).
- Concluded Logistic Regression remains the best-performing model so far.

## Day 6

- Implemented Random Forest model.
- Compared performance with Logistic Regression and Decision Tree.
- Observed improved stability compared to a single Decision Tree.

## Day 7

- Evaluated model using confusion matrix
- Achieved AUC score of 0.96.
- Observed only 3 false negatives.
- Learned importance of evaluating beyond accuracy.

## Day 8

- Extracted feature importance using Random Forest.
- Top features: thalach, ca, oldpeak.
- Observed that model prioritizes cardiovascular stress indicators and vessel blockage.
- Findings align with known clinical risk factors for heart disease.
- Improved interpretability and trust in model predictions.

## 9. Cross-Validation

- Applied 5-fold cross-validation to Logistic Regression model
- Observed performance variation across folds (78% – 91%)
- Average accuracy: ~84%
- Identified that initial single-split accuracy (~90%) was optimistic
- Concluded that the model is moderately stable
- Improved understanding of model generalization and reliability

## 10. Hyperparameter Tuning

- Performed hyperparameter tuning using GridSearchCV
- Optimized Logistic Regression regularization parameter
- Best parameter: C = 0.1
- Improved model performance and consistency
- Strengthened model reliability through systematic tuning
