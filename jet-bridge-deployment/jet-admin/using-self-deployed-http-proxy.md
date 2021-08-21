By default, all queries for **HTTP based resources** \(**Custom Rest API, 3rd party integrations**\) are sent by **Jet Admin** through our **Jet Bridge** proxy endpoint at [https://api.jetadmin.io/api/proxy\_request/](https://api.jetadmin.io/api/proxy_request/) for convenience. Requests data going through our servers are never being recorded, but if you don't want data to go through **Jet Admin** servers you can use a self-hosted **HTTP Proxy** on your side as part of an open-source **Jet Bridge** application.

# Using self-deployed HTTP proxy

Follow instructions after you have created **Jet Admin** **Rest API** resource:

### 1. Install Jet Bridge

Use the following guides to install **Jet Bridge** application as standalone **Python application** or **Docker container.** Specify the following **Jet Bridge** configuration during install if you don't need **SQL** integration:

**DATABASE\_ENGINE** = none  
**ALLOW\_ORIGIN** = &lt;Jet Admin hostname&gt; \(https://app.jetadmin.io or your custom domain\)

{% page-ref page="user-guide/integrations/postgresql-integration/python-app-installation" %}

{% page-ref page="user-guide/integrations/postgresql-integration/docker-installation" %}

{% hint style="info" %}
You can skip a database configuration part and use **Jet Bridge** just for proxying **HTTP requests**.
{% endhint %}

Check the link below to learn how to specify **Jet Bridge** configuration:

{% page-ref page="jet-bridge-deployment/jet-admin/configuration" %}

### 2. Run Jet Bridge

**3. Update resource to use custom HTTP proxy**

In resource settings click **Edit Settings** button and set **Custom HTTP proxy** to your **Jet Bridge** proxy request URL:  
&lt;**JET\_BRIDGE\_HOST&gt;/api/proxy\_request/**

For example for Jet Bridge running on localhost and port 8888 this will be:   
[http://localhost:8888/api/proxy\_request/](http://localhost:8888/api/proxy_request/)

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MA_tq1uE2eP7xzJBnnV%2F-MA_vQYOStyxX00f1vRF%2Fimage.png?alt=media&token=1ff228d9-19e2-4884-af0d-41af918bda3b)

### 4. You are done!

Now all HTTP queries for this resource will be sent through your server.

