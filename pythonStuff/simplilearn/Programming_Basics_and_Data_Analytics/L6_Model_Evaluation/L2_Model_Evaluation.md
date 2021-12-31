# 6.2 Model Evaluatiion

* In-sample evaluation -> how well model fits training data, not how well it predicts new data

* Use Out-of-Sample Evaluation

## train_test_split()
`from sklearn.model_selection import train_test_split`

`x_train,x_test,y_train,y_test=train_test_split(x_data,y_data,test_size=0.3,random_state=0)`

## Generalization Performance
* Generalization Error- Measure of how well data does at predicting previously unseen data
    * Error obtained from testing data is an approx of this error
* Precision vs Accuracy
    * Precision
        * How close results are to each other
        * Greater when Less data points used
    * Accuracy
        * How close results are to true value
        * Greater when more data points are used
## Cross Validation
* One of the most common out-of-sample evaluation metrics
* split data into folds - some are used for training, rest are test sets
* every partition is used for training and testing
* average is used for out-of-sample error

## cross_val_score()
* Performs multiple out-of-sample evaluations

`from sklearn.model_selection import cross_val_score`  

`scores= cross_val_score(lr,x_data,y_data,cv=3)` // the model, predictor variable, target variable, number of folds
* Function returns array of scores
* np.mean(scores)

## cross_val_predict()
* Returns prediction obtained for each element when it was in the test set  
`from sklearn.model_selection import cross_val_predict`  
`yhat=cross_val_predict(lr2e,x_data,y_data,cv=3)`
* returns an array of outputs of model