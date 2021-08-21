For instance, you need to make your own API request, just choose `Make an HTTP request` as an operation. Let's look at an example of how to get a list of transactions. We are going to display a list of transactions in the table component with the Stripe API \(you can use any API\). 

## Make API request using API Builder

1. Go to the Component Settings then `Add Data Resource`

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MGaCnX1IjAQA86jco5F%2F-MGaGGH4oL0pnZ2iIv5V%2FGIF107.gif?alt=media&token=1e47c8a1-1174-4a86-aca0-f1d27bcd39b8)

2. Select a resource then choose collection as `Make an HTTP request`

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MGaCnX1IjAQA86jco5F%2F-MGaGkBy_N-7hBnxwcdy%2FGIF108.gif?alt=media&token=37c72ebc-4e46-4ce1-87d1-03098ad6a8a0)

## Pass API parameters

Now you are in API Query Builder. Specify `endpoint` and add new `customer` parameter \(to return charges for the customer specified by this customer ID\)

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MGaCnX1IjAQA86jco5F%2F-MGaHy_w34V1wrIzM6Ak%2FGIF109.gif?alt=media&token=5e466124-cb10-4ec7-a31e-16fbcf1998e9)

## Use tokens on your API request

When you create a new parameter it becomes available as tokens. You can set a value for the parameter to request a list of customer's transactions.

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MGaCnX1IjAQA86jco5F%2F-MGaKJPj0BZ9US2B6c_n%2FGIF110.gif?alt=media&token=7edd5910-f4f2-4e1d-82d3-b47a4126bb81)

## Transform your response

To transform the response, use the `Response Nested Keys` to specify the result of your request:

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MGaCnX1IjAQA86jco5F%2F-MGaLC0_yXdfPSDZ9dVW%2FGIF111.gif?alt=media&token=43e67b85-a696-4923-a726-8f0b50f7955d)

## Paginate by pages

To paginate by the list of pages specify `cursor pagination` :

1. Select `Cusror Pagination` as `Pagination`:

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MGaCnX1IjAQA86jco5F%2F-MGaMCzVraeF3xgeyCp2%2FGIF112.gif?alt=media&token=a60e513c-1a55-4197-9b9f-e32f2528b821)

2. In general, `Cursor pagination` is specified by `next_cursor`, `has_more` parameters. To parse the response we use Javascript notation. You can modify your function's return value by adding a transformer. Use the identifier `data` for the return value and enter any expressions to modify the result, such as add a property or loop over the data set. 

* `next_cursor` as `data['data'][data['data'].length - 1].id`  
* `has_more` as`data['has_more']`

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MGaCnX1IjAQA86jco5F%2F-MGaNHEIEmnaxooVQifi%2FGIF113.gif?alt=media&token=8dda8a2a-3ef7-42ce-b309-d73a522874a1)

3. Let's specify the request by providing `Query Params`:

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MGaCnX1IjAQA86jco5F%2F-MGaOK2R4eDUDGrW18GQ%2FGIF114.gif?alt=media&token=a847de7b-19cf-44c6-8b32-b0377940093b)

## Run your request

Simply click `Refresh Data` button to run your request

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MGaCnX1IjAQA86jco5F%2F-MGaOqz4e7OUcHDFXp0x%2FGIF115.gif?alt=media&token=cc0aae1c-ed04-48a3-b638-0d05265d4199)

{% page-ref page="user-guide/data/make-an-http-request" %}

