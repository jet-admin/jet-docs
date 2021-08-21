To quickly configure the display of your data from a database, you can build SQL queries by selecting Custom SQL. 

## Open SQL Query Builder

1. Go to Component Settings then click `Add Data Source`

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MG_psD4L-Hj5eIFJ5Fj%2F-MG_q_FOrInMGFQmtdPV%2FGIF85.gif?alt=media&token=951fc8fe-7bd5-4545-8e1c-8816b4cf71a6)

2. Choose Resource – SQL Database \(PostgreSQL, MySQL\) and Collection – `Make an SQL request`

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MG_psD4L-Hj5eIFJ5Fj%2F-MG_rIlgt6vOUvq5B4ry%2FGIF85.gif?alt=media&token=c2690e0a-c599-4161-9075-cba2a7387f58)

## Pass parameters

To pass [parameters](user-guide/data/parameters) from SQL Query Bilder, such as `id`or `email`, you need to specify them in the Filters field in the SQL Builder.

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MEPZl5nXUqkFwLq4_KD%2F-MEPahFJVPcXkJzGRm0r%2Fimage.png?alt=media&token=fade7e77-60e5-4a74-9647-f8672b6aa8ab)

## Use app variable values in your request

Tokens are app variables that store Jet's data. There are different type of tokens that you can use on your requests:

* Current User
* Parameters
* Sorting
* Tables Tokens

You can specify default values for your tokens that will use in the request.

For example, you need to select data with a specific `id` or `email`from the table, you can make an SQL query and use the parameters:

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MEPZl5nXUqkFwLq4_KD%2F-MEPbss00zUEyU8YHT_o%2FGIF.gif?alt=media&token=1f0e2183-d891-4591-a9a8-4318b732f7de)

## Run an SQL query

Simply click Update results button to run SQL command:

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MGcwezTmpMCVHgRFJgC%2F-MGdSpufwMc1GRdf8oY6%2FGIF149.gif?alt=media&token=70c1902a-67b6-4a3e-8d0b-76ff95ebf13e)

