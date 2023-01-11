[comment]: # ($page_title=Xano)
[comment]: # ($page_description=This guide explains how to quickly connect Xano back-end to a Jet Admin front-end.)

---
description: >-
  This guide explains how to quickly connect Xano back-end to a Jet Admin
  front-end.
---

# Xano

Xano is the fastest way to build a powerful, scalable backend for your app without code. We will guide you how you can quickly connect Xano back-end to Jet Admin. Check our Tutorial: [How to build business apps for your Xano back-end without code](https://blog.jetadmin.io/how-to-build-business-apps-for-your-xano-back-end-without-code/)

### **Step 1: Create APIs on top of your database**

Once you have created a Database and filled in data, you should create APIs for your Database in Xano. There are two options to create Endpoints in Xano:&#x20;

* Default CRUD operations endpoints&#x20;
* Create custom API endpoints

#### 1.1 Default CRUD operations endpoints

1. **Use Default CRUD operations endpoints**. Go to the **API tab** in Xano from the left menu and choose **Default** API Group and Copy **API Group Base URL to your clipboard, and let’s head over to Jet Admin!**

<figure><img src="https://images.surferseo.art/cbc95fa8-9555-4733-8477-4eaae10e07ce.jpeg" alt=""><figcaption></figcaption></figure>

#### **1.2 Create custom API endpoints**

To successfully create custom API endpoints, mark all API endpoints: Specify the **Description** field for each API endpoint.

First, go to **Add API Group** and fill in Name and Description. Next, click **Add API endpoint**.

<figure><img src="https://blog.jetadmin.io/content/images/2023/01/xano5.gif" alt=""><figcaption></figcaption></figure>

Fill the **Description** field of the API endpoint you want to use in Jet Admin with the following content:

* _For Get record list API endpoint:_ Query all **TABLE** records
* _For Create record API endpoint:_ Add **TABLE** record
* _For Delete record API endpoint:_ Delete **TABLE** record
* _For Get one record API endpoint:_ Get **TABLE** record
* _For Update record API endpoint:_ Edit **TABLE** record

where **TABLE** is your Xano table name.

{% hint style="info" %}
Only endpoints with the specified **Descriptions will be imported** to Jet Admin. For example, if API endpoint – Get record list of Deals, in the Description field: **Query all deals records**.
{% endhint %}

### **Step 2: Connect Xano to Jet Admin**

[Create a new Project in Jet Admin](https://app.jetadmin.io/) if you don't have one. Choose Xano as a Data Source that you would like to connect.

<figure><img src="https://blog.jetadmin.io/content/images/2023/01/xano2.gif" alt=""><figcaption></figcaption></figure>

Copy **API Group Base URL** from Xano to Jet Admin

<figure><img src="https://images.surferseo.art/3e821f48-dc0f-44eb-b1e1-9e870c3a9a67.jpeg" alt=""><figcaption></figcaption></figure>

In case if you would like to protect **API endpoints** from unauthorized access, you can learn how to set it up in the video and get an **Access token**:

{% embed url="https://www.youtube.com/watch?v=TiUl1Z8WDXo" %}

Once authentication endpoint is set up, **generate an Auth Token** for **Jet Admin** integration.&#x20;

{% hint style="warning" %}
Make sure to **set expiration to "0"** in endpoint _Create Authentication Token step_ to make Auth Token permanent.&#x20;
{% endhint %}

Copy **Authorization token** to **Authorization header** in Jet Admin.

Next, choose Data Sync, which allows you to do SQL queries, and blend and join data from 30+ data sources.

<figure><img src="https://images.surferseo.art/056b7503-9668-442f-9583-855187f6d9c8.png" alt=""><figcaption></figcaption></figure>

<div>

<figure><img src="https://files.gitbook.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-LQ08RFAKZvFADEiXKFy%2Fuploads%2FJO1yRGtDkU6Tu9yhNvvo%2Fimage.png?alt=media&#x26;token=cae65e2e-c26f-4bf3-b440-2c2317e2a129" alt=""><figcaption></figcaption></figure>

 

<figure><img src="https://files.gitbook.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-LQ08RFAKZvFADEiXKFy%2Fuploads%2Fkjk8J2TRWMnWAuwTAkC8%2Fimage.png?alt=media&#x26;token=f6da508e-0cc5-49b4-a242-97301b4d528f" alt=""><figcaption></figcaption></figure>

 

<figure><img src="https://files.gitbook.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-LQ08RFAKZvFADEiXKFy%2Fuploads%2FllYrJTtbLwM6hoQLd6J2%2Fimage.png?alt=media&#x26;token=2b812333-bf84-4cb3-b692-e61020d2a1d3" alt=""><figcaption><p>Copy authToken value to insert it in Jet Admin.</p></figcaption></figure>

</div>

### How to build Custom CRM using Xano

{% embed url="https://blog.jetadmin.io/how-to-build-business-apps-for-your-xano-back-end-without-code/" %}
