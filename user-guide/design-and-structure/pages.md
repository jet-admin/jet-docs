A Page is an interface element that can span across various use cases. Create pages from scratch, or else you can apply ready-to-use [templates](user-guide/design-and-structure/templates) to get a new page in less than 2 minutes.

In this section we cover the following basic page management tasks in Jet:

* [Creating](user-guide/design-and-structure/pages#create-a-page-from-scratch)
* [Customizing](user-guide/design-and-structure/pages#customize-your-page)
* [Linking](user-guide/design-and-structure/pages#link-pages)

## Create a page from scratch

To create a new page, click on Menu on the top left corner and press icon **+ New Page - Create a blank page.** If you are in **Customer mode**, firstly go to [Visual Builder](user-guide/design-and-structure) by clicking on the icon in the bottom left corner.

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MGOeWw0O7fGSAmu4B2D%2F-MGOkyfHACOuP6s5mGXh%2FGIF34.gif?alt=media&token=d1763d7d-f8e1-4547-80fe-4e35e9e3607f)

## Build a page using Templates

The fastest way to build a page is to use predefined templates. Below is how to apply page templates:

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MGOeWw0O7fGSAmu4B2D%2F-MGOjX-HY65Shq6izIvO%2FGIF31.gif?alt=media&token=da0aa9d3-076e-4915-8c03-6dd03ecfa27a)

{% page-ref page="user-guide/design-and-structure/templates" %}

## Customize your page

Once you created a new page, drag-and-drop any components to the page to succeed with your use cases.

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MGOeWw0O7fGSAmu4B2D%2F-MGOrOjHk002kZBVAL0D%2FGIF37.gif?alt=media&token=94433d39-9eb0-4562-81ca-6dbc88ceadeb)

{% page-ref page="user-guide/components" %}

## Page parameters

The parameters allow you to pass data from one page to another. 

{% page-ref page="user-guide/data/parameters" %}

In case, when you want to build a Detail page for your user with the user info on this page: first name, last name, address, etc. You need to pass the user ID parameter from one page to another. To do this you need to create a parameter for this page and pass this parameter to another page in [Action](user-guide/data/actions). 

## Create page parameters

To create page parameters go to the page settings then click **+Add Parameter.**

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MGPCEPBeDjCCSLh-bxy%2F-MGPNyJnqNqNkmnmLLRg%2FGIF40.gif?alt=media&token=84168c78-5f2f-450c-bb7b-1dfbdc1cc620)

## Link pages

Let's say the **Refund Tool** page includes a customer table, and the other **Users** page includes a table with detailed information about the customer. We want to pass the `customer id` from one page to another to get the additional info. 

1. To create a link between pages create an **Action** specified as **Open Page**

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MGPCEPBeDjCCSLh-bxy%2F-MGPWm9bo-nb-bcRAbms%2FGIF41.gif?alt=media&token=1463af4d-bc99-4561-8686-e31f08bfdab2)

2. Select the page you want to open. **Users** page in our case. 

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MGPCEPBeDjCCSLh-bxy%2F-MGPX3kPeS62_Px26otu%2FGIF42.gif?alt=media&token=d6e13f52-342b-4072-b4b3-2d26e127e64c)

3. Pass the `customer id` parameter from the customer table.

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MGPCEPBeDjCCSLh-bxy%2F-MGPYMRsTNzXX_tD2qV6%2FGIF43.gif?alt=media&token=48ec1f9b-7ea0-47fb-b0ca-522ae2d21d7f)

4. Select a user and click on the Get Info button.

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MGPCEPBeDjCCSLh-bxy%2F-MGPYwWrRZh8ExXt8jYJ%2FGIF44.gif?alt=media&token=4f850109-82bc-4b63-bd92-7e3c21c6cb94)

