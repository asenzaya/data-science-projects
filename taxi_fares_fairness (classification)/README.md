# Predicting taxi fares fairness in New York City

#### Algorithms used in this project: Decision Tree, Random Forest, Bagging, Boosting, Gradient Boosting, LightGBM

The purpose of this project was to practice using different algorithms and evaluating their performance on a classification problem.

Fares below $10 were considered fair, while fares of $10 or higher were considered unfair.

The data was split into train and test sets and cleaned, with missing or outlier values in the train set replaced by the same values in the test set to prevent data leakage. Rows with a target of NaN were excluded because they would not be useful when fitting the models.

AUC ROC was chosen as the best way to measure performance due to the imbalanced nature of the target variable.

In the end, all models performed similarly, but LightGBM was selected for its high AUC and ability to use the most features for its predictions, compared to the decision tree which was mostly influenced by distance.