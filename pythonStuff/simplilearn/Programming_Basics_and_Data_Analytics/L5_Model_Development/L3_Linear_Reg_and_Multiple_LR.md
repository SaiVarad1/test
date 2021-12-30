# 5.3 Linear and Multiple Linear Regression


## Linear Regression
* One independent Variable  
    ## `y=b0+b1x`

    ## Python Implementation
    1. Import linear_model from scikit-learn  
        `from scikit-learn.linear_model import LinearRegression`
    2. Create a Linear Regression Object using Constructor  
        `lm=LinearRegression()`  
    3. Define Predictor and Target Variables  
       ` X=df[["highway-mpg"]]`  
        `Y=df[["price"]] ` 
    4. Use `lm.fit(X,Y)` to fit the model (calculate b0 and b1)  
    5. Prediction is obtained from   `Yhat=lm.predict(X) ` 
        `b0=lm.intercept_ ` 
       ` b1=lm.coef_ ` 
## Multiple Linear Regression
* Two or more independent Variable for one dependent variable  
Y=b0+b1X1+b2X2  
* Graph is 3D when plotting 2 variables (X1, X2), height is proportional to Yhat.  
    ## Python Implementation
    1. Extract Predictor Variables and store them in variable Z  
        `Z=df[["horsepower","curb-weight","engine-size","highway-mpg"]]`  
    2. Train model  
        `lm.fit(Z,df[['price']])`  
    3. `Yhat=lm.predict(X)`  