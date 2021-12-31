# 6.4 Grid Search

## Hyperparameters
* Not part of fitting or training process
* Eg alpha
* Scikit-learn automatically iterates over hyperparam using cross validation called Grid search

## Grid Search
* To select hyperparam
* Split dataset into **Training, Validation, Test** datasets
* Train for different hyperparams, using MSE or R^2
* Select best hyperparam (Minimizes MSE or Maximizes R^2)
* Test model performance using test dataset

### `parameters=[{'alpha':[1,10,100,1000]}]`


* Grid Search takes scoring method (in this case R^2), the number of folds, model or object (Ridge()), free param values

Eg:

`from sklearn.linear_model import Ridge`  
`from sklearn.model_selection import GridSearchCV`  
`parameters1=[{'alpha':[1,10,100,1000,10000,100000,1000000]}] ` 
`RR=Ridge()  `
`Grid1=GridSearchCV(RR,parameters1,cv=4)` // R^2 method is default
`Grid1.fit(x_data[['horsepower','curbweight','engine-size','highway-mpg]], y_data)  `
`Grid1.best_estimator_ ` // best value of free param  
`scores=Grid1.cv_results_`
`scores['mean_test_score']`  

## Ridge Regression has option to normalize data
`parameters=[{'alpha':[1,10,100,1000], 'normalize:[True,False]}]`  
Use Ridge Regression again on this, same as above  

`parameters2=[{'alpha':[1,10,100,1000,10000,100000,1000000], 'normalize':[True,False]}] `   
`RR=Ridge()  `  
`Grid1=GridSearchCV(RR,parameters2,cv=4)`  
`Grid1.best_estimator_ `   
`scores=Grid1.cv_results_`  // dictionary