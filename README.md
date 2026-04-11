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

## 11. Precision, Recall & F1 Score

- Evaluated model performance using classification report
- Precision (class 1): 0.88
- Recall (class 1): 0.88
- F1-score (class 1): 0.88
- Model correctly identifies 88% of heart disease cases
- Demonstrates a balanced trade-off between precision and recall
- Prioritized recall to reduce false negatives in medical predictions

## 12. Threshold Tuning

- Adjusted classification threshold from 0.5 to 0.3
- Increased recall for heart disease class from 0.88 to 0.92
- Model now correctly identifies 92% of positive cases
- Observed trade-off: precision decreased from 0.88 to 0.76
- Reduced risk of false negatives at the cost of more false positives
- Demonstrated control over model decision-making based on real-world priorities

## 13. Cross-Validation

- Applied 5-fold cross-validation to evaluate model reliability
- Cross-validation scores: 0.88, 0.91, 0.79, 0.81, 0.77
- Average accuracy: 0.83
- Observed variation across different data splits
- Model shows moderate stability and generalization ability
- Provided a more realistic performance estimate than a single test split

## 14. Model Comparison & Selection

- Compared Logistic Regression, Decision Tree, and Random Forest models
- Logistic Regression achieved the highest accuracy (0.90)
- Recall for class 1:
  - Logistic Regression: 0.88
  - Decision Tree: 0.83
  - Random Forest: 0.83
- Logistic Regression outperformed other models in both accuracy and recall
- Selected Logistic Regression as the final model

## 15. Model Interpretation

- Analyzed Logistic Regression coefficients to understand feature importance
- Top positive predictors:
  - ca (number of vessels) – strongest influence
  - exang (exercise-induced angina)
  - oldpeak (ST depression)
- Negative predictor:
  - thalach (maximum heart rate)
- Positive coefficients increase likelihood of heart disease
- Negative coefficients reduce likelihood
- Provided interpretability for model decisions in a healthcare context
- Choice was based on performance and importance of recall in healthcare
- Logistic Regression allows threshold tuning to balance recall and precision based on real-world needs

## 16. ROC Curve & AUC

- Plotted ROC curve to evaluate model performance across all thresholds
- Achieved AUC score of 0.96
- Curve shows strong separation between classes
- Demonstrates model’s ability to distinguish between patients with and without heart disease
- ROC analysis complements accuracy, recall, and precision metrics
