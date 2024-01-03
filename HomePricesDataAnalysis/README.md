# Housing Prices - Kaggle Competition
My take on one of the common introductory Kaggle competitions

## Insights
Given the vast set of categorical features and values, a decision tree model is going to be better than trying any linear regression.

For the decision tree, the most important features in housing price are, in order:
1. OverallQual: Rates the overall material and finish of the house
2. GrLivArea: Above Ground Living Area Square Footage
3. TotalBsmtSF: Basement Square Footage
4. GarageArea: Garage Square Footage
5. 1stFlrSF: 1st Floor Square Footage
6. GarageCars: Number of cars the garage can fit
7. YearBuilt: Year the home was built

## Lessons Learned
I struggled mightily to address the issue of categorical data in the test set having different values than the training set. Most of the time spent on this was cleaning the data and getting the feature set right. I did all of this to try and satisfy the requirements of a linear regression. After getting everything set to be able to use the linear regression, it turned out that the linear regression was way overfit on my training data and was useless on the testing data. I suspect this has to do with a number of null values and a very sparse set of categorical values. I think it might work out okay to drastically reduce the number of features when applying a linear regression.

Luckily, once I had things settled with the train/test categories, the random forest model worked very well. It wasn't quite as tight as I might like, but I did some tunining and it was the best we had. An XGBoost model might have yielded better results.