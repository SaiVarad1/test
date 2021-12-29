# 3.6 Turning Categorial Variables into Quantitative Variables in Python


## One-hot Encoding

| Car | Fuel | ... | gas | diesel |
| --- | --- | --- | --- | --- |
A | gas| ...| 1|0| 
|B| diesel|...| 0|1|

## Pandas
pandas.get_dummies()  
###  `pd.get_dummies(df['fuel'])`