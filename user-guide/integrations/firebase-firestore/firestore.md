Connect Jet Admin to Firebase's Admin API to create custom internal tools to manage your Firebase application.

Once Firebase is added to Jet Admin, you'll be able to manage your users, query and update Firebase Real-time Databases as well as query Firestore.

## 1. Get Firebase Key

To get Firebase Key you need to add Firebase to your Google project. First, go to [Firebase ](https://firebase.google.com/)and just click **Get Started**.

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MAp4YMwkQgaiNOUtjdW%2F-MAu_SokLQhpGN-kbfq0%2Fimage.png?alt=media&token=ea6b3f9f-2825-40d5-98f0-629871775368)

Choose your Google Account to start. ****Then you need to click on Add project to get Firebase Key.

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MAp4YMwkQgaiNOUtjdW%2F-MAuc7DbXkiciHNqYvYZ%2FGIF.gif?alt=media&token=4bb17e2d-94c3-4fe7-ad2f-2880a958970c)

Then you need to go to the Service Accounts to generate a new private key. Once you have generated a private key, it will automatically download to your computer.

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MAp4YMwkQgaiNOUtjdW%2F-MAud3odP9B7UxZ1uIPW%2FGIF.gif?alt=media&token=642eb98a-ffa9-4937-b868-f3034cbaa924)

## 2. Add Firebase to Jet Admin

Add a new resource to an existing project or connect to Firebase when creating a new project. The integration process will be the same in both cases.

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MjZ3LfsU1ZReomd0nUz%2F-MjZ5pHRwy0pJsstY7JP%2Fimage.png?alt=media&token=2aaf9671-d100-4d7e-b707-2ab7dda09472)

Select Firebase from the list of available resources and enter your private key in JSON format. You can upload JSON file or copy the code to Service Token field.

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MjZ3LfsU1ZReomd0nUz%2F-MjZanlsGpAN3khPeL8g%2Fimage.png?alt=media&token=5b99c663-1e63-42af-9b86-a49589852b10)

An example of JSON Service Key obtained from Firebase.

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

