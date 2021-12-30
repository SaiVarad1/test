# 5.7 Prediction and Decision Making

## Making Sure Model Checks Out
* Do the predicted values make sense?
    * Train the model:  
    lm.fit(df['highway-mpg'], df['prices])
    * Test the prediction, do values make sense?
        * Checking value for the price of a car with 30 highway-mpg
        lm.predict(30) // Gives 13,771.30
        lm.coef_  // -821.733
* Visualization
    * plot scatter plot with line of best fit for continuous
    * plot histograms for discrete values
    * Residual Plot- Check shape of residuals
    * Distribution Plot
* Numerical measures for evaluation
    * MSE
    * R^2
* Comparing Models
    * Comparing MLR and SLR
    1. A lower MSE doesn't necessarily mean a better fit
        * MSE  for a MLR model will be smaller than a MSE for an SLR model, since the errors of the data will decrease when more variables are included in the model.
        * Polynomial Regression will also have a smaller MSE than regular regression