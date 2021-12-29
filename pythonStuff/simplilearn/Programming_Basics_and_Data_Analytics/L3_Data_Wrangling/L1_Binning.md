# 3.2 Binning

* Equally spaced intervals using numpy Linspace
Example: Price column of df
1) Bin into categories: Low, Medium, High
    * bins.linspace(min(df["price"]), max(df["price"]), 4)
    * group_names=["Low", "Medium", "High"]

    * df["new_col"]= pd.cut(df["price"], bins, labels=group>names, include_lowest=TRUE)
