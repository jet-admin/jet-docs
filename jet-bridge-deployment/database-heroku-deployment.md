Once you have created the project, connected the resource, and selected the [Instant Cloud](user-guide/integrations/postgresql-integration/instant-cloud) deployment method you need to deploy your database on hosting.

In this step-by-step guide, we'll take a closer look at the complete database deployment process on [Heroku](https://www.heroku.com/).

## 1. Sign up for Heroku

To deploy your database you need to [sign up](https://signup.heroku.com/) a free Heroku account. You need to fill in the data and just click on **Create a free account**.

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-M9_G23h5K60f727bnAf%2F-M9_Q1tM6xmqh4DMs2NT%2Fimage.png?alt=media&token=a6a7a9e1-3d9e-4b9e-8c25-0f5fe08e5bed)

## 2. Create a new app

Once you have completed the registration process, you will see this page. Just click on **Create new app**. 

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-M9_G23h5K60f727bnAf%2F-M9_YqvIjrUR3zr9c1Fm%2Fimage.png?alt=media&token=0e7b09d3-79b1-48a2-b26f-baeaf34b99ef)

The next step is to specify the application name. Keep in mind that you can't use spaces and symbols. You also have to choose a region.

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-M9_G23h5K60f727bnAf%2F-M9__PGQjNcjr69PXCAN%2Fimage.png?alt=media&token=194112ca-95d7-42b9-b7c2-d808d05a6ef8)

## 3. Configure your application

Go to the Resources menu. Just search for **Postgres** in the add-ons and select it.

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-M9_G23h5K60f727bnAf%2F-M9_bamouhlykqSQswjS%2Fimage.png?alt=media&token=00ccb2d3-2bd3-4673-8e24-4f473d757307)

Then you need to choose a plan for the add-on. Depending on it you'll have different resources. For test purposes, we will pick **Hobby Dev - free**.

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-M9_G23h5K60f727bnAf%2F-M9_d2iej6Tyfn4YLo_Y%2Fimage.png?alt=media&token=920ba825-683d-43e9-85ae-a90c1b792444)

## 4. Find the credentials

Now you have a working Postgres database. You need to find the credentials. Click on Heroku Postgres to find the data you need.

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-M9_G23h5K60f727bnAf%2F-M9_eFk6XGRpwNf7EMPI%2Fimage.png?alt=media&token=914109da-a905-409f-9273-a4d9843ea773)

Go to the settings and click View Credentials.

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-M9_G23h5K60f727bnAf%2F-M9_fLkMVsp1Vg1Zq02U%2Fimage.png?alt=media&token=537856d5-fb39-4867-ac0c-a20a31b1dcc1)

You need to enter these data in the fields required by the [Instant Cloud](user-guide/integrations/postgresql-integration/instant-cloud) deployment method.

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-M9YbUJIgKX8G719gk4j%2F-M9YfsJcJj_kFzppWVYh%2Fimage.png?alt=media&token=f88f04d4-a277-427c-8cb9-56817413ec2d)

Congratulations! You've deployed your database on Heroku. Now you're ready to [integrate](user-guide/integrations) it into Jet Admin.

