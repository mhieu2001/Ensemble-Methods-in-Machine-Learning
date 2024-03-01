# Some-learning-code
Bagging, Boosting, RandomForest maybe more in future let's see

## Bagging 
In binary classification problems, predictions from models are often continuous values representing probabilities. A common threshold for converting these probabilities into binary predictions is 0.5. If the predicted probability is greater than or equal to 0.5, it is classified as the positive class; otherwise, it is classified as the negative class.

When we use a decision tree, all the features are used and the split is chosen as the one that increases the information gain the most. While it may seem counter-intuitive, selecting a random subset of features can help in the performance of an ensemble model. In the following example, we will use a random selection of features prior to model building to add additional variance to the individual trees. While an individual tree may perform worse, sometimes the increases in variance can help model performance of the ensemble model as a whole.

## RandomForest 
The random forest algorithm has a slightly different way of randomly choosing features. Rather than choosing a single random set at the onset, each split chooses a different random set.

After splitting the data on the best feature from that subset, we’ll likely want to split again. For this next split, we’ll randomly select three features again to consider. We’ll continue this process until the tree is complete.

One question to consider is how to choose the number of features to randomly select. 

*A good rule of thumb is select as many features as the square root of the total number of features*. 

But if we had a dataset with 25 features, we’d want to randomly select 5 features to consider at every split point.
