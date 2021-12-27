# 7.1-3 Pandas 

## Data Structures of Pandas

## 1. Series  
### `pd.series(data,index=[index])`
* 1D labelled array
    * "Labelled"- has indices
* supports multiple data types
* Can be created with different inputs
    * ndarray
    * dict
    * scalar
    * list
### Accessing Elements in Series
* use index position
    * `dict_country_gdp[0]`
* slicing
    * `dict_country_gdp[0:5]`
* by name or index
    * `dict_country_gdp.loc["United States"]`
* by position
    * `dict_country_gdp.iloc[0]`
### Vectorized Operations
* Addition through **indices**  
    `series1 + series2`

## 2. Data Frame
### `pd.DataFrame()`
* Data Inputs:
    * ndarray
    * dict
        * dict of lists  
            `pd.DataFrame("Col_NAME":list1, COLNAME2:list2)`
            * NOTE: indices are automatically added, use dict of series instead if you want to set the indices

        * dict of dictionaries   
            `pd.DataFrame({'Dict1Key':{Dict_SUB_1key:dict_SUB_1_value}, 'Dict2Key':{dictSUB2key:dictSUB2value}})`
            * NOTE: can set value between exact col and row using this method
        * dict of series (make sure indices match)
            * NOTE: Same as list, but indices are the series indices
    * series
    * DataFrame
* 2D labelled array
* Supports multiple data types
* Input can be a series or a df
### Viewing a DataFrame
* referring to `df.column_name` or `.describe` NOTE: `.describe()` for stats info (similar to `summary()` from R)

3. Panel
    * 3D array
    * Supports multiple data types
    * Items -> axis 0
    * Major Axis-> rows
    * Minor Axis -> Cols
4. Panel 4D
    * 4D array
    * supports multiple data types
    * Labels ->axis 0
    * Items -> axis 1
    * Major Axis-> rows
    * Minor Axis -> Cols