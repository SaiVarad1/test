# 3.4 Data Normalization with Python

* Features can have different ranges
    * Eg: Age, and Income - Income values are much larger, hence would affect the model more

## Methods to Normalize Data
1.  **Simple Feature Scaling**  
    `x_new= x_old/x_max`
    * Range 0-1
2. **Min-Max**  
    `x_new=(x_old-x_min)/(x_max-x_min)`
    * Range 0-1

3. **Z-Score**  
    `x_new=(x_old - mean)/std`
    * Range typically from -3 to 3