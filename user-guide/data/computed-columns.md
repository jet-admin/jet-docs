[comment]: # ($page_title=Computed Columns)

You can create custom columns in a table to handle cases such as math operations on your data, parsing JSON fields, or creating conditions. Let's look at a few examples of how to use it:

## Example 1: Use formulas over your data

In this use case we will create a custom column in the Customer table and calculate a score depends on some logical condition.

1. Simply create a new Custom field in columns settings of table component. 

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MjgtXzTjBj2m2d5c1pE%2F-MjgwCxBeR0Ov1R9UE3A%2Ftestgif52.gif?alt=media&token=68d89b06-0ffa-4c89-b42e-bc8746e7de5c)

2. Now we should configure Value for that Column using Formulas. We will use `IF` function to calculate Scores value, depending on Activities number for each customer:

`=IF(item.activities < 280, '50 points', IF(item.activities < 400, '70 points', '100 points'))`

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MjgtXzTjBj2m2d5c1pE%2F-MjgwPkqpSH2mSxdAJHn%2Ftestgif53.gif?alt=media&token=e3655496-2c2d-4ed7-a04f-31be790fb1c7)

## Example 2: Math operations over your data

Let's suppose you need to calculate the total cost by multiplying the Price and Quantity fields:  
  
1. Simply create a new Custom field in columns settings of table component:

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MkLCtEM0yOqTTl7SN8l%2F-MkLI4sDNOiUbTNSEVyW%2Ftestgif77.gif?alt=media&token=8ca2132f-d68d-494e-9595-c749991c05ba)

2. Now we should configure Value for that Column. We will use \* operation to calculate Total cost value:

`=item.Price * item.Quantity`

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MkLCtEM0yOqTTl7SN8l%2F-MkLIXRo1hBGbPdHqboA%2Ftestgif78.gif?alt=media&token=0ead493a-e308-4325-b921-1f04a1c2c552)

3. Now let's concatenate the Total cost with the currency $ using CONCAT\(\) function: 

`=CONCAT("$", item.Price * item.Quantity)`

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MkLCtEM0yOqTTl7SN8l%2F-MkLJ4xTsl5Cvwey3Cri%2Ftestgif79.gif?alt=media&token=36abc463-b3c0-4212-bbe4-add5a86cb404)

## Example 3: Parse JSON columns

Suppose you have a field that stores data in JSON format. You can display the desired data in a separate column. The JSON structure shown in the example: 

```javascript
{
  "fields": {
    "pricing": {
      "integerValue": "109"
    },
    "quantity": {
      "integerValue": "98"
    }
  }
}
```

1. Simply create a new Custom field in columns settings of table component:

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MkLCtEM0yOqTTl7SN8l%2F-MkLLSvokuFinLjmjizJ%2Ftestgif80.gif?alt=media&token=646b0e34-e54f-4af4-b060-c9b112664d7c)

2. Now let's display the Pricing value in a separate column. For the JSON structure shown in the example above, you need to use the following value:

`=item.order.fields.pricing.integerValue`

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MkLCtEM0yOqTTl7SN8l%2F-MkLLrYat5hTQNbfraXE%2Ftestgif81.gif?alt=media&token=30b9bf05-039b-4bf0-a77f-7832324940f3)

Now your data is displayed in a clear and readable way in a separate column.

{% hint style="info" %}
Note that the value may differ depending on the JSON field structure.
{% endhint %}

