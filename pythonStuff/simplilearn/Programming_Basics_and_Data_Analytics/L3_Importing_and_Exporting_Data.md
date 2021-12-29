# 2.3 Importing and Exporting Data in Python


## Importing Data
* Format
    * .csv, ,json,.xlsx,.hdf

* File Path of Dataset

## Importing a CSV into Python
* `df.read_csv(url)`
    * If no headers in file  
        `df.read_csv(url,headers=None)`

## Printing Df in Python
* `df.head(n)`
* `df.tail(n)`

## Adding Headers
`df.columns=headers_list`

## Exporting df 
`df.to_csv(filepath)`

| reading | writing |
| ---|---|
|pd.read_csv() | df.to_csv() |
| pd.read_json() | df.to_json()|
|pd.read_excel() | df.to_excel()|
|pd.read_sql()| df.to_sql()|
pd.read_hdf() | df.to_hdf()
