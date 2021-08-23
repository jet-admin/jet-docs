---
description: >-
  The following instructions will guide you through the installation process of
  Jet Admin
---

# Installation – Jet Bridge

**Jet Bridge** is an open**-**source plugin available on [**Github**](https://github.com/jet-admin/jet-bridge)**.** It will connect to your database and link **Jet Admin** with your project. It will work even with your local application on **localhost**.

{% hint style="warning" %}
**Jet Admin** is a small web server that connects to your database using **Tornado** and generates an API interface through which **Jet Admin** can operate with your data.
{% endhint %}

### Method 1. Deploy to Heroku

The simplest way to install **Jet Admin** is to deploy it to the **Heroku** cloud platform. It will require you to allow external access to your database.

{% page-ref page="any-sql-deploy-to-heroku.md" %}

### Method 2. Using only Jet Bridge

Install **Jet Bridge** without additional software or web services on any server or localhost. You will need to install **Python** dependencies and run the application manually.

{% page-ref page="any-sql-jet-bridge-app.md" %}

### Method 3. Using Jet Bridge inside Docker

Install **Jet Bridge** without need to install any dependencies except **Docker** application. May require additional network configuration for your OS.

{% page-ref page="any-sql-jet-bridge-docker.md" %}

### For Django framework

To integrate **Jet Admin** with your **Django**-based project you need to install the **Jet Bridge** package. It will work even with your local application on **localhost**.

**Jet Bridge** **for Django** sources are available on **Github:**  
[https://github.com/jet-admin/jet-django](https://github.com/jet-admin/jet-django)

This is the quickest way to install **Jet Admin** for Django based projects. Installed in the same way as most **Django** packages.

{% page-ref page="../../getting-started/integrations/django-framework-package.md" %}

## Common problems

Please see our guide to fixing some of the most common installation issues.

{% page-ref page="common-problems.md" %}

