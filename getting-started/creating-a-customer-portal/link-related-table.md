[comment]: # ($page_title=Link Related Tables)

You can **link different tables** as long as there's a common field in both of them. In our case, we'll link by the `Project name` field.

{% hint style="info" %}
In Jet Admin you can link tables from **different Bases**
{% endhint %}

## Display the Projects

Drag the `Table` component and change the mock data to your own. Select the data source you've connected and the page you want to display:

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-Mj-RfSLs9dEAC_NRUL8%2F-Mj-_l5DUiATl62Ew0X9%2FQuickstart-portal5.gif?alt=media&token=bde8a086-9939-4e58-9448-ca4f70019171)

## Link the Tables

Each `Project` has many `Tasks` and we want to see the list of `Tasks` for a given `Project`. To create this flow, we need to **dynamically filter** the `Tasks` table by the `Project name` value, obtained from the selected row in the Projects table. For this, Jet Admin has the **Formulas** modal window, where you can map the components:

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-Mj-ss64tLpMELW8d5Xn%2F-Mj014YoZIvc8TUEFdD_%2FQuickstart-portal8.gif?alt=media&token=1f6e598a-8330-4258-ae51-fd3ebb74d053)

And we've got our tables **linked**:

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-Mj-ss64tLpMELW8d5Xn%2F-Mj01Xyg3gu5JOdQrPKf%2FQuickstart-portal9.gif?alt=media&token=14b011a4-1726-4496-a3c4-a3df74dc1039)

Now, let's **customize** our Portal:

{% page-ref page="getting-started/creating-a-customer-portal/customize-your-portal" %}

