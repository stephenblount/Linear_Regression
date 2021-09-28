## Linear Regression analysis of the Car Data

The aim of this project is to determine which features of a car are heavily related to the value of a car.

The initial step of the analysis, after data acquisition and cleaning, was to create a pairplot and correlation heat maps of the numerical variables to determine if collinearity existed. These results show there is heavy collinearity between certain features of cars, with Power being the most linearly correlated with price.


Next, collinear features were removed from analysis to create a more stable model, keeping power due to its strong relationship with the target variable. All categorical features where then converted to dummy variables and a baseline linear regression model was created.


After the baseline was created, a LASSO model was iterated to determine the best lambda value to minimize error and a Lasso model was fit to the training data. From the list of variable coefficient, columns were removed from the analysis if the coefficient went to zero.
![](Images/base_linear_regression.png)

I plan to iterate a few more cycles through LASSO to try to reduce my total number of variables more. Diagnostic plots will be added to look at the spread of residuals and y vs y pred.
I want to try to run Ridge and ElasticNet to see how my results vary. If I have time, trying to implement a kfold schema throughout the code will be undertaken.
