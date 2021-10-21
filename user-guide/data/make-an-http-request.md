To quickly connect a custom API use HTTP Request Builder. You can make `GET` request to visualizing orders data in Table component or `POST` request to reset a password for a specific user. 

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-Mjh4WH_3plDnw1Mr2q1%2F-Mjh4voR0KQJ3Hlq1UTt%2Fimage.png?alt=media&token=3260a4a8-3dfc-4d82-a13d-783a4deb02e5)

Watch the video below on how to get API Builder set up!

{% embed url="https://www.youtube.com/watch?v=ajqCp3uTb-o&ab\_channel=JetAdmin" %}



## Open API Builder

You can open the API Builder directly from the component simply by selecting the Rest API resource. The API Builder will be opened automatically in case you do not create any collections yet, otherwise you will need to select Make HTTP Request from the list of collections for your Rest API resource:

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MjeajOjNWzJRcYkJVpo%2F-MjeczoFF0YERqnV7vL3%2Ftestgif38.gif?alt=media&token=3d14016b-81bd-45e9-ada6-6cb5782a34dc)

## Pass Values to API Builder

To pass [Values](user-guide/parameters) to **API Builder**, such as `charge` you need to specify **Inputs**.

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MjeajOjNWzJRcYkJVpo%2F-MjefXqit0bVQoQhOsui%2Ftestgif39.gif?alt=media&token=39e6d7ae-9e38-40ef-b60f-f591cdb706a4)

## Visual Response Transformer

You can transform the data from the response with a Visual Response Transfomer:

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MjeajOjNWzJRcYkJVpo%2F-MjegEFlOmU7YJNhGDdb%2Ftestgif40.gif?alt=media&token=15b397a0-aac6-477c-ad7b-9d51ccaad25d)

## JavaScript Response Transformer

If you need custom transformation you can use a JavaScript response transformer. The`data` is a JS variable that stores a response from your request. Javascript transformation:

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MjeajOjNWzJRcYkJVpo%2F-MjeggjKodSSv8yV-_bg%2Ftestgif41.gif?alt=media&token=77d70c1f-db00-42d6-8376-ed3b533f2689)

For example, you can use JS functions to parse the data:

```javascript
function getProperties(data) {
    result = {};
    for (var key in data) {
        result[key] =  data[key]['value'];
    }
    return result;
}

function contactMapper(contactData) {
    result = getProperties(contactData['properties']);
    result['dealId'] = contactData['dealId'];
    return result;
}
return  data['deals'].map((x)=>contactMapper(x));
```

## Sorting your data

You can sort all fields by ascending and descending value:

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MjeajOjNWzJRcYkJVpo%2F-Mjeh13QsTS31gOFNWy1%2Fimage.png?alt=media&token=6b28322e-d690-4123-8db7-df47ed45438f)

## Pagination

APIs like to send data back in pages. By default, you only get 1 page. You will need to ask for more. In your API docs, there is probably a section called Pagination. 

There are 3 types of pagination: **page**, **offset**, and **cursor pagination**.

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MjeajOjNWzJRcYkJVpo%2F-Mjeh7Tik3XOqATBsA_4%2Fimage.png?alt=media&token=8c69d74b-b8c6-4cd9-9f7a-5e100af4a5da)

## Page based pagination

If you see the mention of a numerical page number that you increment to get each page, then you are in the right place.

Intercom uses this style of pagination. And it looks like this in their docs:

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MEN7lusGJUPDvMe9NsW%2F-MEPYVTsk1ywtvFYEr8I%2Fimage.png?alt=media&token=23edd633-f704-4a05-bedf-4a016d67a588)

 The first page from this endpoint would look like this: `https://api.intercom.io/users?page=0`

```javascript
$ curl https://api.intercom.io/users?page=0 \
-H 'Authorization:Bearer <access_token>' \
-H 'Accept:application/json'
```

In API Builder that would be set up with these settings:

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MjeajOjNWzJRcYkJVpo%2F-MjehP__TaOg0tzuG1ac%2Fimage.png?alt=media&token=510011fb-9212-4eda-956d-8cb01fd8d181)

## Offset pagination

If you see the word `offset` in your API docs, this is the style for you. **Hubspot** uses this style. Their docs say:

Some endpoints support a way of paging the dataset, taking an offset and limit as query parameters:

```javascript
https://api.hubapi.com/v1/deals/v1/deal/paged?offset=20&limit=20

```

In this example, in a list of 20 \(`total`\) singles by the specified deal: from the twentieth \(`offset`\) deal, retrieve the next 10 \(`limit`\) deals.

In Jet API Builder that would be set up with these settings:

```javascript
https://api.hubapi.com/v1/deals/v1/deal/paged?offset={{paging.offset}}&limit={{paging.limit}}
```

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MjeajOjNWzJRcYkJVpo%2F-MjehZ-rj12DLFeO5VIJ%2Fimage.png?alt=media&token=0acb47b8-ea1f-409d-884a-39d46ac03991)

## Cursor based pagination

Sometimes APIs use something that looks weird for their pagination. Each call may return a cursor key to use to get the next page. Something like _"_`nextPageCursor": "<cursor_key>"` or ID as the next cursor \(Stripe API\) `"next cursor" : data['data'][data['data'].length - 1].id`

For instance, **Stripe** sends back a URL as well as a cursor \(object ID\) to use to get the next page. Their docs show this:

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MEN7lusGJUPDvMe9NsW%2F-MEPWCcGwF8nrcBM8x5f%2Fimage.png?alt=media&token=6204ecaa-2a8e-48be-b752-d556e887a3b6)

You can send this in two ways. Either use the cursor or use the full URL. If you use the cursor, you need to send it in a parameter.

For instance, Stripe API in Jet API Builder that would be set up with these settings:

```javascript
https://api.stripe.com/v1/customers?limit={{paging.limit}}&starting_after={{paging.cursor_next}}&ending_before={{paging.cursor_prev}}
```

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MjeajOjNWzJRcYkJVpo%2F-MjehsUdpDGygv5JTn4M%2Fimage.png?alt=media&token=db8dbaa5-a8f5-4561-bd9e-963cbd1ca317)

