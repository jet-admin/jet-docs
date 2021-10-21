To create custom **user flows** in your app, you need to be able to pass values between components. For this, Jet Admin has the `Formulas` modal window, where you can map the components:

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MibVvskqBYKMjIK3SFW%2F-Mibc7lUHF6PCHCEhazj%2FScreenshot%20%2831%29.png?alt=media&token=1236731f-09f7-4b3b-ac24-6f603f28ee58)

In our example, we need the `Stage` and the `Amount` values to be fetched from the selected customer in the `Customers` table:

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MibVvskqBYKMjIK3SFW%2F-MibazUBpPedmENaLv_s%2FQuickstart-components7.gif?alt=media&token=9670aa47-1299-418a-bdd0-e3dda16636c7)

Now, let's set up an **action** that will `update` our customer record with the input values:

{% page-ref page="getting-started/quickstart/configure-an-action" %}

