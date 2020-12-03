# Amazon_Food_Reviews
In this repository, I am practiced and implemented various machine learning algorithms using the real-world dataset amazon food reviews from Kaggle.

![Amazon_Food_Reviews](https://miro.medium.com/max/523/1*bXDiOoCFTSJJdTQ7JbuijQ.png)

## Task 01. Amazon_Food_Reviews_Featurization

### First We want to know What is Amazon Fine Food Review Analysis?
This dataset consists of reviews of fine foods from amazon. The data span a period of more than 10 years, including all ~500,000 reviews up to October 2012. Reviews include product and user information, ratings, and a plaintext review. We also have reviews from all other Amazon categories.

Amazon reviews are often the most publicly visible reviews of consumer products. As a frequent Amazon user, I was interested in examining the structure of a large database of Amazon reviews and visualizing this information so as to be a smarter consumer and reviewer.

Source: https://www.kaggle.com/snap/amazon-fine-food-reviews

### Introduction

The Amazon Fine Food Reviews dataset consists of reviews of fine foods from Amazon.

1. Number of reviews: 568,454
2. Number of users: 256,059
3. Number of products: 74,258
4. Timespan: Oct 1999 — Oct 2012
5. Number of Attributes/Columns in data: 10

### Attribute Information:
1. Id
2. ProductId — unique identifier for the product
3. UserId — unqiue identifier for the user
4. ProfileName
5. Helpfulness Numerator — number of users who found the review helpful
6. HelpfullnessDenominator — number of users who indicated whether they found the review helpful or not
7. Score — rating between 1 and 5
8. Time — timestamp for the review
9. Summary — brief summary of the review
10. Text — text of the review

## Objective
Given a review, determine whether the review is positive (Rating of 4 or 5) or negative (rating of 1 or 2).

[Q] How to determine if a review is positive or negative?

[Ans] We could use the Score/Rating. A rating of 4 or 5 could be cosnidered a positive review. A review of 1 or 2 could be considered negative. A review of 3 is nuetral and ignored. This is an approximate and proxy way of determining the polarity (positivity/negativity) of a review.

To Know the Complete overview of the Amazon Food review dataset and Featurization visit my medium blog  https://medium.com/analytics-vidhya/amazon-fine-food-reviews-featurization-with-natural-language-processing-a386b0317f56

## Task 02. Apply KNN to Amazon_Food_Reviews_Dataset

![knn](https://miro.medium.com/max/700/0*QPWeWP5FWVMlXNgu.png)

##### Apply Knn versions on these feature sets
- Review text, preprocessed one converted into vectors using (BOW)
- Review text, preprocessed one converted into vectors using (TFIDF)
- Review text, preprocessed one converted into vectors using (AVG W2v)
- Review text, preprocessed one converted into vectors using (TFIDF W2v)


KNN is a non-parametric and lazy learning algorithm. Non-parametric means there is no assumption for underlying data distribution. In other words, the model structure determined from the dataset. This will be very helpful in practice where most of the real-world datasets do not follow mathematical theoretical assumptions.

KNN is one of the most simple and traditional non-parametric techniques to classify samples. Given an input vector, KNN calculates the approximate distances between the vectors and then assign the points which are not yet labeled to the class of its K-nearest neighbors.

The lazy algorithm means it does not need any training data points for model generation. All training data used in the testing phase. This makes training faster and the testing phase slower and costlier. The costly testing phase means time and memory. In the worst case, KNN needs more time to scan all data points, and scanning all data points will require more memory for storing training data.

To Know how K-NN works visit my medium blog link here https://medium.com/analytics-vidhya/k-nearest-neighbors-algorithm-7952234c69a4.

To Know detailed information about performance metrics used in Machine Learning please visit my medium blog link here https://medium.com/analytics-vidhya/performance-metrics-for-machine-learning-models-80d7666b432e.

After applying KNN algorithm to amazon food reviews data set we make below conclusions.

### Conclusions

![conclusion](https://miro.medium.com/max/569/1*6o-q6t2nK0AiqvwTVWNrWA.png)

1. From the above table, we can conclude the for all the text features best_K by Hyperparameter tuning is 49.
2. From the above table, we observed that the K-NN simple brute model of Word2vec features having the highest AUC score of 84.61% on test data.
3. The K-NN simple brute model of TF-IDF and Bag of words features also works reasonably well on test data having an AUC score of 81.34% and 80.18%.
4. The Avg_Word2Vec and TFIDF_Word2vec are having a low AUC score on test data.

## Task 03. Apply NaiveBayes to Amazon_Food_reviews_Dataset

![Naive_bayes](https://cdn.educba.com/academy/wp-content/uploads/2019/04/Naive-Bayes-Algorithm.jpg)

### Apply Multinomial NaiveBayes on these feature sets
- Review text, preprocessed one converted into vectors using (BOW)
- Review text, preprocessed one converted into vectors using (TFIDF)

Naive Bayes is a statistical classification technique based on Bayes Theorem. It is one of the simplest supervised learning algorithms. Naive Bayes classifier is a fast, accurate, and reliable algorithm. Naive Bayes classifiers have high accuracy and speed on large datasets.

Naive Bayes is the most straightforward and fast classification algorithm, which is suitable for a large chunk of data. Naive Bayes classifier is successfully used in various applications such as spam filtering, text classification, sentiment analysis, and recommender systems. It uses Bayes theorem of probability for prediction of unknown class.

Naive Bayes makes an assumption that features are conditionally independent. Theoretically, if the assumption does not hold true then the performance of NB degrades. But the research has shown that even if there is some feature dependency the Naive Bayes gives the best result.

To Know detailed information about NaiveBayes algorithm and implementation  please visit my medium blog link here https://medium.com/analytics-vidhya/naive-bayes-algorithm-with-amazon-food-reviews-analysis-66bb59b66e62

After applying Naive Bayes  algorithm to amazon food reviews data set we make below conclusions.

### Conclusions

![conclusion](https://miro.medium.com/max/465/1*g7VGRbn1qsMLtpMxaPzQfQ.png)

1. Compare to Bag of words features representation, TFIDF features are got the highest 95.51% AUC score on Test data.
2. Both are having 0.1 as the best alpha by Hyperparameter tuning.
3. Both models have reasonably worked well for Amazon_food_reviews classification.

## Task 04. Implementation_of_Stochastic_Gradient_Descent

![graient descent](https://d2o2utebsixu4k.cloudfront.net/media/images/aa76a582-a221-4fd8-9ad1-4fdd3ba91397.jpg)

### Apply SGD Regressor from scratch

1. Take the boston data set from sklearn.
2. Write the SGDRegressor from scratch.
3. You don’t need to split the data into train and test, you consider whole data for this implementation.
4. Get weights( coefs_ and intercept ) from your model and the MSE value.
5. Don’t forget to standardize the data, and choose appropriate learning rate.
6. Train your model using SGDRegressor with the same parameters, and find the MSE on the same data.
7. Compare these two results.
8. You can choose any other metric other than MSE to compare them. They both should be same.

The solution to an optimization problem can be done by selecting different methods. Moreover, the user can navigate on the surface or curve to establish an initial point and find the optimal or critical point, which can be observed on the plotted function.

Some functions are very complex to solve, so the computer science technique to solve those types of functions is the Gradient descent algorithm.

Gradient descent is an optimization algorithm that is mainly used to find the minimum of a function. In machine learning, gradient descent is used to update parameters in a model. Parameters can vary according to the algorithms.

To Know detailed information about Gradient_Descent and implementation  please visit my medium blog link here https://medium.com/analytics-vidhya/solving-for-optimization-problems-fee1e7ee5d22

After applying Gradient_Descent  algorithm to boston data set we make below conclusions.

### Conclusions

![conclusion](https://miro.medium.com/max/700/1*fudzwFus59rd0wZgcZdmSA.png)

As from the above, we can see that mean of the differences in the prediction of the two models is at 0 As we can see above intercept and weight(coef) is almost same for sklearn SGD and self-implemented SGD.

## Task 05. Apply Logistic_Regression to Amazon_Food_Reviews_Dataset

![Logistic regression](https://miro.medium.com/max/640/0*Zv8zeMeD-PZVSDYC.jpg)

### Apply Logistic Regression on these feature sets
- Review text, preprocessed one converted into vectors using (BOW)
- Review text, preprocessed one converted into vectors using (TFIDF)
- Review text, preprocessed one converted into vectors using (AVG W2v)
- Review text, preprocessed one converted into vectors using (TFIDF W2v)

Logistic regression is a classification algorithm used to assign observations to a discrete set of classes. There are lots of classification problems that are available, but the logistics regression is common and is a useful regression method for solving the binary classification problem.

There are lots of classification problems that are available, but the logistics regression is common and is a useful regression method for solving the binary classification problem.

Logistic Regression is one of the most simple and commonly used Machine Learning algorithms for two-class classification. It is easy to implement and can be used as the baseline for any binary classification problem.

Its basic fundamental concepts are also constructive in deep learning. Logistic regression describes and estimates the relationship between one dependent binary variable and independent variables.

To Know detailed information about Logistic_Regression and implementation  please visit my medium blog link here https://medium.com/analytics-vidhya/logistic-regression-with-amazon-food-reviews-164b3748335e

After applying Logistic_Regression  algorithm to Amazon_food_reviews data set we make below conclusions.

### Conclusions

![conclusion](https://miro.medium.com/max/700/1*4mGAgDaEp78cuOTw5dxLWA.png)

1. Compare to Bag of words features representation, TFIDF features with L2 Regularization are getting the highest 93.25% AUC score on Test data.
2. The C values are different from model to model.

## Task 06. Apply Support_Vector_Machines to Amazon_Food_Reviews_Dataset

![svm](https://www.learnopencv.com/wp-content/uploads/2018/07/support-vector-machine-cover.jpg)

### Apply SVM on these feature sets
- Review text, preprocessed one converted into vectors using (BOW)
- Review text, preprocessed one converted into vectors using (TFIDF)
- Review text, preprocessed one converted into vectors using (AVG W2v)
- Review text, preprocessed one converted into vectors using (TFIDF W2v)

SVM is a supervised Machine Learning algorithm that is used in many classifications and regression problems. It still presents as one of the most used robust prediction methods that can be applied to many use cases involving classifications.

Logistic Regression doesn’t care whether the instances are close to the decision boundary. Therefore, the decision boundary it picks may not be optimal. If a point is far from the decision boundary, we may be more confident in our predictions.Therefore, the optimal decision boundary should be able to maximize the distance between the decision boundary and all instances. i.e., maximize the margins. That’s why the SVMs algorithm is important!Find a Hyperplane that separates Positive points from Negative points as wide as possible.

The support vector machine works by finding an optimal separation line called a ‘hyperplane’ to accurately separate 2 or more different classes in a classification problem. The goal is to find the optimal hyperplane separation through training the linearly separable data with the SVM algorithm.

To Know detailed information about Support Vector Machines and implementation  please visit my medium blog link here https://medium.com/analytics-vidhya/support-vector-machines-with-amazon-food-reviews-9fe0428e09ef

After applying Support Vector Machines  algorithm to Amazon_food_reviews data set we make below conclusions.

### Conclusions

![conclusion](https://miro.medium.com/max/700/1*XKxT7IiMbpnXrkj0N-dFIQ.png)

1. Compare to Bag of words features representation, TFIDF features with L2 Regularization are getting the highest 93.29% AUC score on Test data.
2. The C and Gamma values are different from model to model.

## Task 07. Apply Decision_Tree to Amazon_Food_Reviews_Dataset

![Decision_Tree](https://arbordayblog.org/wp-content/uploads/2017/09/japanese-maple-shade-tree-iStock-180454493-1080x608.jpg)

### Apply Decision Trees on these feature sets
- Review text, preprocessed one converted into vectors using (BOW)
- Review text, preprocessed one converted into vectors using (TFIDF)
- Review text, preprocessed one converted into vectors using (AVG W2v)
- Review text, preprocessed one converted into vectors using (TFIDF W2v)

Decision trees are a popular supervised learning method for a variety of reasons. The benefits of decision trees include that they can be used for both regression and classification, they are easy to interpret and they don’t require feature scaling. They have several flaws including being prone to overfitting.

Decision trees which are also modernly known as classification and regression trees (CART) were introduced by Leo Breiman to refer, Decision Tree algorithms. They have a supervised learning algorithm that has a pre-defined target variable & they are mostly used in non-linear decision making with a simple linear decision surface. In other words, they are adaptable for solving any kind of problem at hand (classification or regression).

One of the best and most used supervised learning methods are tree-based algorithms. They empower predictive modeling with higher accuracy, better stability, and provide ease of interpretation. Unlike linear modeling techniques, they map non-linear relationships quite well. Methods like decision trees, random forest, gradient boosting are being popularly used in all kinds of data science problems. Hence, for every analyst, it’s important to learn these algorithms and apply them at the time of modeling.

To Know detailed information about Decision Tree and implementation  please visit my medium blog link here https://medium.com/analytics-vidhya/decision-tree-with-amazon-food-reviews-5639a7b70cef

After applying Decision Tree  algorithm to Amazon_food_reviews data set we make below conclusions.

### Conclusions

![conclusion](https://miro.medium.com/max/514/1*3-g4jeREUkiPE8GvVffV0Q.png)

1. Compare to all other features representation, Bag of words features with Depth of 50 and min_split of 500 are getting the highest 80.65% AUC scores on Test data.
2. The optimal Depth and Min_split values from Grid_search_CV are different from model to model.

## Task 08. Apply Random_Forest to Amazon_Food_Reviews_Dataset
![ensemble](https://miro.medium.com/max/700/0*qKfYwZGpJtQsjXKS.jpeg)

### Apply Random Forests & GBDT on these feature sets
- Review text, preprocessed one converted into vectors using (BOW)
- Review text, preprocessed one converted into vectors using (TFIDF)
- Review text, preprocessed one converted into vectors using (AVG W2v)
- Review text, preprocessed one converted into vectors using (TFIDF W2v)

Commonly, the individual model suffers from bias or variances and that’s why we need ensemble learning.

An Ensemble method is a technique that combines the predictions from multiple machine learning algorithms together to make more accurate predictions than any individual model. A model comprised of many models is called an Ensemble model.

Random forest is a Supervised Learning algorithm that uses an ensemble learning method for classification and regression.

Random forest is a bagging technique. The trees in random forests are run in parallel. There is no interaction between these trees while building the trees.

It operates by constructing a multitude of decision trees at training time and outputting the class that is the mode of the classes (classification) or mean prediction (regression) of the individual trees.

A random forest is a meta-estimator (i.e. it combines the result of multiple predictions) which aggregates many decision trees, with some helpful modifications.

To Know detailed information about Ensemble models and implementation  please visit my medium blog link here https://medium.com/analytics-vidhya/random-forest-and-ensembles-learning-with-amazon-food-reviews-e58c72c189be

After applying Random Forest  algorithm to Amazon_food_reviews data set we make below conclusions.

### Conclusions

![conclusion](https://miro.medium.com/max/679/1*J1iY59_aVC75CFl7tekbZg.png)

1. From the above table, we conclude that TFIDF in Random Forest with an optimal depth of 60 and optimal estimator of 500 have the Highest AUC score i.e 93.40 %.
2. xgboost also TFIDF with an optimal depth of 10 and optimal estimator of 500 have the Highest AUC score i.e 93.96 %.
3. Both Random Forest and xgboost models have performed reasonably well on Test data.

