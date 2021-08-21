To enable **Basic Authentication** schemes, choose Basic Auth in the **Authentication** dropdown, and then provide the username and password.

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MEEy8r9TeZrjti2WcdH%2F-MEF0xskiG5S2ER9ac6l%2Fimage.png?alt=media&token=3c57b138-4938-4372-a503-e1161fefcdb8)

This is most commonly called **Username/Password** or just **Basic**. If you see the word basic around an authentication section, then you should use this type.

Most of the time, you just put in the username and password that you have for this service, and they use it to authentication you.

Sometimes, an API may tell you to send your API key as a username or a password or both. In this case, put the API key in the appropriate field, and if the other is not mentioned, leave it blank.

Many times, if the API docs are showing you a cURL example, you will see something like this \(let's go through the Stripe API example\):

```markup
curl https://api.stripe.com/v1/charges \
  -u sk_test_W6QCMUNIMOQMaBlZPNPDBFMG00hTMhVJbr: \
  -d limit=3 \
  -G
```

Notice there is the URL, followed by:

`-u sk_test_W6QCMUNIMOQMaBlZPNPDBFMG00hTMhVJbr:`

That is what tips you off that this is Basic Auth. The **-u** part signifies Basic Auth, and then the colon at the end tells you this is being sent as a username. In normal Basic Auth, you send the username and password in the following format **username : password** so if you see a **-u** then you know that anything to left of the colon is the username and to the right is the password. In this example, the API key is sent as a username.

{% page-ref page="user-guide/data/make-an-http-request" %}

