To send an email, you need to specify such Values as the recipient's email, subject, and body. You have different options to do it: 

1. Ask the user to fill the form in your App
2. Specify default values
3. Extract values from components

## Ask the user to fill the form in your App

We need to configure Values for the "Send Email" button in that case. So all we have to do just select `Ask from user user option` in [Formulas](user-guide/parameters/formulas) pop-up window. 

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-Mjgnl0gl1n5hbbhv0Nk%2F-MjgsMhxqeacjCzM92WQ%2Ftestgif44.gif?alt=media&token=387aa771-3a98-41d1-bae5-371857237769)

Now, when the user will send an email, the values will automatically be passed from the selected row in the table to the button values.

## Specify default values

You can set a default value for any parameter for the value to be passed automatically:

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-Mjgnl0gl1n5hbbhv0Nk%2F-Mjgt67WLU7ccycs8wZR%2Ftestgif45.gif?alt=media&token=652de562-38d7-42ff-8af3-a3d88e9c73ce)

Now when the user sends an email, he or she will not have to manually enter the `from email` parameter.

## Extract values from components on the Page

Let's say you have the Customers table. Once the user is selected in the Customers table, his or her email value will be used as the`User email` parameter so that to send a promotional email with a Marketing tool. The succession of events will be this:

1. Click on Value text area. There will be a pop-up window.
2. Then select Customers table  -&gt; Clicked row \(the value will pass once you click a row\) -&gt; User email.
3. The Value field will be populated with the following expression:

`=elements.Customers["0"].selected_item.email`

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-Mjgnl0gl1n5hbbhv0Nk%2F-MjgrBr70M7R5UoQsjpE%2Ftestgif44.gif?alt=media&token=d421dfdc-7b7d-4ad1-8265-379bbc869110)

