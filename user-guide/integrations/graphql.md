GraphQL is an API design architecture that takes a different, more flexible approach. The key difference between GraphQL vs REST is that GraphQL doesn’t deal with dedicated resources. Instead, everything is regarded as a graph implying it’s connected.

What this means in practical terms is that you can tailor your request to match your exact requirements using the GraphQL query language. In addition to this, it lets you combine different entities into a single query.

A GraphQL query for a movie listings app might look something like this:

```graphql
{
  characters {
    results {
      id
      name
      status
      species
      type
      gender
      origin {
        name
        id
      }
    }
  }
}
```

## 1. Add your GraphQl resource 

To connect GraphQL to JetAdmin, add a new resource from the settings and select GraphQL or select GraphQL as the resource when creating a new project.



![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MjZ3LfsU1ZReomd0nUz%2F-MjZDXsEBzZTuXAkp_Zx%2Fimage.png?alt=media&token=b3d3b3df-0908-420f-9c05-872a7434a72d)

Then, enter your API endpoint in the **Base URL** field. Base URL example: 

```text
https://rickandmortyapi.com/graphql
```

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MjZ3LfsU1ZReomd0nUz%2F-MjZbpDoywpOsDY4ZDUX%2Fimage.png?alt=media&token=04f6082f-930b-44c7-bcb6-c2eb964da41b)

Depending on your API authentication settings, you may need to enter URL parameters or headers, or set the method via the [Authentication](user-guide/integrations/rest-api) dropdown.

## 2. Make a request

You can display the results of GraphQL queries as with any other query in Jet Admin.

```graphql
{
  characters {
    results {
      id
      name
      status
      species
      type
      gender
      origin {
        name
        id
      }
    }
  }
}
```

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MjZ3LfsU1ZReomd0nUz%2F-MjZcE0VucAy7u9OULRO%2Ftestgif15.gif?alt=media&token=81051de3-a51a-4d89-9fcf-92879679d8b4)

More information about HTTP Requests in our documentation.

{% page-ref page="user-guide/data/make-an-http-request" %}

