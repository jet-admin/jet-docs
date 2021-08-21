Environments allow you to have multiple configurations of your project within Jet Admin. If you want to update the resource, add a new one, change the settings or alter the UI, you can do it safely in a separate environment, whether it's _staging_ or _dev_, and after the changes are reviewed and approved you can merge this new configuration into the _production_ version. You also can create separate environments to control the updates: test the update on the _staging_ environment and then push it into _production_.

{% embed url="https://youtu.be/E3z8j3tBlbI" %}

## Creating a new Environment

By default, any new project is created in the _production_ environment. To quickly add a new environment you need to click **Add Environment** button in project settings and then merge from the existing production environment into the new one.

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MVqVcemNcd0Dz8VnOny%2F-MVqkvpV0H7_FsvyQAfy%2FGIF191.gif?alt=media&token=3f3d19d4-1505-4614-85eb-3e3db96701d7)

Now you have a full copy of your production version where you can change, test, and troubleshoot without affecting the production version of the project.

{% hint style="info" %}
Initially, you’ll find a single default environment, which is named “Production”. Any credentials you’ve already added are kept in the "Production" environment. When you connect your data sources to Jet, it uses only the default environment, and not any other one.
{% endhint %}

## Managing Updates

To make sure your users always use a stable version of Jet, you can lock the production version of the project in the Production environment, and set the project version to "Latest" in the staging environment. This will keep the staging version up to date and allow you to test any new update prior to approving it for production.

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MVqVcemNcd0Dz8VnOny%2F-MVqm6Fjng9YQB-K-Uih%2FGIF192.gif?alt=media&token=0b10a884-8806-4321-ad58-3b12ff86c866)

{% hint style="info" %}
You can rename your environment at any time and set a new color for the environment so that you can easily find out which environment you are in right now. You can also create an unlimited number of environments.
{% endhint %}

## Merging Environments

Once you've made the changes in the staging or development environment, you can transfer those changes onto the production or any other environment. For that, in any environment click **Merge environment**. Then select the environment you'd like to copy the changes from and the environment you'd like to apply those changes for and click **Merge**. 

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MVqVcemNcd0Dz8VnOny%2F-MVqoFZE8v32kDyDWpZB%2FGIF193.gif?alt=media&token=3157e385-c246-4211-b191-ca5c67343206)

## Switching between Environments

Any user who is invited into an existing environment can switch between environments. Hover your mouse over the project icon \(top right\) and then select an environment from the drop-down.

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MVqVcemNcd0Dz8VnOny%2F-MVqq0T2t-ACjkb7Q0dj%2FGIF194.gif?alt=media&token=a1e2721a-0394-401f-bdec-0b56871ea743)

{% hint style="info" %}
A user that is not invited to an environment can only see the default "Production" environment.
{% endhint %}

