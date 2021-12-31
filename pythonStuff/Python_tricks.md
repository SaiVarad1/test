# Python Coding tricks to Remember

## Creating dictionaries
Creating from list (using enum and for loop) \
`list_eg=['name1','elem2','elem3']` \
`list_map=dict((name,index) for index,name in enumerate(list_eg))`

## Reading excel files
Can choose specific cell range for pandas as df using `pd.read_excel(filepath,sheetname,skiprows,usecols='B:G')`

## Pd.Dataframe
* Converting Dataframe to arrays:\
`arr=df.to_numpy()`
    * If you need to convert the df columns to arrays, just transpose the above `np.transpose(arr)`
* Dropping NAs from a df column:
    `df.dropna(subset=["colName"], axis=0)`
* Selecting columns:
   *  `df[['col1','col2']]`
   * `df[['col1','col2']].describe()`
* `df.info`
### Binning a Column of a Df
1. Create bins intervals  
    `bins=np.linspace(min(df["orig_col"]), max(df["orig_col"], number_of_intervals)`
2. Create List of names for intervals  
    `groups_list=['bin1', 'bin2', 'bin3']`
3. Add new column to Dataframe by cutting original column  
`df["new_col"]=pd.cut(df["orig_col"], bins, labels=group_list, include_lowest=TRUE)`

We can see that four doors are the most common type. We can also use the ".idxmax()" method to calculate for us the most common type automatically:
`df['num-of-doors'].value_counts().idxmax()`

### Viewing unique values in a df
`df[col].unique()`

## Pearson Coeff
`pearson_coef, p_value = stats.pearsonr(df['wheel-base'], df['price'])`
## NumPy
* Equally spaced array  
`np.linspace(1,10,3)`


