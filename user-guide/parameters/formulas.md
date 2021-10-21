A formula is a method to access every piece of data and build up to as complicated a data flow pattern as you need it to be. You can combine, modify or calculate the values, or you can even pull up an access control system based on logical conditions set by an appropriate formula.

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MjgtXzTjBj2m2d5c1pE%2F-MjgtmmSDLovPSqFwO8M%2Ftestgif46.gif?alt=media&token=f3b512ee-0c52-40a8-afa0-dbfbf85a7973)

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

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MjgtXzTjBj2m2d5c1pE%2F-Mjgu6OsT4DKoxsolCIh%2Ftestgif47.gif?alt=media&token=f9b76209-9c69-47e5-a572-9b17fa816b7c)

2. Now we will configure the Subject field using the `CONCAT` function. Let's say we want to select an appropriate value from the Discount dropdown list and have it automatically passed to the Subject field of the promotional email in the following form: "Manuel Allen - 15% discount":

`=CONCAT(elements.Customers["0"].selected_item.username, " - ", elements["Discount"].value)`

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MjgtXzTjBj2m2d5c1pE%2F-MjguYvdfmfJFRdUDxcD%2Ftestgif48.gif?alt=media&token=b4de0c27-0b88-4f66-a105-55778e397b3f)

3. To finish up, we shall configure the Body field. Using the `CONCAT` function we will build a template for the email body:

`=CONCAT("Hi ", elements.Customers["0"].selected_item.first_name, ", here is your promocode: ACX978DF.")`

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MjgtXzTjBj2m2d5c1pE%2F-MjgvY7J_pNfm1rPOoYT%2Ftestgif50.gif?alt=media&token=988e3503-f78b-4f92-addd-0ff7feddcec8)

4. Now when you select any customer, it will launch a completely automated process to create a promotional email to treat this customer. The only manual job remaining for you will be to select the discount and hit the Send email button:

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MjgtXzTjBj2m2d5c1pE%2F-Mjgvr4ocohZXiYUe6QS%2Ftestgif51.gif?alt=media&token=99c2d7e4-94aa-4ad5-989a-0e52e8195ac9)

## Create Custom fields using Formulas

In this use case we will create a custom column in the Customer table and calculate a score depends on some logical condition.

1. Simply create a new Custom field in columns settings of table component. 

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MjgtXzTjBj2m2d5c1pE%2F-MjgwCxBeR0Ov1R9UE3A%2Ftestgif52.gif?alt=media&token=68d89b06-0ffa-4c89-b42e-bc8746e7de5c)

2. Now we should configure Value for that Column using Formulas. We will use `IF` function to calculate Scores value, depending on Activities number for each customer:

`=IF(item.activities < 280, '50 points', IF(item.activities < 400, '70 points', '100 points'))`

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MjgtXzTjBj2m2d5c1pE%2F-MjgwPkqpSH2mSxdAJHn%2Ftestgif53.gif?alt=media&token=e3655496-2c2d-4ed7-a04f-31be790fb1c7)

## Formulas variables

Essentially, this is a tabbed pop-up window which reflects all the components on the current page, a list of functions and a set of filters to manage data in the selected table. 

The number and type of tabs depends on the context. This allows the user to have access to only those tools which are applicable to the objects he or she is working with. For example, if we work with table parameters, there will be a tab with filters. In case we drill down to a specific record of a table and have this record fields displayed on a page, a tab with Record components will be available:

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MjgtXzTjBj2m2d5c1pE%2F-MjgtmmSDLovPSqFwO8M%2Ftestgif46.gif?alt=media&token=f3b512ee-0c52-40a8-afa0-dbfbf85a7973)

## Tabs context

When you configure the table parameters, the features displayed in the Formulas window will fit the component context, e.g. there will be a new tab with `Filters` to set up filtering for selected table or a tab with [User properties](user-guide/security-and-privacy/user-and-team-properties) if any exists. Let's walk through the possible context Tabs.

### Search tab

In this tab you see a general list of all available interactions with the current component or other components and parameters. 

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MjgtXzTjBj2m2d5c1pE%2F-MjgxaHqMz6oXPJJA-jA%2Ftestgif54.gif?alt=media&token=94b7533e-6745-4742-8cf0-47a2dd2c5cb1)

### Current component tab

When you are working on a Current Component setting, the context in the formulas will show you the Current Component setting at the very top. In this tab, you can only access the fields in the current component:

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MjgtXzTjBj2m2d5c1pE%2F-MjgyFpcqgd2TH-cGFzW%2Ftestgif55.gif?alt=media&token=33a4eedc-52ae-4ef9-a375-36e35a678b02)

### Components tab

Here you can access any data from your resources through any component \(fields, tables, charts, etc.\) on the current page.

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MjgtXzTjBj2m2d5c1pE%2F-MjgydhbtHhS-CPY5uUx%2Ftestgif56.gif?alt=media&token=d647c0bd-bf58-4777-ad64-90e6189876ca)

## User-specific properties

If you want to restrict access for a User or a Team to data that is relevant for their work within a JetAdmin app, you can quickly access the [User & Team properties](user-guide/security-and-privacy/user-and-team-properties) in these tabs and assign the user or team ID to the data columns which should be visible for them: 

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MjgtXzTjBj2m2d5c1pE%2F-MjgzSGRnx9RSPLK0N4w%2Ftestgif57.gif?alt=media&token=1289a96b-0a60-49d9-b0f2-cfd2070fe612)

