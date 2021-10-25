[comment]: # ($page_title=Python app Installation)
[comment]: # ($page_description=Step-by-step guide to installation with Python.)

Integrate our [**Jet Bridge**](https://app.gitbook.com/@jetadmin/s/doc/~/drafts/-M9TnCmHUbdvDWPtOccj/jet-bridge-deployment/install) ****plugin with Python installation. You can place it behind your VPN, in your own VPC, and works locally. We won’t get access to your data, however, you will still receive updates normally.

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MjZ3LfsU1ZReomd0nUz%2F-MjZDAnqL4DrfAe8ZOPy%2Fimage.png?alt=media&token=5da62cf8-e625-439f-9628-c0ccc09ed4d9)

### Requirements:

* Python 2.7 or 3.4+
* **pip** - package manager for Python
* Any of the following SQL Databases:
  * PostgreSQL
  * MySQL
  * SQLite
  * Oracle
  * Microsoft SQL Server
  * Firebird
  * Sybase
* **localhost** or **web server** with an external IP

### Installation

1. [Install Python](https://www.python.org/downloads/) 2.7 or 3.4+ \(comes with **pip**\).

2. Install jet\_bridge package using **pip** or update it from the command line as follows:

```bash
pip install jet_bridge -U
# or for Python 3
pip3 install jet_bridge -U
```

3. Install an appropriate database adapter and libraries:

```bash
# for PostgreSQL
pip install psycopg2

# for PostgreSQL + PosGIS
pip install GeoAlchemy2==0.6.2
pip install Shapely==1.6.4

# for MySQL
pip install mysqlclient

# for MSSQL
pip install pyodbc
```

 4. Run Jet Bridge from the command line as shown below:

```bash
# for Ubuntu/MacOS/Linux/etc (UNIX systems)
PROJECT={{project_name}} TOKEN={{token}} jet_bridge

# for Windows
set PROJECT={{Project Name}} && set TOKEN={{Token}} && jet_bridge
```

{% hint style="info" %}
**{Project Name} and {Token}** is automatically generated when you create a project.
{% endhint %}

This command creates a config if you run it for the first time.

After filling all required options you can now run Jet Bridge by executing the command once again:

```bash
jet_bridge
```

5.  Finish your project installation by opening this link in your browser \(usually, it opens automatically\):

```bash
http://localhost:8888/api/register/
```

**localhost** is your **Jet Bridge** HOST and **8888** is its PORT.

If you want to run Jet Bridge on a different host or port, read the instructions on the [Configuration page](jet-bridge-deployment/jet-admin/configuration#setting-up-your-configuration).

{% page-ref page="user-guide/data" %}



