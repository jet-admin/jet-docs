In Jet any action that's executed comes with the notification pop-up window, displaying different messages depending on the outcome. The typical success message looks like this:

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MW3aQQNlsHQtUBwgj3e%2F-MW4CDYqY2pt_w1O9ZSz%2Fimage.png?alt=media&token=59bd0fdb-3505-4852-9685-039c934cb8f1)

Now you can set your own custom messaging so that our example message might be something like that:

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MW3aQQNlsHQtUBwgj3e%2F-MW4E-L8tV1AOUChiBXy%2Fimage.png?alt=media&token=ae22b81b-8aab-46ac-8b97-a2498d53a2cd)

## Notification types

We provide 4 types of notifications: **success**, **info**, **warning,** and **error**. You can set up any of these depending on your workflow. Let's look at the two most common use cases with Success and Error notifications.

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MW4qJ0uZZFiLyu5cj3J%2F-MW4q_Xh1KRq26Qg3VWv%2Fimage.png?alt=media&token=ad127128-5772-4172-baf4-bdf0f2aaccd4)

## Set up Success notification

Let's look at the workflow of changing a customer's status, for which you have already configured a primary [action ](user-guide/design-and-structure/actions)to change the status field in your data source. Now you have to set another action that'll be executed after completing the primary action \(status change\). The succession of events will be this:

1. Go to **After Completion** section
2. Navigate to **When action succeeded** and click **Success action**
3. Select from the dropdown **Show notification** and specify: **title**, **description**, **Success type**

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MW4HmpfcwY-WBYomnWd%2F-MW4oszxjs-Cw4qu9CkG%2FGIF205.gif?alt=media&token=797db8b3-a1fc-4377-843c-d46e359961bd)

Now, whenever the Update button is clicked, users will see the new custom "Status Updated" notification.

## Set up Error notification

Let's consider a case where there's an error after executing an action. Error notifications in Jet usually show up with "404 or 500 status", which might be confusing to the non-tech support team. To customize our **Error notification**, we will follow the same logic as in the previous case:

1. Go to **After Completion** section
2. Navigate to **When action failed** and click **Error action**
3. Select from the dropdown **Show notification** and specify: **title**, **description**, **Success type**

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MW4qJ0uZZFiLyu5cj3J%2F-MW521n6VwBcgy_JH3dZ%2FGIF206.gif?alt=media&token=f57b9162-ac73-40ce-a1e2-bb9372a78c9f)

Now, whenever there is an error in the process of executing the action, users will see the new custom "Error occured" notification.

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MW4qJ0uZZFiLyu5cj3J%2F-MW52poy-tm-c11b6yQV%2Fimage.png?alt=media&token=02ee24cf-0faf-4210-827b-743799f9cb73)

