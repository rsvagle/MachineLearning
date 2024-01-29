# Spaceship Titanic - Kaggle Competition
My take on one of the common introductory Kaggle competitions

## Lessons Learned
This was a good one to reinforce some feature engineering principles. The first notebook has some of the feature engineering ideas I tried originally, but I stripped out a couple for my second pass. It actually didn't help my model much to do additional feature engineering or the grid search on the model parameters. A basic XGBoost out of the box was as good as it was going to get for a smaller dataset with only a few features like this one. My first submission had an accuracy of 0.79494, and the tuned model only increadsed to 0.79985. It looks like 99% of the submissions are capped at about 0.81, so I think that's about as good as can be done.

## Insights
The biggest feature of importance in determining if a passenger would be transported to another dimensions was whether or not they were in CryoSleep. Second most important was the planet they came from.

![Feature Importance](feature_importance.png "Feature Importance")

![Confusion Matrix](confusion_matrix.png "Confusion Matrix")

![Decision Tree](tree.png "Decision Tree")