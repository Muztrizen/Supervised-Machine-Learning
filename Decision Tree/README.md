## Basic Rules to Growing a Tree
* Features to choose.
* Condition for splitting.
* Knowing when to stop.
* Pruning.

## Common Decision Tree Algorithm
* Gini index
* Chi Square
* Information Gain
* Reduction in Variance

## Advantage of Decision Tree
* **Speed**: Very fast and efficient compared to KNN and other classification algorithms.
* **Simplicity & Interpretability**: Simple to understand. Easy to interpret. Trees can be visualised.
* **Data Preparation**: Require little data preparation. Don’t require feature scaling.
* **Training effort**: Require relatively less effort for training the algorithm.
* **Flexibility**: Able to handle both numerical and categorical data. Decision trees can be used to predict both continuous and discrete values i.e. they work well for both regression and classification tasks.
* **Evaluation**: Possible to validate a model using statistical tests.
* **+Alpha**: can be used to classify non-linearly separable data.

## Disadvantage of Decision Tree
* **Overfitting**: Leading to poor accuracy on unseen data. Mechanisms such as pruning (not currently supported), setting the minimum number of samples required at a leaf node or setting the maximum depth of the tree are necessary to avoid this problem.
* **Unstability**: Can be unstable even due to small variation in data (variance). Mitigant: Use decision trees within an ensemble such as bagging and boosting method.
* **Non-optimal**: Cannot guarantee to return the globally optimal decision tree. Mitigant: Training multiple trees in an ensemble learner.
* **Bias of class**: Decision tree learners create biased trees if some classes dominate. Recommendation: Balance the dataset prior to fitting.

## Reference:
1. https://www.youtube.com/watch?v=DCZ3tsQIoGU
