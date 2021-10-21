**Single relations** help you fetch data from the **related collections**. 

To illustrate how it works, let's imagine we have the `Transactions` table that doesn't contain a **customer's email** and the `Users` table that contains the customer information including the email:

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MkNJppa1ZfoM33DXJBQ%2F-MkNPkf61ukzo95Sex7S%2Fimage.png?alt=media&token=54d96850-ae15-4bab-aa1f-9844298b2819)

And we want to **display the email** in the `Transactions` list:

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MkNJppa1ZfoM33DXJBQ%2F-MkNSOI-p4c83n5VXJT5%2Fimage.png?alt=media&token=489cfb7f-3b49-4543-b938-b56c12e5c0c1)

First of all, we identify how our tables are **related**: for each user, there are several transactions that are related to the users list by the **ID** and **Customer ID fields:**

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MkNJppa1ZfoM33DXJBQ%2F-MkNN1Zfv7MgU1uT4A6a%2Fsdhx.PNG?alt=media&token=c2ff7cac-cc06-42e0-b299-b12ee38aba8a)

Now, let's create a new **custom column** in the `Transactions` table:

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MkNJppa1ZfoM33DXJBQ%2F-MkNTfKtz24SDPcnPcsU%2Fdeep1.gif?alt=media&token=86bdd404-fd0e-44fb-8fca-cfc1ccb92102)

Then change the **column type** to `Link to record`

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MkNJppa1ZfoM33DXJBQ%2F-MkNUgvW4-UXL5u_HPQL%2Fdeep2.gif?alt=media&token=65118cb9-01b9-40e8-a383-d6c2d8e78a60)

Now, we need to select where we'll get the user email from \(a related `Users` table\), what field in the `Users` table is used to set relations with the `Transactions` table \(the `ID` field\), and what field from the `Users` table we'd like to display \(the `Email` field\):

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MkNJppa1ZfoM33DXJBQ%2F-MkNWT6xG9xGbSQ0OZDQ%2Fdeep3.gif?alt=media&token=5b0a4b91-7a2d-42ec-84b9-30e9432a54c6)

And the **final step** is to get our custom field value from the `Transactions` table field that sets relations to the `Users` table \(the `Customer ID` field\):

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MkNJppa1ZfoM33DXJBQ%2F-MkNXnKZh7yXZuEOwA7k%2Fdeep4.gif?alt=media&token=608989ad-a4a8-4da0-8610-d3b07b5b2c4a)

Now, let's make UI components **dynamically visible** based on a rule:

{% page-ref page="getting-started/part-2-intermediate/conditional-visibility" %}

