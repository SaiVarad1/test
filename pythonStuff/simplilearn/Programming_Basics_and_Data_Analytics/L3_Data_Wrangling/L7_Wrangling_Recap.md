# 3.7 Pre-processing Data in Python

* Identify/Handle Missing Values
    * df.replace("?",np.nan, inplace=True)
    * Evaluating for Missing Data
        * missing_data=df.isnull()
            * Generates Boolean table
        * Counting missing values in each column
            * missing_data[column].value_counts()
    * dealing with missing data
        * drop or replace data
            * replace mean, frequency etc
* Data Formatting
    * df[["","".astype("float")]]
* Data Normalization
    * Z score, divide by max, etc
* Data Binning
    * np.linspace()
* Turning Categorical Values to Numeric Variables
    * hot encoding
        * pd.get_dummies(df["cols"])
        * pd.concat(df, getdummies)