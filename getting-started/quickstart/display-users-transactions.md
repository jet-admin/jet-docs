In this section, we will set our tool to display Stipe transactions by a specific customer. For a start, drop a table component to the page, then select Stripe as the resource, and choose the Payments collection.

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MGEKN_o1JIvz1hgs3Vm%2F-MGEKwBFBNjjn2W4OEdl%2FGIF10.gif?alt=media&token=e6b31782-9731-43b8-881a-b92ca626d6e8)

At this point, we can use the column selector again to filter out redundant data:

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MGEN6905mJPSdBhmj-l%2F-MGENn5ADnmFyd_Y_0pQ%2FGIF12.gif?alt=media&token=3d90d7e7-d115-46b2-9fd5-a4407a25303c)

## Let's specify a user for the transaction list

Let's pull a transaction list from Stripe for a specific selected customer from a table. You can use [parameters](user-guide/data/parameters) passing a `customer ID` as a value for `customer_id` parameter. 

Go to Component Settings -&gt; Data -&gt; Specify Parameters, choose the `customer ID` for the parameter as a value :  `Take value from components` to select the component from which you want to get the customer ID value. 

You will need to select the `id` field in the customer table \(`Take value from components` -&gt; `Clicked Row` -&gt; `Customers table` -&gt; `id)`.

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MGc3w6SL-VIMNB1wPzs%2F-MGc5xuCd2si3Et4SbAy%2FGIF129.gif?alt=media&token=ce396f0c-d8f7-4d39-9426-744ef2e55f74)

## Display the exact number of rows

You can set pagination to specify the number of rows to be displayed per page:

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MGES8Bn7HSsLsivt62t%2F-MGESkDmDS0FnMcxLj3v%2FGIF15.gif?alt=media&token=104ef983-db46-48fb-a138-f3367457f45f)

## Transaction Details

Let's add a Detail component to display the detailed information of the selected transaction. 

1. Drag-and-drop the Title component to set the "Transaction Details" title.

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MGc8irqKLHzQ4wAnzbC%2F-MGcBdGlhnpZEv1mnYzk%2FGIF130.gif?alt=media&token=f94dee0f-f183-44a5-8942-340d0f6da7a0)

2. Drag-and-drop the Detail component from the Data section to display the selected transaction:

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MGc8irqKLHzQ4wAnzbC%2F-MGcDo-iwEjrn3XeGigS%2FGIF131.gif?alt=media&token=f1807693-f7b2-415b-bca5-1351315a862e)

3. Select the `Stripe` resource and the `Payments` collection to display the payment:

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MGc8irqKLHzQ4wAnzbC%2F-MGcF30qRr5-HwtUQXGt%2FGIF132.gif?alt=media&token=db7f9b71-0f0a-456a-abb2-68af17fda83c)

4. Just switch checkbox to select the fields you want to display:

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MGc8irqKLHzQ4wAnzbC%2F-MGcFstx3p3AFirrPZIj%2FGIF133.gif?alt=media&token=e7eaad3a-4ec0-4acf-bd0a-d332bdbe41e0)

5. Pass `charge_id` parameter to display selected transaction. We need to pass the parameter as `take value from component`.

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MGc8irqKLHzQ4wAnzbC%2F-MGcHSbRTgWbzp9S3eF0%2FGIF134.gif?alt=media&token=52d7810f-89a2-4ef8-9e97-d85ba1bcb78c)

6. Now let's add a dynamic field to display the transaction amount so that we can change it to refund the partial amount. Simply drag-and-drop Text Field component.

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MGc8irqKLHzQ4wAnzbC%2F-MGcIPlch4wIGcDesuvX%2FGIF135.gif?alt=media&token=b1ee9261-1ce2-40b6-8279-8a158c7a8c1d)

7. Set Data as `take value from component` to pass the amount value from the selected transaction:

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MGc8irqKLHzQ4wAnzbC%2F-MGcKQXOxFqK-X4XGhfW%2FGIF136.gif?alt=media&token=59ab1bca-7f2a-4613-8857-4767d1e25bb5)

8. Select transaction to get detail:

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MGc8irqKLHzQ4wAnzbC%2F-MGcKvVY_HPZxxhts2an%2FGIF137.gif?alt=media&token=236ec617-bfa0-45a8-9ed5-f8879293cbc1)

{% page-ref page="getting-started/quickstart/refunding-money" %}



