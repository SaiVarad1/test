# 3.3 Histogram
* Represents frequency distribution of variable  
`df["col"].plot("kind="hist")` # Histograms ticks won't align with bars
    * use np.histogram
        * `count,bin_edges=np.histogram(df["col"])`
        `df["col"].plot(kind="hist",xticks=bin_edges)`