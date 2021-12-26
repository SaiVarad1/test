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