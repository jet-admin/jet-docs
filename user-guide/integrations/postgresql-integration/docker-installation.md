Integrate our [Jet Bridge](jet-bridge-deployment/jet-admin) plugin with Docker installation in one command. You can place it behind your VPN, in your own VPC, and works locally. We won’t get access to your data, however, you will still receive updates normally.

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MEATPYmRPkKrbdBF-ss%2F-MEAU0_SZcU_GYa4Eh0l%2Fimage.png?alt=media&token=df27931d-7909-43bb-8cd1-656435690691)

### Requirements:

* Docker installed
* localhost or web server with an external IP

### Installation:

1. Install [Docker](https://docs.docker.com/get-docker/) and make sure it works correctly.

2. Install Jet Bridge container by running: 

```bash
sh <(curl -s https://app.jetadmin.io/install_jet.sh) {{Project Name}} {{Token}}
```

{% hint style="info" %}
**{Project Name} and {Token}** is automatically generated after signed up
{% endhint %}

3.  Finish your project installation by opening in your browser:  
**localhost** is your **Jet Bridge** HOST and **8888** is its PORT.

```bash
http://localhost:8888/api/register/
```

{% page-ref page="user-guide/data" %}

