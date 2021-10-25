[comment]: # ($page_title=Conditional Visibility)

When you build an interface you want to be available both for your customers and users who support them, you might also want to set visibility for components that should only be available to either your support team or your users. We provide a Visibility feature that can be assigned for any component.

Component Visibility rules allow you to create rules to determine whether a given component is visible \(and able to be interacted with\). For example, you can place several buttons in the same place and then create different visibility rules to determine which one appears for each User or Team in your app.

## Creating a visibility rule

When setting up any component, you will see a Display tab in the edit menu of the component on the right:

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-Mjh4zY8c8YAo0HsrJ6Q%2F-Mjh9akvTjOGz3fz9fCk%2Fimage.png?alt=media&token=ea7c9445-b358-46e8-87b7-67ec48f6e07d)

In Builder mode, you will clearly understand if the component is hidden and your conditions are working properly by the label in the upper left corner of the component: `Component is hidden`.

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MjhC0u2P0uFlRna5erg%2F-MjhCy-LJ5pEieS2Gdl9%2Fimage.png?alt=media&token=8bc57b1b-d625-43f2-bfab-fd0cfc6bb945)

{% hint style="info" %}
The Visible field can either be a dynamic value \(a value from another component or page, or a computed value\) or a default value.

Any operation in this field is converted to a boolean type, so you don't even have to return True or False values.
{% endhint %}

{% page-ref page="user-guide/parameters/formulas" %}

## Example 1: Hiding a component until a row is selected

For instance, you need to hide a component until a row is selected in a table. To do this, you need to do the following:

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MjhDfHJYZ82e88G8NBh%2F-MjhEAOAqky110eeyxtw%2Ftestgif62.gif?alt=media&token=8930a8d9-b7f6-490a-a435-86c47a6e09e8)

The value of the Visible field in this case will be as follows:

`=elements.Customers["0"].selected_item.email`

{% hint style="info" %}
The Email field will now be hidden as long as no row is selected in the table.
{% endhint %}

## Example 2: Hiding a component until a row with a certain value is selected

As an example, you need to hide a component until the value in a certain field is equal to a certain value. Let's consider the same example, will hide the Email field until a user with Active status is selected in the table. To do this, we will use the EQ\(\) function to compare the two values:

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MjhDfHJYZ82e88G8NBh%2F-MjhGfVDaWXkZgsZJMlv%2Ftestgif63.gif?alt=media&token=c3f06f0b-f9e1-4417-a0a8-b5e5900ed120)

The value of the Visible field in this case will be as follows:

`=EQ(elements.Customers["0"].selected_item.status, "active")`

{% hint style="info" %}
The Email field will be hidden until a user with Active status is selected in the table.
{% endhint %}

## Example 3: Hiding a component if the value is greater than or less than a certain value

Now let's look at an example of component visibility using basic compare operators \(such as &gt; or &lt;\). Suppose you want to hide the button if the value in the Quantity field is less than 1:

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MjhHonvn3cgqhI1Kk-O%2F-MjhO0AnzhjRuc-OE7Qc%2Ftestgif64.gif?alt=media&token=66ce9699-1d74-48d3-beda-db20e6a4998f)

The value of the Visible field in this case will be as follows:

`=elements.Quantity.value >= 1`

{% hint style="info" %}
Now the button will be hidden if the Quantity field is less than 1.
{% endhint %}

## Example 4: Hiding a component if the Page Value, User or Team Property value is equal to a certain value

Now let's look at an example of hiding a component depending on values such as Page Values, User & Team Properties and implement the condition of hiding a component if User Property has a readonly value. To do this, you first need to create a User Property, see [here](user-guide/security-and-privacy/user-and-team-properties) for details.

For this purpose, I set the User Property Access for my user with the value readonly.

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MjhOHOEZPP-Nzw64YsS%2F-MjhSWFAnXwGhTRYI9DB%2Ftestgif65.gif?alt=media&token=fc54c7fe-44e0-46c2-afe4-1e2b95fcffc4)

The value of the Visible field in this case will be as follows:

`=IF(EQ(user_properties.Access, "readonly"))`

{% hint style="info" %}
Now the button will be hidden for all users who have a read-only Access property value.
{% endhint %}

## Example 5: Hiding a component depending on several conditions

Now let's implement a more complex scenario of hiding a component depending on several conditions. Let's consider the simple variant of hiding the button until the two fields Active and Subscribed are true.

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MjhOHOEZPP-Nzw64YsS%2F-MjhVp9smflclHbI9SS4%2Ftestgif66.gif?alt=media&token=3e004c74-9b38-49c3-8105-dfe14f550867)

The value of the Visible field in this case will be as follows:

`=AND(elements.Active.value, elements.Quantity.value)`

{% hint style="info" %}
Now the button will be hidden until both values are true.
{% endhint %}

{% hint style="success" %}
Note that you can do the same for dynamic values passed from other components, as in the examples above.
{% endhint %}

