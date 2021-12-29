# 3.5 Dealing With Missing Values

* ## Check with Data Collection Source
* Drop the Missing Values
    * drop the variable
    * drop the data entry
* ## Replace the Missing Values
    * replace with an average
    * replace with frequency
    * replace based on other functions

* Leave it as missing data


## How to drop missing values in Python

* `df.dropna()`
    * `axis=0` - drops entire row
    * `axis=1` drops entire column

`df.dropna(subset=["price"],axis=0.inplace=True)`  
* inplace - param modifies the df directly

## Replacing missing values
df.replace(missing val, new val)  
    `mean= df["normalized-losses"].mean()
    df["normalized_losses"].replace(np.nan, mean)`  
    follow with  
     `df.reset_index(drop=True, inplace=True)`