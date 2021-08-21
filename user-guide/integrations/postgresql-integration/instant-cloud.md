The quickest way to integrate database \(**localhost** not valid, use [**Docker**](user-guide/integrations/postgresql-integration/docker-installation) ****or [**Python**](user-guide/integrations/postgresql-integration/python-app-installation) ****integration instead\). We encrypt all data and credentials that go through our servers using an HTTPS connection.

You'll need to fill out the following form:

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MEATPYmRPkKrbdBF-ss%2F-MEATsLNP6T7IfV1ALfq%2Fimage.png?alt=media&token=fed518f0-c18e-4968-9997-9cf489e076e4)

| Name | Description |
| :--- | :--- |
| Host | The IP address or hostname \(db.example.com\) of where your database instance resides. Note, `localhost` and **`127.0.0.1` are not valid!** Make sure it is accessible from these IPs: `95.179.253.121` |
| User | Username for this database |
| Password | Password for this database |
| Database Name | The name of the database you would like to interact with. |
| Database Port | Port to connect to. By default PostgreSQL: 5432 |
| PostgreSQL Schema  | Your database schema \(`optional`\) |
| Extra Parameters | Extra parameters, ex. charset=utf8 \(`optional`\) |

## Make a SQL queries

Using Database integration you can make simple or [SQL queries](user-guide/data/make-a-sql-query) to your database:

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-ME-iIaphZMtnaaHk2WV%2F-ME-lQVBeLBZC_ybD9gX%2FGIF.gif?alt=media&token=2d26a6b0-a9be-4038-9468-4297abad1000)

Here is a [step-by-step guide](jet-bridge-deployment/database-heroku-deployment) to deploying the database to Heroku and finding your credentials.

{% page-ref page="jet-bridge-deployment/database-heroku-deployment" %}

