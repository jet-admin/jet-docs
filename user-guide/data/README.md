{% embed url="https://youtu.be/adS8L7XoQ0E" %}

`Data` helps you to pull data from different [Resources](user-guide/integrations) and display it on [Components](user-guide/components). You can do different operations with your `Data`:

* Pull data from different Resources \(Database, Stripe, Zendesk, etc.\)
* Specify any parameters to filter your data or pass parameters to make a request
* Define relations between collections with different resources

You handle the Data when you add a resource to your component. Collections are visualizations of the data that Jet gets from your resources.

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MGPn-eauD5UWR4bkf9b%2F-MGPoPo5VlBe47G6ue5j%2FGIF53.gif?alt=media&token=7fc74b12-2056-4c4c-bd3f-28b462cd044e)

## Collection

Сollection like a spreadsheet is a list of records with rows and columns. You can display Collection in one of the Lists components: Table, Kanban, Gallery, Map, Calendar, or Timeline.

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MGPn-eauD5UWR4bkf9b%2F-MGPpFHzExUYWoYJeaO-%2FGIF54.gif?alt=media&token=e709b115-de31-4635-a706-efcecfe793e3)

{% page-ref page="user-guide/data/collection" %}

## Records

Record is a single data item in your collection. For example, if your collection is called Customers, it is likely to be customer's data: `first name`, `last name`, `address`, etc. Simply click on the record and the Record page will open.

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MGPn-eauD5UWR4bkf9b%2F-MGPs5T5pg2fI_T3uqEg%2FGIF55.gif?alt=media&token=9cd4d47f-91d7-4eef-b01f-26fc30078a7a)

{% page-ref page="user-guide/data/records" %}

## Fields

The field is a single piece of your data \(such as `first name`, `last name`, `address`, etc.\) that is displayed in the collection record based on your resources. 

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MGPn-eauD5UWR4bkf9b%2F-MGPsV7QUdnO5NdS5iD7%2FGIF56.gif?alt=media&token=794e721e-066b-431b-b439-495f2ba73fb6)

{% page-ref page="user-guide/data/fields" %}

## Actions

Action is what you can perform \(API request, write and read data in the database\) in Jet Admin and it will return the answer to your request. Visually, the action is a button in the Jet's interface.

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MEJZ7GEDKD1k6OFhrr7%2F-MEJeBhO6IdpsOZvvTMn%2Fimage.png?alt=media&token=29e736c9-a14c-4f03-bbb5-64cc9b85e3cc)

{% page-ref page="user-guide/data/actions" %}

## Relations

You can also define Relations between Collections from different Resources. For example, you can link your Transactions from Stripe with Users from the database.

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MGPn-eauD5UWR4bkf9b%2F-MGPtQCpOoq_qNDWXvdU%2FGIF57.gif?alt=media&token=27adcf5e-84f2-4a25-b9f7-8aa705d9d1fe)

{% page-ref page="user-guide/data/relations" %}

## Parameters

Specify parameters such as subject, body to send an email, filter a list by specific fields, or pass data from one page to another. 

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MGPn-eauD5UWR4bkf9b%2F-MGPu5XeubEnC2ggzmIG%2FGIF58.gif?alt=media&token=42b7c8a3-b0e5-46cb-91f5-c45c17611667)

{% page-ref page="user-guide/data/parameters" %}

