To quickly connect a custom API use HTTP Request Builder. You can make `GET` request to visualizing orders data in Table component or `POST` request to reset a password for a specific user. 

{% embed url="https://www.youtube.com/watch?v=ajqCp3uTb-o&ab\_channel=JetAdmin" %}



## Open API Builder

1. Go to Component Settings then click `Add Data Source` 

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MG_mF4DBM_mAAf-m13M%2F-MG_oVr5n_BSODLyTPPM%2FGIF82.gif?alt=media&token=eea727d5-0cbc-4d71-bcde-74fa7341f1cd)

2. Choose Resource – [Rest API](user-guide/integrations/rest-api) then choose Collection – `Make an HTTP request`

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MG_mF4DBM_mAAf-m13M%2F-MG_otPHbSZtKiUL2OUb%2FGIF83.gif?alt=media&token=ea96bf4a-8e20-4e6d-a19a-73eed81909cd)

## Pass parameters

To pass [parameters](user-guide/data/parameters) from API Query Builder, such as `customer id` you need to specify it as a parameter.

* Go to Parameters then click +Add Field

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MGcPbu1qIXnhKLjP7VU%2F-MGcTHdYOucVZsPHBi1e%2FGIF141.gif?alt=media&token=f2803709-425e-477a-82af-baaae0d2e275)

* Specify Parameter type \(for example, Number Field for ID parameter or Text Field for Email parameter\)

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MGcPbu1qIXnhKLjP7VU%2F-MGcTw8mEKMFvjMuCRKN%2FGIF142.gif?alt=media&token=a2da39dc-2c9f-434e-b959-3883ac2b2b11)

* Mark as Required \(if you need to make this field required\)

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MGcPbu1qIXnhKLjP7VU%2F-MGcUN0hE-lZyspSkzcn%2FGIF143.gif?alt=media&token=e4267869-072e-4ec2-86c0-5eb46777684e)

* Specify query parameters

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MGcPbu1qIXnhKLjP7VU%2F-MGcYMx_9q1_HdnSDb-3%2FGIF145.gif?alt=media&token=5046b2a6-6340-464d-a86b-591b7672a2ea)

* Set `customer` value in Tokens and run query

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MGaCnX1IjAQA86jco5F%2F-MGaKJPj0BZ9US2B6c_n%2FGIF110.gif?alt=media&token=7edd5910-f4f2-4e1d-82d3-b47a4126bb81)

## Use app variable values in your request

Tokens are app variables that store Jet's data. There are different type of tokens that you can use on your requests:

* Parameters. When you create a new parameter it becomes available as tokens
* Current User. User's account properties like email, id, token, etc. available in `Current User`. You can specify [custom properties]()\)
* Pagination
* Sorting

You can specify default values for your tokens that will use in the request.

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MEKJuv9iR030XmMuORf%2F-MEN5ryopH5Cb-6r5VhT%2FGIF.gif?alt=media&token=06e675fa-e098-4c25-a67c-fb33f9c36c95)

## Transform a body of your request

To transform a body before the request is performed you can specify `Body Transformer`.  You can modify your function's return value by adding a transformer. Use the identifier `data` for the return value and enter any expressions to modify the result, such as add a property or loop over the data set. 

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MGe2XiA82wI-LireLzl%2F-MGeFdie-o041VuWxgkD%2Fimage.png?alt=media&token=5386dd6f-1f4c-4626-9c01-dc0534cc855e)

```javascript
return data['email'];
```

## Transform a response of your request

For simple transformers, you can use `response nested keys` to transform the response:

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MG_mF4DBM_mAAf-m13M%2F-MG_piPtvMIdriY7Uf_r%2FGIF84.gif?alt=media&token=2a6b22ad-4629-4026-9865-5de077b6d826)

For more complex transformers, you can use a JavaScript response transformer. The`data` is a JS variable that stores a response from your request. You can find it in Advanced Settings:

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

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MGccOmyqfa9Yot3CWOP%2F-MGceo0PY_sXBDBvo9pk%2FGIF146.gif?alt=media&token=1e62d9e2-4eb9-4b1b-8894-c13fd78bcb24)

## Sorting your data

You can sort all fields by ascending and descending value:

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MEXGnJxiDMMiiB9U_hu%2F-MEXIED-BkEPZqRYBlKg%2Fimage.png?alt=media&token=7e736d0a-fa76-4c76-8163-1d7970b452a8)

## Pagination

APIs like to send data back in pages. By default, you only get 1 page. You will need to ask for more. In your API docs, there is probably a section called Pagination. 

There are 3 types of pagination:  **page**, **offset**, and **cursor pagination**.

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MEN7lusGJUPDvMe9NsW%2F-MEO_ijjbBqchqx9MY6I%2Fimage.png?alt=media&token=e7706ce4-a4b2-47b6-8daf-1712793eacac)

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

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MEN7lusGJUPDvMe9NsW%2F-MEPZPW39puCP5jppl1n%2Fimage.png?alt=media&token=69e64b60-70ee-43ea-bfb6-697cb09cafdb)

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

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MFjjEGPoN0wZB8n51aB%2F-MFjk-_repKhaD1USpso%2Fimage.png?alt=media&token=dd9277ae-aed1-4f30-972b-28c4d92657c8)

## Cursor based pagination

Sometimes APIs use something that looks weird for their pagination. Each call may return a cursor key to use to get the next page. Something like _"_`nextPageCursor": "<cursor_key>"` or ID as the next cursor \(Stripe API\) `"next cursor" : data['data'][data['data'].length - 1].id`

For instance, **Stripe** sends back a URL as well as a cursor \(object ID\) to use to get the next page. Their docs show this:

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MEN7lusGJUPDvMe9NsW%2F-MEPWCcGwF8nrcBM8x5f%2Fimage.png?alt=media&token=6204ecaa-2a8e-48be-b752-d556e887a3b6)

You can send this in two ways. Either use the cursor or use the full URL. If you use the cursor, you need to send it in a parameter:

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MEN7lusGJUPDvMe9NsW%2F-MEPT8PmNmtUSVj_jZJ7%2Fimage.png?alt=media&token=5bc3d948-684a-47c9-b99b-f83cfab19511)

For instance, Stripe API in Jet API Builder that would be set up with these settings:

```javascript
https://api.stripe.com/v1/customers?limit={{paging.limit}}&starting_after={{paging.cursor_next}}&ending_before={{paging.cursor_prev}}
```

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MEN7lusGJUPDvMe9NsW%2F-MEPUVOy2EN8ti90PI6Y%2Fimage.png?alt=media&token=c84361af-91d1-4ce1-8c78-28331dc6dc40)

