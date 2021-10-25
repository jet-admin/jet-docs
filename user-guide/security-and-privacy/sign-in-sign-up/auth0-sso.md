[comment]: # ($page_title=Auth0 SSO SAML2)

## 1. Go to SSO Applications

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-M0UJ1ZdHOf7P2oavvqy%2F-M0UKeS9Ky35jgU28qnx%2Fimage.png?alt=media&token=082e8e48-c23f-487d-83c2-3c69f3d119d2)

## 2. Create a new SSO application

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MRzE6dowz9UERCObym7%2F-MRzEnIgtsG5Vs1b6DyS%2Fimage.png?alt=media&token=28df24c1-1b1d-42fa-9c40-09d3598a0a5b)

## 3. Go to Auth0 applications and create new Application

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MRzE6dowz9UERCObym7%2F-MRzEyp5oJDkqZAMJ61p%2Fimage.png?alt=media&token=5e270ec3-9e8d-406a-8c08-2376fb0de205)

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MRzE6dowz9UERCObym7%2F-MRzF1didlzstICgICUW%2Fimage.png?alt=media&token=c55212c3-91ac-4bb6-842a-13a0617f2009)

## 4. Activate SAML2 Web App

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MRzE6dowz9UERCObym7%2F-MRzF9dhlzr3QIRjZTWP%2Fimage.png?alt=media&token=6d89135e-7a14-45a2-84da-72baf3374e70)

## 5. Specify mappings in Settings

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MRzE6dowz9UERCObym7%2F-MRzFLKCD4IB_nYHEbgb%2Fimage.png?alt=media&token=39b194e4-4eff-4a0a-aa7f-20ba3164210c)

```javascript
{
  "mappings": {
    "email": "Email",
    "given_name": "FirstName",
    "family_name": "LastName"
  }
}
```

## 6. Download metadata

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MRzE6dowz9UERCObym7%2F-MRzFgjlV1Hbf9hsB--B%2Fimage.png?alt=media&token=3d9f1eea-9063-4088-ba8d-9833daeef938)

## 7. Upload metadata and set ACS url in Auth0

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MRzE6dowz9UERCObym7%2F-MRzG-0thn6iYxneKfNf%2Fimage.png?alt=media&token=f2aa368e-69ef-4b0f-b092-a138d0ba36ba)

## 8. You are all set <a id="10-you-are-all-set"></a>

**SSO** button should appear automatically on the login and register pages when visiting **Jet Admin** from your **custom domain**.

