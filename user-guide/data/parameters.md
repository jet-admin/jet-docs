Using parameters you can pass values such as subject and body to `Send email`, filter a list, or pass data from one page to another. You can specify parameters for each [page](getting-started/quickstart/creating-your-first-tool) or [component](user-guide/components). Here we guide you through parameter types and how to specify parameters for page or component.

# Component parameters

To send an email, you need to specify such parameters as the recipient's email, subject, and the body. You have different options to do it: 

1. Ask the user to fill the form in your App
2. Specify default values
3. Extract values from components on the Page

## Ask the user to fill the form in your App

We need to configure the parameters for the "Send Email" button in that case. So all we have to do just select `Ask from user user option` in [Formulas](user-guide/data/formulas) pop-up window. 

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MOVtBrdDzZLhoXtOvek%2F-MOWGuE0T67Sd4PR5Il8%2FGIF179.gif?alt=media&token=5f24d92d-a33c-4e18-a2cc-f03e6d143a54)

Now when the user will send an email, a popup window will be displayed with a form for entering the required parameters.

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MOVtBrdDzZLhoXtOvek%2F-MOWHlL-Mt5UgMOh-eMM%2FGIF180.gif?alt=media&token=c6a85e13-66df-4f41-bb53-c774b3f12a6f)

## Specify default values

You can set a default value for any parameter for the value to be passed automatically:

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MOVtBrdDzZLhoXtOvek%2F-MOWIdJ-swRmBsczJAQu%2FGIF181.gif?alt=media&token=5a758325-c953-44c2-bf45-4a64e7670ad2)

Now when the user sends an email, he or she will not have to manually enter the `from email` parameter:

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MOVtBrdDzZLhoXtOvek%2F-MOWKgFZ9pyYjGVsxbes%2FGIF182.gif?alt=media&token=73d83442-4816-4c9b-8c1a-f5636407e0c6)

## Extract values from components on the Page

Let's say you have the Customers table. Once the user is selected in the Customers table, his or her email value will be used as the`User email` parameter so that to send a promotional email with a Marketing tool. The succession of events will be this:

1. Click on Value text area. There will be a pop-up window.
2. Then select Customers table  -&gt; Clicked row \(the value will pass once you click a row\) -&gt; User email.
3. The Value field will be populated with the following expression:

`=elements.Customers["0"].selected_item.email`

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MOWNN6upWOlCADhHKVm%2F-MOWQfwgCvO3N9tSHByw%2FGIF183.gif?alt=media&token=f8e491ce-44b7-4318-9583-4adf5871be0e)

# Page parameters

In case, when you want to build a Detail page for your user with the user info on this page: first name, last name, address, etc. You need to pass the user ID parameter from one page to another. To do this you need to create a parameter for this page and pass this parameter to another page in [Action](user-guide/data/actions). 

## Create page parameters

To create page parameters go to the page settings then click **+Add Parameter.**

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MGPCEPBeDjCCSLh-bxy%2F-MGPNyJnqNqNkmnmLLRg%2FGIF40.gif?alt=media&token=84168c78-5f2f-450c-bb7b-1dfbdc1cc620)

## Link pages

Let's say the **Refund Tool** page includes a customer table, and the other **Users** page includes a table with detailed information about the customer. We want to pass the `customer id` from one page to another to get the additional info. 

1. To create a link between pages create an **Action** specified as **Open Page**

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MGPCEPBeDjCCSLh-bxy%2F-MGPWm9bo-nb-bcRAbms%2FGIF41.gif?alt=media&token=1463af4d-bc99-4561-8686-e31f08bfdab2)

2. Select the page you want to open \(**users** page in our case\).

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MGPCEPBeDjCCSLh-bxy%2F-MGPX3kPeS62_Px26otu%2FGIF42.gif?alt=media&token=d6e13f52-342b-4072-b4b3-2d26e127e64c)

3. Pass the `customer id` parameter from the customer table.

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MGPCEPBeDjCCSLh-bxy%2F-MGPYMRsTNzXX_tD2qV6%2FGIF43.gif?alt=media&token=48ec1f9b-7ea0-47fb-b0ca-522ae2d21d7f)

4. Select a user and click on the Get Info button.

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MGPCEPBeDjCCSLh-bxy%2F-MGPYwWrRZh8ExXt8jYJ%2FGIF44.gif?alt=media&token=4f850109-82bc-4b63-bd92-7e3c21c6cb94)





