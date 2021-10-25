[comment]: # ($page_title=Google Cloud Storage)

Before you can use Google Cloud Storage storage, you need to set it up properly. Follow the steps below to integrate GC Storage with Jet.

## Get Google Cloud credentials

In the Cloud Console, go to the [Create service account key](https://console.cloud.google.com/apis/credentials/serviceaccountkey) page and select the required project then follow the steps:

1. Hit **Create Service Account**
2. In the **Service account name** field, enter a name
3. From the **Role** list, select **Project** &gt; **Owner**

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MW-EUvGyD_qbxmNlR9w%2F-MW-l3tcAoqa8oYXOBqG%2FGIF200.gif?alt=media&token=e8809e30-b33e-4bd4-91bc-5e1675f101ba)

Now you have to export the JSON key to integrate Google Storage with Jet:

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MW-EUvGyD_qbxmNlR9w%2F-MW-rDY6WVdnKo-sTAmU%2FGIF201.gif?alt=media&token=1ee8a838-5dd9-4287-8117-5e92427584b0)

## Integrate Google Cloud Storage with Jet

Select GC Storage from the list of available storage options and paste the service token generated for your service account. 

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MW-EUvGyD_qbxmNlR9w%2F-MW0DyLvYBRhW45k-qoD%2Fimage.png?alt=media&token=b94a2cf5-581e-4521-803c-df446e69f2ba)

Here's an example of JSON Service Key obtained from Google Cloud Console.

```javascript
{
  "type": "service_account",
  "project_id": "{project_id}",
  "private_key_id": "{private_key_id}",
  "private_key": "-----BEGIN PRIVATE KEY-----\{private_key}\n-----END PRIVATE KEY-----\n",
  "client_email": "{client_email}",
  "client_id": "{client_id}",
  "auth_uri": "https://accounts.google.com/o/oauth2/auth",
  "token_uri": "https://oauth2.googleapis.com/token",
  "auth_provider_x509_cert_url": "https://www.googleapis.com/oauth2/v1/certs",
  "client_x509_cert_url": "{client_x509_cert_url}"
}
```

