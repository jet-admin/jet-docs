Let's say, we need to display order total amount on `Customer` table for each customer. All Orders we stored in the separate `Orders` table in the SQL database. 

The result`Customers`table contains: `customer_id`, `photo`, `name`, `total_amount`columns of data for each customer.

## Build SQL query using SQL Builder

1. Go to the Component Settings then `Add Data Resource`

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MGaCnX1IjAQA86jco5F%2F-MGaGGH4oL0pnZ2iIv5V%2FGIF107.gif?alt=media&token=1e47c8a1-1174-4a86-aca0-f1d27bcd39b8)

2. Select a resource \(SQL database\) then choose collection as `Make an SQL request`

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MGb_OvVEi6xZK9tivS1%2F-MGbbiVX1PFrzeIhkAtx%2FGIF117.gif?alt=media&token=3a8dd1fb-09b2-4116-8b24-0727316c016c)

## Write SQL query

Let's write a SQL query that returns customers includes the total amount column:

```sql
select 
(select sum(amount) from orders where customer_id = customerscrm.id) as total_amount,
id,
photo,
name
from 
customerscrm
```

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MGb_OvVEi6xZK9tivS1%2F-MGbcucSNZUlfpiVBir7%2FGIF118.gif?alt=media&token=88d3d5c4-f1bc-404a-bb9d-0b71387d2d02)

## Tips

Here is a list of your available tables, you can see the table columns. You can use them while writing SQL, just click on the table name and the name will be automatically added.

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MGb_OvVEi6xZK9tivS1%2F-MGbdbnDARXgDvu6TbTh%2FGIF119.gif?alt=media&token=4c64361a-82d0-418e-89f5-b9617f90f063)

## Run your SQL query

Simply click `Update Result` button to run your SQL command.

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MGb_OvVEi6xZK9tivS1%2F-MGbe8JDvVonoeXxltFU%2FGIF120.gif?alt=media&token=fdf0aed6-c87a-4886-8b56-b0cbfcd98765)

## Customize table

Just close SQL Query Builder to start to customize the result table.

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MGb_OvVEi6xZK9tivS1%2F-MGbehytc7zFuHma4cMT%2FGIF121.gif?alt=media&token=b2701a9e-547c-4a4a-80d8-3150651ef8d6)

{% page-ref page="user-guide/data/make-a-sql-query" %}

