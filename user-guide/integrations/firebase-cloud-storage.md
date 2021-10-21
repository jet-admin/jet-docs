Before you can use Firebase Cloud storage, you need to obtain a service token key. Follow the steps below to integrate Firebase storage with Jet.‌

## Get Firebase Storage JSON Key <a id="1-get-firebase-key"></a>

To get the JSON key you need to add Firebase to your Google project. First, go to [Firebase](https://firebase.google.com/) and just click **Get Started**.

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MWPTvbPDMAbsJaFXHMo%2F-MWPyFl0b8QAl1KwF_q6%2Fimage.png?alt=media&token=d7b1c8d9-56b6-4f9b-a605-fd1141291f2e)

First, Choose your Google Account. Then you need to click on **Add project** to get a Firebase Key.​

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MWPTvbPDMAbsJaFXHMo%2F-MWQ0vloTcTeL4flpQOY%2FGIF.gif?alt=media&token=abd07498-645b-4f37-9d48-be907cd13ff7)

Then you need to go to the Service Accounts to generate a new JSON private key. Once you have generated a private key, it will be automatically downloaded to your computer.​

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MWPTvbPDMAbsJaFXHMo%2F-MWQ1D2ZGO04wQFTIFb3%2FGIF%20%281%29.gif?alt=media&token=ac75c780-fb03-4189-bd46-3cb85bde0770)

## Add Firebase Storage to Jet Admin <a id="2-add-firebase-to-jet-admin"></a>

Select Firebase Storage from the list of available storage options, upload the JSON file or paste the service token generated for your service account.

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MWPTvbPDMAbsJaFXHMo%2F-MWQ2BK8D9ktvP9t8p0Z%2Fimage.png?alt=media&token=1693bead-ba2f-432f-a725-0a5d3e8522c7)

Here's an example of a JSON Service Key obtained from Firebase:

```javascript
{
  "type": "service_account",
  "project_id": "{your_project_name}",
  "private_key_id": "{your_private_key_id}",
  "private_key": "-----BEGIN PRIVATE KEY-----\{your_private_key}\n-----END PRIVATE KEY-----\n",
  "client_email": "{you_client_email}",
  "client_id": "{your_client_id}",
  "auth_uri": "https://accounts.google.com/o/oauth2/auth",
  "token_uri": "https://oauth2.googleapis.com/token",
  "auth_provider_x509_cert_url": "https://www.googleapis.com/oauth2/v1/certs",
  "client_x509_cert_url": "{you_client_url}"
}
```

Once you have integrated Firebase Storage with Jet you will see a **Storage File Viewer** that'll allow you to access your data.

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MWPTvbPDMAbsJaFXHMo%2F-MWQ79trxLw_279zMgCa%2FGIF213.gif?alt=media&token=e5fd4cd9-f09d-4bde-b9b8-4b2adc649c59)

