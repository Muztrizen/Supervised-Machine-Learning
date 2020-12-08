# Advantages of Random Forest
* **Accuracy & robustness**: It is considered as a very accurate and robust method because of the number of decision trees taking part in the process.
* **Flexibility** It can be used for both, classification and regression problem.
* **No Overfitting** The problem of overfitting doesn’t occur in this algorithm because it takes under consideration the average of predictions that are cancelling out the biases.
* **Missing Value Handling** It can also handle the missing values. And it can be done by two ways, first one is to replace the continuous variables with median values and the other one is to calculate the proximity weighted average of missing values.
* **Feature Importance** We can get the information about relative important feature that is contributing in a much better way for the calculation of accuracy.

# [Tuning Parameter](https://scikit-learn.org/stable/modules/generated/sklearn.ensemble.RandomForestClassifier.html)

__Tuning Parameter to Improve Predictive Power__
* `max_depth`:
* `n_estimators`: This is the number of trees you want to build before taking the maximum voting or averages of predictions. Higher number of trees give you better performance but makes your code slower. You should choose as high value as your processor can handle because this makes your predictions stronger and more stable.
* `max_features`: Increasing max_features generally improves the performance of the model as at each node now we have a higher number of options to be considered. However, this is not necessarily true as this decreases the diversity of individual tree which is the USP of random forest. But, for sure, you decrease the speed of algorithm by increasing the max_features. Hence, you need to strike the right balance and choose the optimal max_features.
These are the maximum number of features Random Forest is allowed to try in individual tree. There are multiple options available in Python to assign maximum features. Here are a few of them :
  * Auto/None : This will simply take all the features which make sense in every tree.Here we simply do not put any restrictions on the individual tree.
  * sqrt : This option will take square root of the total number of features in individual run. For instance, if the total number of variables are 100, we can only take 10 of them in individual tree.”log2″ is another similar type of option for max_features.
  * 0.2 : This option allows the random forest to take 20% of variables in individual run. We can assign and value in a format “0.x” where we want x% of features to be considered.
* `min_sample_leaf`: Leaf is the end node of a decision tree. A smaller leaf makes the model more prone to capturing noise in train data. Generally I prefer a minimum leaf size of more than 50. However, you should try multiple leaf sizes to find the most optimum for your use case.

__Tuning Parameter to Improve Model Training Speed__
* `n_jobs`: This parameter tells the engine how many processors is it allowed to use. A value of “-1” means there is no restriction whereas a value of “1” means it can only use one processor.
* `random_state`: This parameter makes a solution easy to replicate. A definite value of random_state will always produce same results if given with same parameters and training data. I have personally found an ensemble with multiple models of different random states and all optimum parameters sometime performs better than individual random state.
* `oob_score`: This is a random forest cross validation method. It is very similar to leave one out validation technique, however, this is so much faster. This method simply tags every observation used in different tress. And then it finds out a maximum vote score for every observation based on only trees which did not use this particular observation to train itself.

## Reference:
* https://scikit-learn.org/stable/modules/ensemble.html#forest
* https://www.youtube.com/watch?v=D_2LkhMJcfY
* https://towardsdatascience.com/hyperparameter-tuning-the-random-forest-in-python-using-scikit-learn-28d2aa77dd74
* https://www.analyticsvidhya.com/blog/2015/06/tuning-random-forest-model/#:~:text=n_estimators%20%3A,but%20makes%20your%20code%20slower
* https://www.analyticsvidhya.com/blog/2020/03/beginners-guide-random-forest-hyperparameter-tuning/
