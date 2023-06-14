# Day 61, 13.06.2023

---
##  __Basic Overview__  

1. [What happened yesterday?](#what_happened_yesterday?) 
1. [Bias Variance Trade Off](#bias_variance_trade_off) 
1. [Root Mean Square Error (RMSE)](#root_mean_square_error_(RMSE)) 
1. [Underfitting vs Overfitting](#underfitting_vs_Overfitting)
1. [Regularization](#5_regularization) 

---

## __1. What happened yesterday?__
* in the first part Lana and Larissa shared her Solution for Notebook 6 from our ds-linear-regression Repo
* second part Larissa had her lecture about Regularization
* third part we worked as groups in Notebook 2 of our ds-predictive-regression Repo

---

## __2. Bias Variance Trade Off__

#### Basics

* $MSE (\hat{y}) = Bias^2 + Variance + Noise$
* is the sweet spot where our machine model performs between the errors introduced by the bias and the variance
* actions that you take to decrease bias leading to a better fit to the training data but will simultaneously increase the variance in the model 
  leading to higher risk of poor predictions and vice versa

#### Bias

* difference between the average prediction of our model and the correct value which we are trying to predict 
* ##### high bias:
* pays very little attention to the training data and oversimplifies the model 
* the model learns the wrong relations by not taking all features into account 
* models can’t perform well on new data
* overly simplifies the model
* high error on both test and train data
* leads to Underfitting
* a low bias model will make fewer assumptions about the form of the target function

![High vs Low Bias](images/bias_high_low.png)


#### Variance

* indicates how much the estimate of the target function will change when different training data is used
* describes how much a random variable differs from its expected value
* measures the inconsistency of different predictions using different training sets 
* can lead to overfitting
* high variance may reflect random noise in the training data set instead of the target function
* will result in significant changes to the projections of the target function
* low variance means sampled data is close to where the model predicted it would be

#### Noise

* is the irreducible error of a model (can’t be influenced)

![High vs Low Bias and Variance](images/high_low_variance_bias.png)

##### Low-Bias + Low-Variance:
* shows an ideal machine learning model (impossible in practice)

##### Low-Bias + High-Variance: 
* model predictions are inconsistent and accurate on average 
* occurs when the model learns with a large number of parameters
* leads to an Overfitting

##### High-Bias + Low-Variance: 
* predictions are consistent but inaccurate on average
* occurs when a model does not learn well with the training dataset or uses to few numbers of the parameter
* leads to Underfitting

##### High-Bias + High-Variance:
* predictions are inconsistent and also inaccurate on average

---
  
## __3. Root Mean Square Error (RMSE)__

* is the standard deviation of the residuals
* standard deviation is a measure of how spread out numbers are
* formula is the square root of the Variance
* Variance is defined as the average of the squared differences from the Mean
* in order to get RMSE we have to use Standard deviation formula but instead of square root of variance we have to calculate the square root of average of squared residuals
* standard deviation is used to measure the spread of data around the mean while RMSE is used to measure the distance between predicted and actual values
* RMSE is a measure of how spread out these residuals are (it tells us how concentrated the data is around the line of best fit)
* since the errors are squared before they are averaged, the RMSE gives a relatively high weight to large errors
* this means the RMSE is most useful when large errors are particularly undesirable
* RMSE should be as low as possible
* what does RMSE indicate?
* it indicates the absolute fit of the model to the data
* provides average model prediction error in units of the variable of interest
* they are negatively-oriented scores which means lower values are better

![RMSE Formula](images/rmse_formula.png)

---

## __4. Underfitting vs. Overfitting__

#### Underfitting
* when high training error and high testing error
* underfit model isn’t complex enough to match the data set
* the model is oversimplified
* the model is unable to generalize and learn from the training data
* therefore has low predictive power on the test dataset as well

#### Overfitting
* when error on training data is low and high on test data
* an overfit model is one that’s too complex for the available data
* the model will often do an extremely good job of matching the available data but be unable to accurately predict what occurs between the data points
* ##### how to prevent:
* gather more data
* reduce its complexity by either reducing the amount or the influence of the features
* can be achieved with Regularization

![Balance Fitting](images/fitting_balance.png)

---

## __5. Regularization__

* is in general any method to prevent overfitting or to help the optimization of a model

#### Ridge Regression (L2 Regularization)

* penalizes the size (square of the magnitude) of the regression coefficients
* a larger regression coefficient is a larger penalty
* enforces the slope to be lower, but not 0
* does not remove irrelevant features, but minimizes their impact
* each feature should have as little effect on the outcome as possible while still predicting well

#### Lasso Regression (L1 Regression)
* Least Absolute Shrinkage and Selection Operator
* regularization term penalizes the absolute value of the coefficients
* lasso restricts also coefficients to be close to zero
* some coefficients become exactly zero (some features are entirely ignored by the model)
* makes models often easier to interpret and can reveal the most important features
* might remove too many features in our model

#### Elastic Net (L1 + L2)
* is the mixing of Lasso and Ridge
* uses both the L2 and the L1 penalty so we don't have to choose between these two models
* when r = 0 it is equivalent to Ridge, if r = 1 it is equivalent to Lasso Regression
* when features are highly correlated preferable to Lasso
* when there are more feature than observations (high dimensional data) 

---

## __Links__

* [StatQuest Youtube Channel](https://www.youtube.com/@statquest “StatQuest Youtube Channel”)

* [More info about Regularization](https://www.youtube.com/@statquest/ “More info about Regularization”)


