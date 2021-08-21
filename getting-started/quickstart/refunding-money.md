Finally, we would like to be able to make a refund whenever a customer's transaction meets specific conditions. The easiest way to do so seems to be by pressing a button. Therefore, we shall just add a button to our tool and then have the button work the way we want it to.

1. Drag-and-drop the button component to the page:

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MGEhzI6OmLytAXIpgS6%2F-MGEn5LlVXwZsJ9_oXfD%2FGIF18.gif?alt=media&token=5725d709-74fb-40d0-9d6e-e31fbf7f2937)

2. Choose **Run Operation** as the type of the action the button performs, Stripe for the data resource and then set the operation as **Refund**:

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MGEhzI6OmLytAXIpgS6%2F-MGEnSBkX-CkvkL69OLa%2FGIF19.gif?alt=media&token=74c1b99c-a7ac-4233-823e-71efdea3df17)

3. To build a simple workflow that we can manage by pressing a button, we need to describe our projected daily routine as some logic: as soon as there's a charge to be refunded, we can enter certain amount and send it back to the customer's card. To identify a charge, select the charge ID and the amount as shown below: 

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MGEhzI6OmLytAXIpgS6%2F-MGEpHHlH2Hed5VNrFW9%2FGIF23.gif?alt=media&token=e27ac015-9475-4275-95d1-72e4719d5222)

4. The operation is now ready to be run:

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MGEhzI6OmLytAXIpgS6%2F-MGEplfB8AB8DtK1FXA7%2FGIF24.gif?alt=media&token=39539d7b-863a-439e-9042-0ba91839b5d4)

{% page-ref page="getting-started/quickstart/adding-a-chart" %}

