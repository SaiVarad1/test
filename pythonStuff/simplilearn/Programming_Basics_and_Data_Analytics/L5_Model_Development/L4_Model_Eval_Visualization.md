# 5.4 Model Evaluation Using Visualization

## Regression Plot
* Scatterplot (Y)
* Fitted Regression line (Yhat)  
`sns.regplot(x='highway-mpg',y='price',data=df)`   
`plt.ylim(0,)`

## Residual Plot
* Plots residuals of model
* Spread of residuals
    * mean of residuals should be zero
    * spread of residuals should be random around x-axis , no curvature
`sns.residplot(df['highway-mpg'],df['price'])`

## Distribution Plots
* Plots actual vs fitted values
* Discrete - Histogram
* Continuous- Distribution Plot  

`ax1=sns.distplot(df['price'],hist=False,color="r", label="Actual Value")  `
`sns.distplot(Yhat,hist=False,color='b',label="Fitted Values",ax=ax1)`