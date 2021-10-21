The related field allows you to represent the relationships between related records by creating links between them. This is particularly helpful when you have multiple tables of related items. For instance, if you have a table of customers and a table of companies, you can use a related field to link each contact to the company that they work for.

Here we'll show how to simply create a related Company field for each Customer. Each customer has `company_id`, to display and link the company in the Customer table let's specify `link to record`. There are 3 steps to set up a related field: 

1. Specify type for a `company_id` column as `Link to record` 

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MjgzYf2toGikK-ZWqKp%2F-Mjh-y9COEk9Hahsw53l%2Ftestgif58.gif?alt=media&token=e98303e8-166b-462f-bef2-41728f1f7803)

2. Specify `related collection` then select `related field` and select `Display field` to display it on the Customer table:

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MjgzYf2toGikK-ZWqKp%2F-Mjh0L6fr22D7C8uJ7rK%2Ftestgif59.gif?alt=media&token=8676ebcb-87ec-4807-9928-c04c10959f25)

{% hint style="info" %}
Related field and Display field are set automatically under the context but you can change these values.
{% endhint %}

