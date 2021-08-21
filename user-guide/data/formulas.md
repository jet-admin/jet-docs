{% embed url="http://youtube.com/watch?v=r0yL\_CQh9J8" %}

Your business data in Jet Admin apps are surfaced with components. Depending on the granularity level, a [component ](user-guide/components)can range from a table to a field in a table.

A formula is a method to access every piece of data and build up to as complicated a data flow pattern as you need it to be. You can combine, modify or calculate the values, or you can even pull up an access control system based on logical conditions set by an appropriate formula.

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MODDA8j1TWiZsvRrB8E%2F-MODDbPNeSKLsJPWNVRa%2FGIF166.gif?alt=media&token=f52ee8a8-9c22-45e3-9bbf-731c3267f0b6)

In a formula, you can reference columns by name. For example, if you wanted a formula that calculated the total based on the price and quantity, the formula would look like:

```text
= Price * Quantity
```

or you would like to concatenate first name and last name fields from your Table, it looks like:

```text
=CONCAT(first_name, last_name)
```

Let's see how you can make use of Jet Admin formulas.

## Setting up promotional email

For an introductory example, we will consider feeding customers email addresses to promotional email. Once the user is selected in the Customers table, his or her email should appear in the `Email` field so that to send a promotional Email with a Marketing tool. We will use Functions as well to create a Promotional Email template. For this purpose, we should be performing the following tasks:

1. Click on Value text area. There will be a pop-up window. Then select Customers table  -&gt; Clicked row \(the value will pass once you click a row\) -&gt; User email. The Value field will be populated with the following expression:

`=elements.Customers["0"].selected_item.email`

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MODDemdXxFZwSXptBAJ%2F-MODIbeUVxQGBN-ltIjv%2FGIF167.gif?alt=media&token=0bc88ffd-b525-4b0a-a58b-cf4fc3d4b273)

2. Now we will configure the Subject field using the `CONCAT` function. Let's say we want to select an appropriate value from the Discount dropdown list and have it automatically passed to the Subject field of the promotional email in the following form: "Manuel Allen - 15% discount":

`=CONCAT(elements.Customers["0"].selected_item.username, " - ", elements["Discount"].value)`

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MODDemdXxFZwSXptBAJ%2F-MODK7y0YDeMnFpSrkzr%2FGIF168.gif?alt=media&token=5de74b90-82c8-4dfe-9021-7ee2309e75ca)

3. To finish up, we shall configure the Body field. Using the `CONCAT` function we will build a template for the email body:

`=CONCAT("Hi ", elements.Customers["0"].selected_item.first_name, ", here is your promocode: ACX978DF.")`

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MODDemdXxFZwSXptBAJ%2F-MODMGbczh1QjuUrCIe1%2FGIF169.gif?alt=media&token=2dbf6332-aba4-471b-baf7-202ef5795c88)

4. Now when you select any customer, it will launch a completely automated process to create a promotional email to treat this customer. The only manual job remaining for you will be to select the discount and hit the Send email button:

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MODDemdXxFZwSXptBAJ%2F-MODNhRBNGsF0gYv2S1Q%2FGIF170.gif?alt=media&token=2c7d860d-41c0-4cdd-965f-51e95efe00e1)

## Create Custom fields using Formulas

In this use case we will create a custom column in the Customer table and calculate a score depends on some logical condition.

1. Simply create a new Custom field in columns settings of table component. 

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MODNlhlFupu4_HbwhSA%2F-MODPoIp9aQmn450_Xrl%2FGIF171.gif?alt=media&token=6adcce6a-13cd-4fd9-835b-b19380ab6dae)

2. Now we should configure Value for that Column using Formulas. We will use `IF` function to calculate Scores value, depending on Activities number for each customer:

`=IF(item.activities < 280, '50 points', IF(item.activities < 400, '70 points', '100 points'))`

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MODNlhlFupu4_HbwhSA%2F-MODVQhe_9CDCC2-UFwo%2FGIF172.gif?alt=media&token=4ffa2953-7591-48f3-9dcf-f7fbd156a5cf)

## Formulas variables

Essentially, this is a tabbed pop-up window which reflects all the components on the current page, a list of functions and a set of filters to manage data in the selected table. 

The number and type of tabs depends on the context. This allows the user to have access to only those tools which are applicable to the objects he or she is working with. For example, if we work with table parameters, there will be a tab with filters. In case we drill down to a specific record of a table and have this record fields displayed on a page, a tab with Record components will be available:

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MODDA8j1TWiZsvRrB8E%2F-MODDbPNeSKLsJPWNVRa%2FGIF166.gif?alt=media&token=f52ee8a8-9c22-45e3-9bbf-731c3267f0b6)

## Tabs context

When you configure the table parameters, the features displayed in the Formulas window will fit the component context, e.g. there will be a new tab with `Filters` to set up filtering for selected table or a tab with [User properties](user-guide/collaboration/user-and-team-properties) if any exists. Let's walk through the possible context Tabs.

### Search tab

In this tab you see a general list of all available interactions with the current component or other components and parameters. 

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MOFacj7paUZICmfE7hc%2F-MOFw9R3qCCdUG9pRAix%2FGIF174.gif?alt=media&token=a3a71665-d112-419c-8996-85217de2c998)

### Current component tab

Here you can only access a field in selected component. You can see how it works [there](user-guide/data/formulas#create-custom-fields-using-formulas).

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MOFacj7paUZICmfE7hc%2F-MOFyoXmN8N24paH4UNI%2FGIF175.gif?alt=media&token=af89cca2-eb49-44d5-b6a1-4c49e694d679)

### Components tab

Here you can access any data from your resources through any component \(fields, tables, charts, etc.\) on the current page.

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MOG3Nw5Pu_ENYhhOQ40%2F-MOG9V54_BzdURCN18In%2FGIF176.gif?alt=media&token=0b02c641-cbf3-499b-8d76-b6194c88e9c7)

### Filters tab

Let's say you have to filter customers by their status in the Customers table. To this end, you can use the Filters tab as follows:

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MOFacj7paUZICmfE7hc%2F-MOFuvjsGtdxcr3MslTV%2FGIF173.gif?alt=media&token=26c2a7db-c337-41c5-97e3-a4d6345117b4)

### Record page tab

When we are drilling down to a specific record of a table and have this record fields displayed on a page, a tab with Record components will be available. This Tab will include only fields from the resource for the table we are currently working with, which makes it very easy to access these fields.

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MOVKue2NhdPe-OHbRYz%2F-MOVQ0TGLRfoaosXlcgH%2FGIF177.gif?alt=media&token=0ff28306-f9e2-4ee8-a51f-b4ebe00f36f8)

### User & Team properties tab

If you want to restrict access for a User or a Team to data which is relevant for their work within a JetAdmin app, you can quickly access the [User & Team properties](user-guide/collaboration/user-and-team-properties) in these tabs and assign the user or team ID to the data columns which should be visible for them: 

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MOVaW2CUsjSHqCt1ZkP%2F-MOVmOM4_j_biunzLVY6%2FGIF178.gif?alt=media&token=00e6c963-ceff-4824-9633-fd3cba548044)

