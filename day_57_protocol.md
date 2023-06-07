# Day 57, 06.06.2023

---
##  __Basic Overview__  

1. <span style="color:grey"> [What happened yesterday?](#What happened yesterday?) 
1. <span style="color:grey"> [Recap Simple Linear Regression](#Recap Simple Linear Regression) 
1. <span style="color:grey"> [Scikit](#3Scikit) 

---

## __1. What happened yesterday?__
* in the first part Niko has held his presentation about Linear Regression
* second part we worked in groups with scikit in the notebooks 1 - 3
* today we will go on with the notebook 3 and further with multiple linear regression
* todays protocoll duty is on Jaad

---

## __2. Recap Simple Linear Regression__

#### Basics

* useful for finding relationship between two continuous variables
* one is predictor or independent variable and other is response or dependent variable
* looks for statistical relationship but not for causality
* core idea is to obtain a line that best fits the data

#### Definitions and Explanations

##### Equation of Simple Linear Regression: 
  
$y_i = b_0 + b_1 x_i + e_i$
* $b_0$ is the intercept (wheres y when x = 0)
* $b_1$ is coefficient or slope
* x is the independent variable
* y is the dependent variable
* $e_i$ is the residual or error = $y_i$ - $\hat{y}$ (actual values – predicted values)

![Regression Plot](images/regression_plot_1.png)

##### Residual / Error

* vertical distance between the data point and the regression line
* each data point has one residual
* operations with residuals / errors always squared
* if we don’t square them, then positive and negative points will cancel out each other

##### Ordinary Least Square Method (OLS)

* there can be an infinite amount of lines possible, concept is to draw a line through which represent the plotted data points the best

##### Assumptions of OLS

* Homogeneity of variance (homoscedasticity): the size of the error in our prediction doesn’t change significantly across the values of the independent variable.
* Independence of observations: the observations in the dataset were collected using statistically valid sampling methods, and there are no hidden relationships among observations
* Normality: the data follows a normal distribution
* the relationship between the independent and dependent variable is linear: the line of best fit through the data points is a straight line (rather than a curve or some sort of grouping factor)

##### Sum of Squares
* Sum of Squares Total (SST): the sum of squared differences between individual data points ($y_i$) and the mean of the response variable ($\bar{y}$)
* Sum of Squares Regression (SSR): the sum of squared differences between predicted data points (ŷ) and the mean of the response variable ($\hat{y}$)
* Sum of Squares Error (SSE): the sum of squared differences between predicted data points ($\hat{y}$) and observed data points ($y_i$)

![SSE_SSR_SST](images/sse_ssr_sst.png)


##### Coefficient of determination R²
* is a measure of how much of the variation in the dependent variable is explained by the independent variables in the model
* it ranges from 0 to 1, higher values indicating a better fit
* R² = SSE / SST = 1 - ( SSR / SST )

---
  
## __3. scikit__

![Cheat Sheet scikit](images/scikit_cheat_sheet.jpg)
  
* [Scikit Crash Course](https://www.youtube.com/watch?v=0B5eIE_1vpU "Scikit Crash Course")

---
