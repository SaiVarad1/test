# 6.3 Overfitting, Underfitting, and Model Selection
Picking the best polynomial order for the model
* Too high -> too flexible, predicts poorly on the testing dataset
* Too low-> doesn't explain the model adequately

## Calculating different R^2 for different degrees

`Rsqu_test=[]`  
`order=[1,2,3,4]`  
`for n in order:`  
    `pr=PolynomialFeatures(degree=n)`  
    `x_train_pr=pr.fit_transform(x_train[["horsepower"]])`  // transforms to polynomial  
    `x_test_pr=pr.fit_transform(x_test[["horsepower"]]) ` // transforms to polynomial  
    `lr.fit(x_train_pr,y_train)`  // fit regression model using transformed data  
   ` Rsqu_test.append(lr.score(x_test_pr,y_test))`