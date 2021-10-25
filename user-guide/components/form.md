[comment]: # ($page_title=Form)

Submit a **Form** to perform actions with input data. The Form component provides a way for users to view and manipulate multiple data fields with their inputs. Upon submission, forms perform functions like creating \(inserting\) a new data record, updating an existing record, or [calling APIs](user-guide/data/make-an-http-request).

Use a form if you expect the user to interact with multiple data fields for the form's function. If you need a user to enter in an email and customer name, select an item from a dropdown, and then write a paragraph of text, forms are your best option. This is usually the best component when your function is to create entirely new data records.

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-Ml622jlw_Du2qN4JOkc%2F-Ml8hE3IE2OmvZZLsfEO%2Fimage.png?alt=media&token=dc4cfcca-9e1e-414f-b83c-58e11cc8369b)

{% hint style="success" %}
You’re looking to build a tool to allow your business to take new orders over the phone. The tool will need to record the **customer name**, **phone number**, **address**, **product SKU**, and **payment information**, and store it in your **Orders** table in your database.

Because there are multiple fields with user input, you choose to use a **Form**. For fields like the **name** and **address**, you allow the user to type in the text. For the **Product SKU** and **Payment** **Type**, you set up a dropdown selector \("Visa", "Mastercard", etc\). When submitted, the form inserts a new Orders record with this data into your database.
{% endhint %}

## Create Form

To add a Form, simply drag-and-drop the Form component to the page and then choose the resource and collection for which you want to generate the form:

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-Ml622jlw_Du2qN4JOkc%2F-Ml8jek2PsRDlWyazONk%2Ftestgif84.gif?alt=media&token=a2ca1ed2-f269-4a6a-afe2-53551eb30bb2)

{% hint style="info" %}
Now, when you fill out the form, you will be able to create a new record in your database.
{% endhint %}

## Customize the Form view

You can customize the form's appearance, such as arranging fields horizontally in multiple columns. To do this, simply drag-and-drop any field to the right of another field:

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-Ml622jlw_Du2qN4JOkc%2F-Ml8lc2-pkzwawMWqrfX%2Ftestgif85.gif?alt=media&token=87b18e41-3c0b-4bd7-b563-2ddcb656e899)

## Example 1: Verify inputs before submission

Sometimes you may have a process where a user needs to fill out the data fields correctly, prevalidating them \(e.g., correctly typed **phone number** or **email**\). To do this, you can set the Validator to the desired data field:

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-Ml622jlw_Du2qN4JOkc%2F-Ml8o29Mate_rYJUkhi5%2Ftestgif86.gif?alt=media&token=e06e2ff2-36b5-4ce2-b833-50dfcc34b1a0)

Now unless the user has entered the correct Email it will not be possible to submit the Form:

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-Ml622jlw_Du2qN4JOkc%2F-Ml8p13NXvWks3u-wUlC%2Ftestgif87.gif?alt=media&token=3fd48236-736d-4737-acc8-a026882ce8cf)

## Example 2: Verify the required fields are filled in

Sometimes you need to make some fields required so the user can't submit a form without specific details. To do this, check the Required option for the desired data field:

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-Ml622jlw_Du2qN4JOkc%2F-Ml8qO223DoJuM3-RjXi%2Ftestgif88.gif?alt=media&token=639dcfb5-8955-4df5-95f9-1425e71b3fc8)

{% hint style="info" %}
Now unless the user has entered the **phone number** it will not be possible to submit the Form.
{% endhint %}

## Example 3: Add a placeholder for the fields

Sometimes you need to add a specific placeholder for a field to hint to the user. To do that, just set a Placeholder for the desired data field:

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-Ml622jlw_Du2qN4JOkc%2F-Ml8s1L3igpWfHSqF0Sa%2Ftestgif89.gif?alt=media&token=f2ffdace-faac-4070-8420-b4e002f35bc8)

## Example 4: Make some fields hidden

Sometimes you need to configure Visibility rules for form fields so that the user can see new fields if the previous ones are filled. To do this, just configure Visibility for the desired data field. 

Let's make the **Email** field appear only if the **Customer name** field is filled in:

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-Ml622jlw_Du2qN4JOkc%2F-Ml8t_gchaUUzaf1uneM%2Ftestgif90.gif?alt=media&token=a56ceed6-f308-419f-97e2-234b42d4bb13)

Now, unless the Customer name field is filled in, the user will not be able to fill in the Email field:

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-Ml622jlw_Du2qN4JOkc%2F-Ml8uDXxPDfFn6cuOBKx%2Ftestgif91.gif?alt=media&token=e67addef-8530-4549-a53f-432e9ba3060e)

See here for more details on Conditional Visibility:

{% page-ref page="user-guide/components-visibility/conditional-visibility" %}

## Example 5: Update the data of the selected row

Let’s say you have a table of Products for your business. Before sending these Products over to be processed, you want a user to review and sanity-check the data in the Product, like the Quantity and Price.

You can create a form that displays the Product data, prefilling each field \(like Quantity\) with the current value in an editable text box. Users can quickly scan the form to review and hit a "Confirm" button to confirm the product or fix any errors they notice before confirming.

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-Ml622jlw_Du2qN4JOkc%2F-Ml8x_--_SkK8TBqpLzW%2Ftestgif92.gif?alt=media&token=2e1e1e16-37cc-4282-ad03-3f2dff503e8f)

We’ll cover a step-by-step example of binding to pre-existing values below.

To bind data from a table to a form, you need to generate a form first with the same resource and collection \(Airtable - Products\) by selecting the operation type \(in our case it is Update operation\):

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-Ml622jlw_Du2qN4JOkc%2F-Ml8xydVX85Yq7N4mQxK%2Ftestgif93.gif?alt=media&token=48c846d4-5061-4a34-8116-b09b54ef0fe8)

Now you need to configure the "Fill form with data" section. To do this, simply click on the Connect Data Source button and Jet Admin will automatically select the desired resource and collection \(the same one used in the form\):

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-Ml622jlw_Du2qN4JOkc%2F-Ml8y_cfkJPPIWAVRWva%2Ftestgif94.gif?alt=media&token=c87603da-a909-48cf-b670-78d6c89b6437)

Next, you need to apply filters, namely a data filter on the primary key \(in our case it is the product ID\). This step is important for the form to display exactly the data you selected in the table \(selected row\):

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-Ml622jlw_Du2qN4JOkc%2F-Ml8z7cMxW2NlqdrBVHR%2Ftestgif95.gif?alt=media&token=179d0f25-27a2-4542-816f-c46a7e92967f)

Now we just need to generate the form and we're done:

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-Ml622jlw_Du2qN4JOkc%2F-Ml8zpgLTC8SGiky8KcU%2Ftestgif96.gif?alt=media&token=303652c0-2505-4ed4-a1b0-de1e208c5d06)

