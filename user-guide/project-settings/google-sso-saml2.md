Setting up **SSO** for your **Jet Admin** project requires your to set up **Custom Domain** for your project first.

## 1. Go to SSO Applications

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-M0UJ1ZdHOf7P2oavvqy%2F-M0UKeS9Ky35jgU28qnx%2Fimage.png?alt=media&token=082e8e48-c23f-487d-83c2-3c69f3d119d2)

## 2. Create a new SSO application

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-M0UJ1ZdHOf7P2oavvqy%2F-M0UKpT31Q2aOyb3dbRe%2Fimage.png?alt=media&token=97d2a07e-5076-48a5-ae5e-ffa7c5fdff14)

## 3. Open your G Suite SAML Apps and create a new one

G Suite Apps page is located at [https://admin.google.com/u/1/ac/apps](https://admin.google.com/u/1/ac/apps)

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-M0UJ1ZdHOf7P2oavvqy%2F-M0UL5WflGOdgVolKNCc%2Fimage.png?alt=media&token=21de4a34-6277-4c93-a6fb-49beec209555)

## 4. Select SETUP MY OWN CUSTOM APP

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-M0UJ1ZdHOf7P2oavvqy%2F-M0ULICT2aGi7V9fEPwE%2Fimage.png?alt=media&token=6aa3f8f7-9abb-4b8f-808e-aa7aae3bd504)

## 5. Download IDP metadata .xml file

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-M0UJ1ZdHOf7P2oavvqy%2F-M0ULQJp3tbHXPpM3mF_%2Fimage.png?alt=media&token=52b9e449-c9b2-4bed-9bef-450d37c5b704)

## 6. Specify application basic information

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-M0UJ1ZdHOf7P2oavvqy%2F-M0ULaXRlC2RKgxFZTc3%2Fimage.png?alt=media&token=2d37508c-6592-481e-9e3c-570217101d54)

## 7. Set up Jet Admin SSO application and copy ACS URL

Specify **Entity ID** and upload saved **Metadata \(.xml\)** file from the previous step.  
**Entity ID** should be unique text identifier of your application

**ACS URL** displayed at the bottom of page will be needed on the next step.

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-M0UJ1ZdHOf7P2oavvqy%2F-M0ULzRsYFXa0PcPX8th%2Fimage.png?alt=media&token=634292d3-15d5-4321-b147-8a4d867a15cd)

## 8. Set up G Suite SAML App

Specify **ACS URL** and **Entity ID** entered on the previous step

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-M0UJ1ZdHOf7P2oavvqy%2F-M0UMgHUAIdwN-Mqt5b8%2Fimage.png?alt=media&token=24bb195f-25ec-4784-85fa-d1bf00b6cd9a)

## 9. Set attributes mapping

You should specify 3 attributes to map on Jet Admin user account:

* **Email** should map to **Basic Information - Primary Email**
* **FirstName** should map to **Basic Information - First Name**
* **LastName** should map to **Basic Information - Last Name**

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-M0UJ1ZdHOf7P2oavvqy%2F-M0UMMFHAkWbp2GNnok2%2Fimage.png?alt=media&token=30b2dbce-3217-4e86-9ad1-30eba48ec56a)

## 10. You are all set

**SSO** button should appear automatically on the login and register pages when visiting **Jet Admin** from your **custom domain**.

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-M0UJ1ZdHOf7P2oavvqy%2F-M0UMT54AlLu1h3VVSEK%2Fimage.png?alt=media&token=5315bd5c-39a8-4e5f-a41a-da690c10a943)

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-M0UJ1ZdHOf7P2oavvqy%2F-M0UOX4RWg10QpSnDwCE%2Fimage.png?alt=media&token=be61ec00-5391-46cd-aa4c-490b87232c25)

