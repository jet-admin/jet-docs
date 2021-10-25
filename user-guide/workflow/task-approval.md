[comment]: # ($page_title=Approval Workflow)
[comment]: # ($page_description=Creating and managing task workflows within Jet Admin)

As the company is growing and the roles are diversifying, the need for some sort of a task management system for your internally-facing applications is increasing. So we came up with the "Task Queue" feature.

{% embed url="https://www.youtube.com/watch?v=-DMkubFxhDs&ab\_channel=JetAdmin" %}

## How it works

There are certain actions that you wouldn't want your support team to have the full authority over as the price for the error is really high. In that case, you can create an _approval workflow_.  Such a workflow would help:

* route approval requests to the approver
* provide the approver with information pertinent to the case
* make it a rule that certain actions can only be performed if approved
* optionally, enable communication within the approval process 

Here's the setting: your customer wants his money back. You scroll through the customer list, find the one to return the money to and select the transaction to be refunded. Now you press the Refund button to make it happen, but here's an approval workflow baked in to this process. Therefore, instead of just sending the charged amount back to the customer's account, pressing of the Refund button creates a task yet to be approved. You will be presented with a message informing you of the fact, and once you give your consent to the approval requirement, there's a task in the approval tasks queue.

## Create a new task queue

To start off, we need to create a new task queue. To do this, go to the settings of the Button component, select the Actions tab and activate Approval feature for this button:

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-Mjh15jd2ixodHPddB36%2F-Mjh2PazwHwzVXwYwVum%2Ftestgif60.gif?alt=media&token=721c7da3-f2c6-4f20-aafd-fb8f9f8b4879)

Enter the name of the task and set statuses that will represent the stages and outcomes of the workflow: the most common statuses would be "new", "in progress" and "completed". 

## Configure the task queue parameters

You can pass helpful information to the task from the application so that the approver could make a better decision of either approving or rejecting a task.

Technically, every meaningful bit of information can be presented to the approver through a corresponding parameter, such a `transaction id` or a `customer id`:

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-Mjh15jd2ixodHPddB36%2F-Mjh2lJMVq3y4EMAHPj4%2Fimage.png?alt=media&token=80599065-f37b-42a5-8980-9fc2e320382a)

A task queue being formed, you can perform that action from a Jet Admin application to the approval queue to require the approval from the team leader or whoever you set as the assignee of the task.

## Create an approval task

First, select the task queue that we've created in the previous steps. For the "**Task Name**" you can either type a name or use formulas to use the dynamic values from the page. "**Initial status**" sets the status that the assignee will see in the task queue list and in the task queue details. "**Status after approve**" and "**Status after reject**" are the statuses that the task will change to after approval and rejection correspondingly. And the initial assignee is the person who should receive this task in their task queue and decide whether to approve or reject the task:

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-Mjh15jd2ixodHPddB36%2F-Mjh3ht9fBTOy0qcWPZW%2Ftestgif61.gif?alt=media&token=8bd210cb-e31e-412e-b63e-8c9dc71a06e2)

## Pass parameters

The next thing to do is to pass parameters that the assignee will see in the task details before making the decision. Those might be the amount of the transaction to refund, the account status or any other value from the page or a formula. You can add as many parameters as you need.

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-Mjh15jd2ixodHPddB36%2F-Mjh46JHrLZuRF9KhGzI%2Fimage.png?alt=media&token=3c756c64-222e-4e4b-99e6-8049ffed513b)

{% page-ref page="user-guide/parameters" %}

## Approving and rejecting the tasks

Now, every time a user clicks on the "Refund" button, a task would be created and passed over to the task queue feed of the chosen assignee. To see the list of tasks you need to open the collaboration page:

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MO5c8r8iHD0iy25YmfD%2F-MO5fTqxXSpk87kxahBQ%2F%D0%91%D0%B5%D0%B7%D1%8B%D0%BC%D1%8F%D0%BD%D0%BD%D1%8B%D0%B9.png?alt=media&token=c06a8397-01d8-4d34-b912-3f69abe2f196)

## Organizing the tasks

You can filter tasks by the assignee and the date as well as by the priority. "Priority" is the attribute of the task set by the assignee to help determine how important the given task is.

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MO5c8r8iHD0iy25YmfD%2F-MO5g4p9axBF4_VvC2av%2FGIF157.gif?alt=media&token=e73ab5f7-1674-42a1-988e-3bf8ccdb254d)

## Managing the tasks

After organizing the tasks the assignee can click on the task and view and change the details of the task. The parameters sent along with the task for the given action will appear in the "Details" section:

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MO5c8r8iHD0iy25YmfD%2F-MO5h4bfA6f-jK0RUktn%2FGIF159.gif?alt=media&token=0fc19f6c-caf9-4dae-b2f7-1cfb9344a103)

## Approving and rejecting tasks

The final step of the workflow is either approving or rejecting the task. Hitting "Approve" will deploy the action that the task has been created for \(in our case the refund\) and change the task status. Pressing "Reject" will just change the status of the task. 

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MO5c8r8iHD0iy25YmfD%2F-MO5gk6yPpmI3QSMnfqB%2FGIF158.gif?alt=media&token=f4799030-f6e5-4c83-937b-1bdcfebe6140)



