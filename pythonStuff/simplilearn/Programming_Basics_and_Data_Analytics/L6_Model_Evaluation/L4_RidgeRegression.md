# 6.6 Ridge Regression

* Prevents Overfitting

* Controls Magnitude of Polynomial Coeffs
    * If alpha too large ->  coeffs small, underfits
    * If alpha too small -> coefs bigger, overfits
* alpha is selected before fitting or training model

* use cross validation to select alpha

`from sklearn.linear_model import Ridge`
`RidgeModel=Ridge(alpha=0.1) ` 
`RidgeModel.fit(X,y)`  
`Yhat=RigeModel.predict(X) `


* Use validation data (AKA test data for params like alpha) for cross validation  
    TRAIN -> PREDICT -> R^2   
    put into array and take average