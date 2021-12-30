# 4.7 GroupBy in Python

## Pandas dataframe.Groupby()
* Categorical Variables
* Groups on single or multiple variables


## Example
`df_test=df["drive_wheels","body-style","price"]`  
 Grouping data on body-style and 'drive-wheels'

 `df_grp=df_test.groupby(['drive_wheels","body-style"],as_index=False).mean()` 

 ## pd.Pivot()
 One variable is displayed along columns while the other is displayed along rows 

 `df_pivot=df_grp.pivot(index='drive-wheels',columns='body-style')`

 ## Heatmap
 * Plot target variable over multiple variables  
 `plt.pcolor(df_pivot, cmap='RdBBu')`  
 `plt.colorbar()`  
 `plt.show()`
