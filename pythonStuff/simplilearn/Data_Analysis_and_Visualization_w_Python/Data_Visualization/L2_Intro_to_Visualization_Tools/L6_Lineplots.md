# 2.6 Line Plots

## Example

        import matplotlib.pyplot as plt
        years=list(map(str,range(1980,2014)))
        df_canada.loc["Haiti",years].plot(kind="line") # plotting Haiti row (countries are indexes in this df) against years (Each year is a column)
        plt.title()
        plt.ylabel()
        plt.xlabel()
        plt.show()
