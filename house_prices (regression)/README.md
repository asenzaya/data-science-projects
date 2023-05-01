## Predicting House Prices in Ames, Iowa

- Technologies Used: Python, NumPy, Pandas, Matplotlib, Seaborn, Scikit-Learn.
- Algorithms: Linear regression, Random forest, Gradient boosting.
- Main Measure of Performance: RMSE (provided by Kaggle upon submission)
- Link to Code: [House Prices](https://github.com/asenzaya/data-science-projects/blob/main/house_prices%20(linear%20regression)/house_prices.ipynb)
- Data Source: Kaggle

The main focus of this project was to challenge myself with a dataset that has an overwhelming amount of features available. The first step was to dive into the data and analyse what should be included and excluded from the models. 

### Data cleaning

- Features with large amounts of missing values were excluded as they wouldn’t provide valuable insights to our models. 
- Categorical features with too many categories (>30) were excluded as they would risk causing overfitting in the linear regreassion models dur to the poor ability to generalize to new data. 
- Numerical NaN features were replaced by the median of train and categorical features were replaced by the mode.
- All features were scaled and categorical features were transformed into binary features.
- Features with multicolinearity were excluded. The ones with the highest correlations with the dependent variables were kept in the models.


### Model fitting and performance

Four models were proposed, including two benchmark linear regression models, one random forest regressor, and one gradient boosting regressor. 

#### Model 1: Linear regression with numerical features only

The intent for this first model was to test the hypothesis that the model was going to give a good performance simply by excluding categorical variables. Its best RMSE performance ended up being 0.22.

#### Model 2: Linear regression with numerical and categorical features.

With this model, the goal was to use add all categorical features that were not excluded during the cleaning stage. Its best performance ended up being a RMSE of 0.65. The worst performance of all models.

#### Model 3: Random Forest Regressor

Despite manipulating the data in different ways, linear regression models were not able to do better than a 0.22 RMSE. It was time to try different algorithms that were going to be more appropriate. This one is using Random Forest and performed better than linear regression’s best score with a RMSE of 0.16.

#### Model 4: Gradient Boosting Regressor

Last but not least. Gradient boosting is the winning model. Its best RMSE is 0.14.

### Conclusion

Even though linear regression was not the best way to approach this dataset, it was interesting to notice how much better the numerical only performed compared to the one that included categorical features. This is most likely due to the model struggling to handle a large amount of features. Random forests and grandient boosting are more appropriate in those situation and it is with no surprise they performed better.