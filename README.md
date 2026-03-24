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
