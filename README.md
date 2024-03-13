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

Nice work! Here are some of the major takeaways about random forests:

- A random forest is an ensemble machine learning model. It makes a classification by aggregating the classifications of many decision trees.
- Random forests are used to avoid overfitting. By aggregating the classification of multiple trees, having overfitted trees in a random forest is less impactful.
- Every decision tree in a random forest is created by using a different subset of data points from the training set. Those data points are chosen at random with replacement, which means a single data point can be chosen more than once. This process is known as bagging.
- When creating a tree in a random forest, a randomly selected subset of features are considered as candidates for the best splitting feature. If your dataset has n features, it is common practice to randomly select the square root of n features.

## AdaBoost (Adaptive Boosting)
