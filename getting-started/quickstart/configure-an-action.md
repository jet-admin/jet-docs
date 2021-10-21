There are different sorts of **actions** that can be set in Jet Admin: `update a record`, `create a record`, `mass-delete`, `export`, custom `SQL/API queries`, and more. Every action can be triggered by `buttons` or components' functions, such as `row click`.

For our case, let's drag and drop a `button`, select `Run operation` then select the **data source** and the **collection** you want to update:

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MibfkEEy6_1P2EGaXDX%2F-MicAufZ84vmymZerwkW%2FQuickstart-components8.gif?alt=media&token=676079a8-a9d0-4873-a5b6-3b4c66b18f93)

{% hint style="info" %}
When you connect databases, Jet Admin generates all the **CRUD operations** automatically, so you need only to choose the right collection and the right type of operation
{% endhint %}

Now, we need to specify all the fields for the `Customers-Update` operation. First of all, we need to set which record our button will update - for that we'll get the row value from the `selected row` of the `Customers` table:

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MibfkEEy6_1P2EGaXDX%2F-MicDj1orzHUICpthcTy%2FQuickstart-components9.gif?alt=media&token=b2e6d43e-87a3-4f87-81a0-1adb8aa3bb0d)

{% hint style="info" %}
Depending on a data source, the **identification field** might be different: `Id`, `Document path`, `Document ID`
{% endhint %}

Next, we need to obtain the `Stage` and the `Amount` values from the `Input fields` - thus providing the editing functionality in the app:

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MibfkEEy6_1P2EGaXDX%2F-MicFnriQONOjwXmPQcW%2FQuickstart-components10.gif?alt=media&token=c9e454de-decc-4ae7-be2c-2503c3a4c2c2)

The next step is to customize or app's **appearance**:

{% page-ref page="getting-started/quickstart/customize-your-app" %}

