Before we get into the nuances of using a modal in a JetAdmin app, it’s probably worth taking a moment to define what a modal is in the first place. 

Modals are windows - both large and small - that “pop” onto the screen when an action is taken. Sometimes these come in the form of a warning \(e.g. “Are you sure you want to delete that?”\) and sometimes they can be in the form of something useful \(e.g. clicking a "view details" button and seeing the specifics about an object\). 

Modals allow you to both save space as well as present the right information, at the right time.

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-Ml8zvhKJwyAnCOLVjcY%2F-Ml978cHRXfoe6zZKzk_%2Ftestgif97.gif?alt=media&token=de4bb6e0-d198-484b-bab7-414c923a85c9)

## The basics and properties

To add a modal into your application, find button in the component sidebar on the right and drag in onto the page. It will look just like a normal button at first, so don’t be alarmed. To see the modal in action, click the button. Once you do so, you’ll see the modal window pop up.

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-Ml8zvhKJwyAnCOLVjcY%2F-Ml98B58mfQJRgpbBI9p%2Ftestgif98.gif?alt=media&token=9a3dfbf8-1cd5-4c93-9f9a-9760d3dc77a2)

{% hint style="info" %}
An open modal acts as a Page does, meaning that you can drag-and-drop other components into it when it’s open.
{% endhint %}

You can change the width of the modal window and the content will automatically be adjusted:

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-Ml99EbDLSj5K1c2poMn%2F-Ml9F5anH1jauxBvSu79%2Ftestgif99.gif?alt=media&token=2f539819-1611-4594-bac1-f52356f4ce2c)

Modal windows in Jet Admin have various display styles. You can change it in the modal settings:

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-Ml99EbDLSj5K1c2poMn%2F-Ml9FWJyTF2J02NjXzLa%2Ftestgif100.gif?alt=media&token=83dddcbf-dc08-41e0-84a4-cf528939e9ce)

You can also set the title for the modal window in different ways. The title can be a **static** value or a **dynamic** value using formulas \(e.g., you want to display Update Product \# {{id}}\). 

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-Ml99EbDLSj5K1c2poMn%2F-Ml9GAwkZeRg0Rvn5ML5%2Ftestgif101.gif?alt=media&token=24f52c6c-c3ca-4b4d-9c94-c0b6ea0a8bd7)

See here for more details on how to use the formula functionality for dynamic values:

{% page-ref page="user-guide/parameters/formulas" %}

## Open a Modal from a Table

You have a table that displays a list of Products. After clicking on the product row \(the selected row\) you want to see product details - displayed in modal. To do this, let's set up a Row click action with the **Open Modal** type:

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-Ml99EbDLSj5K1c2poMn%2F-Ml9TdsgNGU7RtKLf1cJ%2Ftestgif102.gif?alt=media&token=62be4eca-12a3-427a-820d-7590cfedebcc)

Next, you can choose a created and configured modal or create a new one:

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-Ml99EbDLSj5K1c2poMn%2F-Ml9U8bhCsbqU8SQFBa0%2Ftestgif103.gif?alt=media&token=8945611c-c031-43a4-90fb-8075748367d6)

Now let's add a Detail component to the Modal window to display detailed information:

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-Ml99EbDLSj5K1c2poMn%2F-Ml9UZ89os3XY_Wr0lNn%2Ftestgif104.gif?alt=media&token=9eb4b72d-eef4-49fc-be13-4479f2655dbb)

Next, you need to apply filters, namely a data filter on the primary key \(in our case it is the product ID\). This step is important for the form to display exactly the data you selected in the table \(selected row\):

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-Ml99EbDLSj5K1c2poMn%2F-Ml9UqRLRVXiPnQD7ZCk%2Ftestgif105.gif?alt=media&token=14a55937-afaa-4cbd-9d67-6cb7e99cd420)

{% hint style="info" %}
Now, when you select a row, the modal window will open with product details.
{% endhint %}



