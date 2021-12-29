# 3.2 Data Formatting

## Calculations to an entire Df Column:

`df["city-mpg"]=235/df["city-mpg"]`

## Renaming Columns
`df.rename(columns={"city_mpg:city-L/100km", inplace-True})`

## Changing datatype of Col
`df["price"]=df.astype("int")`