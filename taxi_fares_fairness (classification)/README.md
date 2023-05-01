## NYC Taxi Fares Fairness

The purpose of this project was to practice using different algorithms and evaluating their performance on a classification problem.

- Technologies Used: Python, NumPy, Pandas, Matplotlib, Scikit-Learn
- Algorithms: Decision Tree, Random Forest, Bagging, Boosting, Gradient Boosting, LightGBM
- Main Measure of Performance: AUC Roc
- Link to Code: [Project Taxi Fares Fairness](https://github.com/asenzaya/data-science-projects/blob/main/taxi_fares_fairness%20(classification)/Project_taxi_fares_fairness.ipynb)
- Data Source: Kaggle

Fares below $10 were considered fair, while fares of $10 or higher were considered unfair.

### Data Cleaning

- The data was split into train and test sets and cleaned, with missing or outlier values in the train set replaced by the same values in the test set to prevent data leakage. 
- Rows with a target of NaN were excluded because they would not be useful when fitting the models.
- Latitude and Longitude were shortened to 2 decimals to enable the model to generalize properly.
- Features were created by extracting information such as the day of week and time of day from ‘pickup_datetime’.

### Performance

Accuracy was not chosen due to the imbalanced nature of the target variable. AUC ROC was chosen as it takes into account this characteristic of our data.


### Conclusion

In the end, all models performed similarly, but LightGBM was selected for its high AUC and ability to use the most features for its predictions, compared to the decision tree which was mostly influenced by distance.