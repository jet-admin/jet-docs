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

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MEATPYmRPkKrbdBF-ss%2F-MEAVOFF4g25gq8s82JV%2Fimage.png?alt=media&token=3145497b-4998-40ff-bee5-71d65283ef68)

Then, enter your API endpoint in the **Base URL** field. Base URL example: 

```text
https://rickandmortyapi.com/graphql
```

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MEEy8r9TeZrjti2WcdH%2F-MEF25PppwrA56qG8VfX%2Fimage.png?alt=media&token=05f3c209-f0b2-4007-8743-893dc7298078)

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

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-ME-iIaphZMtnaaHk2WV%2F-ME-nqvLeHYkRZxlh5Dd%2FGIF.gif?alt=media&token=d0451ec8-ae32-4b5d-a6be-368e24e88379)

More information about HTTP Requests in our documentation.

{% page-ref page="user-guide/data/make-an-http-request" %}

