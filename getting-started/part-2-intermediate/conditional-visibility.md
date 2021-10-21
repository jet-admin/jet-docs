In Jet Admin, you can make certain components visible or invisible depending on the values or combination of values from your data or user attributes. 

Say, we want to show two different status change `buttons` depending on the status value of the selected row of the `users` table:

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MkfYzwIiYAzw06D690g%2F-MkgFhSXlnt5fbAjvCz0%2Fvisibility1.gif?alt=media&token=0cb6b168-edf7-4b84-9178-66f118400cdf)

{% hint style="info" %}
If standard permissions are not enough and you may want to **restrict access** on the level of **individual UI components**, use [user properties](user-guide/security-and-privacy/user-and-team-properties) in the visibility logical expression
{% endhint %}

To achieve that, let's first drop **two buttons**: one that changes the status of a user to "active" and the other that changes it to "inactive":

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MkfYzwIiYAzw06D690g%2F-MkgHjYYjBz2TurTvxpq%2Fzthxbcxgn.png?alt=media&token=955b24e7-b88c-4c51-9d00-ff763f3866e2)

Then, we proceed to the "Activate" button's settings to the **"Visible" section**:

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MkfYzwIiYAzw06D690g%2F-MkgIeg9WfYt8QbOJPlC%2Fvisibility2.gif?alt=media&token=2aa2a7f3-96f5-44ba-9972-beeebbd5266c)

Next, we type in the condition: `IF` the `status` value from the selected row equals "inactive", then return `true`, otherwise, return `false`. Returned `true` will make the component visible and `false` will make it invisible:

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MkfYzwIiYAzw06D690g%2F-MkgKklxhgu8c3b0s1JQ%2Fvisibility3.gif?alt=media&token=d6b6f1bf-c381-4b8c-a8b1-acfe965e7117)

Here's the expression: `=IF(EQ(elements.users["0"].selected_item.Status, "inactive"), 1, 0)`

Then we do the same for the "Deactivate" button, grabbing the "active" value from the selected row:

`=IF(EQ(elements.users["0"].selected_item.Status, "active"), 1, 0)`

And we get our buttons being **dynamically hidden** based on the status value from the selected row:

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MkfYzwIiYAzw06D690g%2F-MkgFhSXlnt5fbAjvCz0%2Fvisibility1.gif?alt=media&token=0cb6b168-edf7-4b84-9178-66f118400cdf)

