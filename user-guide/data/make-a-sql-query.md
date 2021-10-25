[comment]: # ($page_title=Making SQL queries)
[comment]: # ($page_description=An overview of SQL request with PostgreSQL)

To quickly configure the display of your data from a database, you can build SQL queries by selecting Custom SQL. 

## Open SQL Query Builder

You can open the SQL Builder directly from the component simply by selecting the SQL resource. The SQL Builder will be opened automatically in case you do not create any collections yet, otherwise you will need to select Make SQL Query from the list of collections for your SQL resource:

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MjehuplWWd6OK_2hI_D%2F-MjeidvxKZ6geBub4A1n%2Ftestgif42.gif?alt=media&token=36bfd635-665e-492a-942f-108a64ea512a)

## Pass Inputs

To pass [values](user-guide/parameters) from SQL Query Builder, such as `id`or `email`, you need to specify them within the Inputs tab:

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MjehuplWWd6OK_2hI_D%2F-MjeisIsNwvdh6JOrgjr%2Fimage.png?alt=media&token=4be7a963-9d44-4529-89e3-e31b232132df)

## Use inputs in the query

For example, you need to select data with a specific `id` or `email`from the table, you can make an SQL query and use the parameters:

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MjZ3LfsU1ZReomd0nUz%2F-MjZ6Tonqdbn2e2wxgfC%2Ftestgif13.gif?alt=media&token=df427cc1-c46f-4611-a8fd-750ad9a8e016)

## Migrating from old Inputs syntax \(before Jet Admin v2.4.0\)

Since **Jet Admin v2.4.0** we have changed the way how parameters are inserted in SQL query. Now you don't need to surround parameter value with quotes. **Previously saved queries will continue to work, but you will need remove unnecessary quotes when you will be changing the query \(or use compatibility flag described below\).**

```sql
SELECT * FROM people WHERE 
city = {{params.city}} 
AND age >= {{params.age}} 
AND name ILIKE {{'%'+params.search+'%'}}

# Before Jet Admin v2.4.0

SELECT * FROM people WHERE 
city = '{{params.city}}' 
AND age >= {{params.age}}
AND name ILIKE '%{{params.search}}%'
```

You can use **compatibility flag** if you want to stay with old parameters syntax, but it will be deprecated at some moment. Just insert the following option at the top of the query.

```sql
-- @JET_QUERY_VERSION=1
SELECT * FROM people WHERE city = '{{params.city}}'
```

