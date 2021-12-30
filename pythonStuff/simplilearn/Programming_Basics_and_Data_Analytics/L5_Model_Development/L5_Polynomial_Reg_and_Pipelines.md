# 5.5 Polynomial Regression and Pipelines

1. Calculate Polynomial of the 3rd Order  
    `f=np.plyfit(x,y,3) `  
    `p=np.polydl(f)`


## Pre-Processing
### Polynomial Regression with More than One Dimension
Use preprocessing library  
    `from sklearn.preprocessing import PolynomialFeatures`    
    `pr=PolynomialFeatures(degree=2)  `
    `pr.fit_transform([1,2],include_bias=False)`
### Normalizing each feature simultaneously
`from sklearn.preprocessing import StandardScaler`    
`SCALE=StandardScaler()  `  
`SCALE.fit(x_data[["horsepower","highway-mpg]])  `  
`x_scale=SCALE.transform(x_data[["horsepower','highway-mpg']])`


### Pipelines
* Simplify Code {Transformations -> Prediction}
    * Eg:  NORMALIZATION -> POLYNOMIAL TRANSFORMATION -> LINEAR REGRESSION 

`from sklearn.preprocessing import PolynomialFeatures`  
`from sklearn.preprocessing import LinearRegression`  
`from sklearn.preprocessing import StandardScaler`
`from sklearn.preprocessing import Pipeline`

Create list of tuples
* first elem in tuple is estimator model
* second elem is model constructor

`Input=[('scale', StandardScaler()), ('polynomial', PolynomialFeatures(degree=2)), ('mode',LinearRegression())]`

`pipe=Pipeline(Input)`

### Training pipeline

`Pipe.train(X['horsepower','curb-weight','engine-size','highway-mpg'],y)`  
`yhat=Pipe.predict(X['horsepower','curb-weight','engine-size','highway-mpg'])`

X -> Normalization -> Polynomial Transform -> Linear Regression -> yhat
