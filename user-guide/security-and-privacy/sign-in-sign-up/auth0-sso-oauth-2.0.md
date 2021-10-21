## 1. Go to SSO Applications

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-Mj0XZ1uwgtIRHAomVlJ%2F-Mj0YllfWnnHbYkvlzPs%2Fimage.png?alt=media&token=c01df8af-85c7-4635-9012-204b24748cef)

## 2. Create a new SSO application

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-Mj0UAersMVyFn2dPvgi%2F-Mj0V6PkXRK_z4WgM0Bx%2Fimage.png?alt=media&token=08fae1ad-94c6-493c-81f6-4b85fdc57735)

## 3. Go to Auth0 applications and create new Application

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MRzE6dowz9UERCObym7%2F-MRzEyp5oJDkqZAMJ61p%2Fimage.png?alt=media&token=5e270ec3-9e8d-406a-8c08-2376fb0de205)

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MRzE6dowz9UERCObym7%2F-MRzF1didlzstICgICUW%2Fimage.png?alt=media&token=c55212c3-91ac-4bb6-842a-13a0617f2009)

## 4. Copy credentials to Jet Admin

Choose Provider **Auth0OAuth2** on **Jet Admin** and after that copy **Domain, Client ID, Client Secret** from **Auth0**. You should also set **Scope** as **openid,profile,email,offline\_access**.

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-Mj0UAersMVyFn2dPvgi%2F-Mj0VlqrLA6dj6YT2rZW%2Fimage.png?alt=media&token=d2ae69c5-1a1d-49f7-9cb0-8b01c7136172)

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-Mj0UAersMVyFn2dPvgi%2F-Mj0W-bKol9WBVTBZPbC%2Fimage.png?alt=media&token=b0feb680-a8d6-4ea3-861d-1cad9d005347)

## 5. Set Allowed Callback URL on Auth0

Copy **REDIRECT URL** from **Jet Admin** in **Application parameters** section to **Auth0 Allowed Callback URLs** and click **Save** on both **- Auth0** and **Jet Admin.**

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-Mj0UAersMVyFn2dPvgi%2F-Mj0WpuT-ZIhaLaKV1Ud%2Fimage.png?alt=media&token=0c0cbe8c-8470-4fd2-9eeb-66d577729175)

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-Mj0UAersMVyFn2dPvgi%2F-Mj0WvAC0xQSgs59xOb1%2Fimage.png?alt=media&token=e72fd06b-085c-4e6c-902d-16627c07f6fe)

## 6. You are all set

**SSO** button should appear automatically on the login and register pages when visiting **Jet Admin** from your **custom domain**.

