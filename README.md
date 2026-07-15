# Heart Disease Prediction

An educational machine-learning project exploring binary heart-disease classification with clinical variables. The project follows the workflow from data preparation and exploratory analysis through model comparison, validation, threshold tuning, and interpretation.

> **Important:** This model is a learning project, not a clinical diagnostic tool.

## Project question

How effectively can common classification models distinguish between records with and without heart disease, and how does changing the classification threshold affect the balance between missed cases and false alarms?

## Workflow

1. Cleaned the dataset and converted the target into a binary outcome.
2. Explored distributions, outliers, correlations, and class relationships.
3. Trained Logistic Regression, Decision Tree, and Random Forest models.
4. Compared accuracy, precision, recall, F1 score, and ROC-AUC.
5. Used five-fold cross-validation to estimate performance stability.
6. Tuned the Logistic Regression regularisation parameter with GridSearchCV.
7. Adjusted the decision threshold to prioritise recall.
8. Interpreted Logistic Regression coefficients and model feature importance.

## Reported results

| Evaluation | Reported result |
|---|---:|
| Best single-split accuracy | 0.90 |
| Five-fold mean accuracy | approximately 0.83 |
| ROC-AUC | 0.96 |
| Logistic Regression recall | 0.88 |
| Recall after lowering threshold to 0.30 | 0.92 |
| Precision after lowering threshold to 0.30 | 0.76 |

The cross-validation result is more realistic than the strongest single train-test split. Lowering the threshold reduced false negatives, but increased false positives. That trade-off is central to interpreting classification performance in a health-related setting.

## Model comparison

Logistic Regression was selected as the final model because it produced the strongest reported accuracy and recall while remaining easier to interpret than the tree-based alternatives. Decision Tree performance improved after depth restriction, illustrating how controlling complexity can reduce overfitting.

## Interpretation

The analysis identified variables including number of major vessels, exercise-induced angina, ST depression, and maximum heart rate as influential. These associations describe the behaviour of this dataset and model; they do not establish medical causation.

## Tools

- Python
- Pandas and NumPy
- Matplotlib and Seaborn
- Scikit-learn

## Limitations

- The dataset is relatively small.
- Performance varies across folds.
- Results have not been externally validated.
- Threshold selection reflects an illustrative priority rather than a clinical decision rule.
- The project should not be used for diagnosis or treatment decisions.

## Next improvements

- Add a precise dataset citation and data dictionary.
- Consolidate the analysis into one reproducible notebook or pipeline.
- Add a dependency file and fixed random seeds.
- Evaluate calibration and confidence intervals.
- Test the final workflow on an untouched external dataset.

## Author

Daniel Enemona Mamodu  
[GitHub](https://github.com/Danniejnr) · [LinkedIn](https://www.linkedin.com/in/danniejnr)
