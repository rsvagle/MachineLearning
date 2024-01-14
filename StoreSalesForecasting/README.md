# Grocery Store Sales Forecasting - Kaggle Competition

### Summary
In the first pass, I ignored history and used the generic XGBRegressor to make predictions. I tried using the objective of squared mean error, but the model consistently returned terrible results with that. Using a different metric to fit the XGBRegressor, I was still able to get the Root Mean Squared Logarithmic Error to be 1.54655, but on the Kaggle data it was scored 2.018. In this pass, I'll try to use the Holiday table to try and get an improvement on my results.

In the second pass, I successfully added in the holiday information, but didn't change anything else. The second pass was similar on RMSLE for the training data, but the Kaggle test data it scored 1.994, which isn't much better than before.

In the third pass pass, I used different slices of time for training and test data, and also removed the transactions from the model fitting, being that the test data does not have any transaction data in that range. Transaction data was obviously very correlated with the sales, and so I'm sure the previous models were more fitted towards that variable that was missing in the test data. With these changes my submission goes does to a score of 1.366, a significant improvement.

### Lessons Learned
This notebook was an exercise in joining several datasets together to create a coherent and consistent datamodel to feed into a regressor. It took me a while to intuit the transaction data was non-existant in my test data, but was highly correlated to sales, giving me a bad model. I also ended up surfing through XGBoost documentation quite a bit after seeing my regressor objective function wasn't working for fitting in notebook 1.