# 4.3 Correlation - Statistics

Measures the strength of the correlation between two features
* Correlation Coeff
* P-value

## Correlation Coefficient
* Close to 1 - Large Positive relationship
* Close to -1 -Large Negative Relationship
* Close to 0 - No relationship


## P-value
< 0.001 - Strong certainty  
< 0.05 - Moderate certainty  
< 0.1 Weak Certainty  
\> 0.1 No Certainty


**Strong Correlation when Coeff is close to -1 or 1 & P value is less than 0.001**


## Python Implementation 
scipy stats package

`Pearson_coeff, p_value=stats.pearsonr[["horsepower"], df["price"]]`

* can create heatmap of Pearson correlation coeffs
