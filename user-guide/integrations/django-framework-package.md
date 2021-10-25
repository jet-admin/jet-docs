[comment]: # ($page_title=Django)
[comment]: # ($page_description=Connecting Django to Jet Admin)

To integrate Jet Admin with your Django project you need to install the [Jet Bridge](jet-bridge-deployment/jet-admin) ****package. It will work even with your local application on localhost. Jet Bridge is an open-source plugin available on [Github](https://github.com/jet-admin/jet-bridge). ****It will connect to your database and link Jet Admin with your project. 

{% page-ref page="jet-bridge-deployment/jet-admin" %}

This is the quickest way to install **Jet Admin** for Django based projects. Installed in the same way as most **Django** packages. 

### Requirements

* **Python** 3.4+
* **Django** 1.11+
* **localhost** or **web server** with external IP

### Installation

1. Download and install the latest version of **Jet Bridge** for **Django**:

```bash
pip install jet-django
```

3. Add `jet_django` application to the `INSTALLED_APPS` setting inside **settings.py** file \(your Django project\):

```python
INSTALLED_APPS = (  ...  'jet_django',  ...)
```

4. Set `JET_PROJECT` and `JET_TOKEN` inside **settings.py** file:

```text
JET_PROJECT = '{{your_project_name}}'
JET_TOKEN = '{{your_jet_token}}'
```

Jet Token is automatically generated for each project, you can find it in the settings.

5. Add a URL-pattern to the **urls.py** file. Remember to import **path** and **include:**

```python
urlpatterns = [  ...  path('jet_api/', include('jet_django.urls')),  ...]
```

If you use **Django &lt; 2.0:**

```python
urlpatterns = [  ...  url(r'^jet_api/', include('jet_django.urls')),  ...]
```

6. Run your Django server. Change into the outer your project directory, if you haven’t already, and run the following command:

```python
py manage.py runserver
```

8. Finish installation by opening this link in your browser, where **localhost** is your **Django** HOST and **8000** is its PORT. 

```http
http://localhost:8000/jet_api/register/
```

{% hint style="info" %}
**Jet Django** package sets **CORS** headers for **/jet\_api/** endpoints. If it conflicts with your **CORS** headers and you want to deal with it yourself, add the following in **settings.py**:   
JET\_CORS\_HEADERS = False
{% endhint %}

{% page-ref page="jet-bridge-deployment/jet-admin/common-problems" %}



