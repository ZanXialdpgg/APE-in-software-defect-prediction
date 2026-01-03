#Software defect prediction using ensemble learning on selected features

This is my own implement of the paper https://www.sciencedirect.com/science/article/abs/pii/S0950584914001591?via%3Dihub

The paper proposes a new approach to improve defect classification by tackling challenges such as data imbalance, feature redundancy, and irrelevance. The authors introduce the Average Probability Ensemble (APE) model, which combines seven classifiers—random forests, gradient boosting, stochastic gradient descent, weighted SVMs, logistic regression, multinomial naive Bayes, and Bernoulli naive Bayes—and show that integrating it with Greedy Forward Selection (GFS) for feature selection significantly enhances prediction accuracy. I only working with NASA dataset due to limited resource but it is the one that give out the best result base on the paper.

The training process will go like this : The older dataset will be the train set and the younger one right after the train set is the validate set. The validate set will then be the train set for which the younger one after it will be the validate set. We do this for all dataset and the result of one model will be the average of all training. The result of each model is then average to get the final result of our APE model.
