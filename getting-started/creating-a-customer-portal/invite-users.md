[comment]: # ($page_title=Users & Permissions)

The key functionality of any Portal is that any user or groups of users see and interact **only with their data**. In this step, we'll invite our users and set permissions to turn our Airtable app into a **secure portal**.

## Invite Users

Click `Share` and add the email of a user. Then we can invite this user to the existing team or create a New Team by clicking `Add a new Team`. In our example, we build a portal for corporate clients, so we'll create separate teams for every company we work with.

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-Mj0KWLBMzBscDrz_1iL%2F-Mj0KnRTFAMq-OCJTN80%2FQuickstart-portal14.gif?alt=media&token=d9bff09f-6729-4305-a874-189d3e5284e4)

{% hint style="info" %}
In Jet Admin, **Teams** are the groups of users with the same permissions
{% endhint %}

Then **send invites** to the users. In our case, we invite Beans Coffe employees:

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-Mj0KWLBMzBscDrz_1iL%2F-Mj0QjAT2QrV_0zsqG8p%2FQuickstart-portal16.gif?alt=media&token=3d3b5a0e-e7ca-45ce-89f4-52236e1d00a8)

## Set the Data Separation

**Team Properties** and **User Properties** are used to set the data separation in Jet Admin. For each team or user, we add a `Property` that uniquely identifies a company or a client, such as `domain` or `email`. In our case, we use the company name:

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-Mj345Zfb12TArzDKjL4%2F-Mj3Ga__P7kSp4MykGay%2FQuickstart-portal18.gif?alt=media&token=7954d048-c74b-4109-b75c-abe7948dbeb9)

{% hint style="info" %}
To be able to separate data, we need to have the property value in our data
{% endhint %}

Next, we need to **filter** our Portal's data by the property. Select the component you want to separate data for, proceed to filters, and set the `Client field` to match `Client property` we've created:

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-Mj345Zfb12TArzDKjL4%2F-Mj3SyCdaFXBYWw9BCZn%2FQuickstart-portal23.gif?alt=media&token=3e9b86a8-f8ec-4325-94a8-212d4f5f02dd)

## Set Permissions

Additionally, we want our Coffe Beans employees to interact only with the portal page we've created. For this, go to the **Teams** and set page-level permissions to allow access to the `Tasks` , `Tasks-edit` and the `Tasks-create` pages:

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-Mj345Zfb12TArzDKjL4%2F-Mj3LexdUBBsS4z0z_D7%2FQuickstart-portal19.gif?alt=media&token=847d7458-e734-4e24-826d-aa1530d3c53b)

Now, let's check how that works: the Beans Coffee employee that we've invited can see **only their company's projects**:

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-Mj345Zfb12TArzDKjL4%2F-Mj3Qy5_4OXYQ_zT7yw8%2FQuickstart-portal22.gif?alt=media&token=3929c975-c36b-4025-b3a4-0382fc779a55)

