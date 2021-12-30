# 5.6 Measures for In-Sample Evaluation
* A way to numerically determine how good the model fits on dataset
    * Mean Squared Error MSE
        * **(Residuals-Mean)^2/#observations**  
        `from sklearn.metrics import mean_squared_error ` 
        `mean_squared_error(df['price'],Y_predict_simple_fit)`
    * R squared (R^2)
        * Coeff of Determination
        * Is a measure to determine how close the data is to the fitted regression line
        * R^2: the percentage of variation of the target variable(Y) that is explained by the linear model
        * MSE comparison with Mean line  
            **R^2=(1-(MSE of regression line)/MSE of average of the data))**  
           ` X=df["highway-mpg"]`  
            `Y=df["price"]`  
            `lm.fit(X,Y) `   
            `lm.score(X,y) // returns R squared value`
        
