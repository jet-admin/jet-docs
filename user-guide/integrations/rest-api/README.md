**Jet Admin** can help you make your tool make requests to any **Rest API** you need to integrate to your workflow. The integrations Jet provides are ready-to-use business APIs such as [Stripe](user-guide/integrations/stripe), [SendGrid](user-guide/integrations/sendgrid), [Zendesk](user-guide/integrations/zendesk), [Slack](user-guide/integrations/slack), etc. \(To reduce the time to get your internal tool talking to a Rest API to the minimum, use the [Templates]()\). To have the  available APIs at hand, select Resources from the project menu to open the resource selection pane:

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MjZ3LfsU1ZReomd0nUz%2F-MjZDXsEBzZTuXAkp_Zx%2Fimage.png?alt=media&token=b3d3b3df-0908-420f-9c05-872a7434a72d)

You can also implement your own custom API using API Builder. For instance, you can set up a `GET` request to [display orders your customers made](getting-started/part-2-intermediate/perform-api-requests) or a `POST` request to reset a password for a specific user.  

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MjZ3LfsU1ZReomd0nUz%2F-MjZVvG9K5ZfSoInml1f%2Fimage.png?alt=media&token=a7a3a486-e420-4624-b478-c532e6cd28d8)

{% page-ref page="user-guide/data/make-an-http-request" %}

## Connect custom API resource

Let's start with implementing **Rest API**, select it from the list of available resources, and specify the general information that will use for all API requests for this resource: 

* **Resource name** – unique name that indicates API resource in Jet Admin.
* **Base URL** – URL that will use for all requests for this resource \(if you want to use different URL, create different resources for each URL\).
* **Authentication** –  used to authenticate requests: [Bearer token](user-guide/integrations/rest-api/bearer-token), [Basic Auth](user-guide/integrations/rest-api/basic-authentication), [OAuth 2.0](user-guide/integrations/rest-api/oauth-2.0).

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MEEy8r9TeZrjti2WcdH%2F-MEF0ooHWOzlsbGq1cEl%2Fimage.png?alt=media&token=877903df-16f6-4cd0-b3e8-bd0284ae3504)

{% page-ref page="user-guide/data/make-an-http-request" %}



