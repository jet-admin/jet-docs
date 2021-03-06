[comment]: # ($page_title=Custom component)
[comment]: # ($page_description=Custom component overview)

# What is a Custom Component?

For very specific pages you can create your own custom Component based on React, Angular, ****or any other framework and integrate it in Jet Admin interface. Writing your own custom JS/CSS/HTML has no limits in implementing any page you need. 

To integrate your custom Component with Jet Admin data you can use the Jet Admin SDK library.

# Create a Custom Component

In this tutorial, we'll show you how to create a sample Flex View component which you can, later on, extend to satisfy whatever needs you have.

### 1. Create your FlexView component project \(playground\) or clone an example

A Flex View uses [Web Component](https://www.webcomponents.org/introduction) specification to integrate any **JS** based component to **Jet Admin** – this allows you to use any **Frameworks** and **Libraries** you like as long as you create them as custom **Web Components**. So it can be **React**, **Angular**, **Vue.js** based components or any other.

First, you need to create a **FlexView** project where you can develop and test it. This project will be your playground for creating **FlexView**. It will work the same way as on **Jet Admin** but will make your development easier so that you can use your favourite **IDE** and environment. To make it simpler, you can use some of our ready-to-use starter projects on **GitHub** or use them as a reference:

* React – [https://github.com/jet-admin/jet-flex-view-react-example](https://github.com/jet-admin/jet-flex-view-react-example)
* Angular – [https://github.com/jet-admin/jet-flex-view-angular-example](https://github.com/jet-admin/jet-flex-view-angular-example)

For example, here's an example of cloning React and preparing it for work:

```bash
git clone git@github.com:jet-admin/jet-flex-view-react-example.git
cd jet-flex-view-react-example
npm install
```

### 2. Run your project

After you created your project and cloned an example, make sure it works by running this command \(or any other you use\):

```text
npm run start
```

![http://localhost:3000/](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-LY1QiCedojQjKZlgig5%2F-LY1WxkHIRpYS50Ol5Yi%2Fimage.png?alt=media&token=dde5b84a-36a3-4aba-b6f8-68aaec629eb0)

The project works fine, which means that you can start developing your **FlexView**. But before that, read the following step if you need the **Jet Admin API** integration.

{% hint style="warning" %}
Consider the following limitation while developing:

* You can't use change URL inside FlexView since component is embed inside Jet Admin view
* Consider incapsulating styles inside your view, not use global styles
{% endhint %}

### 3. \(optional\) Set up Jet API integration

To integrate your custom **FlexView** with **Jet Admin** data and API, you can use **Jet Admin SDK** library. To start using it, you would have to install it first:

```bash
npm install jet-admin-sdk
```

To work with **API** and perform queries, the **SDK** needs to know which **Project** you are working with and your **Access Token.** When a **FlexView** is uploaded to production, it will fetch these automatically, but for development you need to specify it manually as shown below:

```javascript
import { getPublicApiService } from 'jet-admin-sdk';

if (!process.env.NODE_ENV || process.env.NODE_ENV === 'development') {
  getPublicApiService().projectsStore.setCurrent('YOUR_PROJECT_UNIQUE_NAME');
  getPublicApiService().authService.tokenLogin('YOUR_USER_TOKEN');
}
```

* **YOUR\_PROJECT\_UNIQUE\_NAME** – can be taken from URL of your project on Jet Admin
* **YOUR\_USER\_TOKEN** – can be taken from cookie token on [https://app.jetadmin.io/](https://app.jetadmin.io/)

That's it! You can now use **Jet Admin API** through **PublicApiService.** For example:

```typescript
import { getPublicApiService } from 'jet-admin-sdk';

getPublicApiService().currentUserStore.get().subscribe(result => {
  if (result) {
    console.log('Current User is ' + result.username);
  } else {
    console.log('Failed to get Current User');
  }
});
```

###  4. Upload your FlexView to Jet Admin

Once you're finished with your **FlexView** or just want to test it in a real application, you need to upload it. Build your project first:

```bash
npm run build
```

Usually, it will create your build files in **dist** folder, but it can differ for your environment. To upload your **FlexView** to **Jet Admin,** you need to upload a **.zip** file with your build files. Go to **dist** folder and compress all the contents to a single **.zip** file.

Now go to **Jet Admin** and create **Custom Component** as shown below.

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MTKcyZiEnBxoDdDTFai%2F-MTKdHGPmjCC0UD09whA%2Fimage.png?alt=media&token=79074d91-5791-4e43-adb1-85b095294fdb)

You will need to specify the following settings and click the **Save** button:

* **Compiled custom element** – **zip** file containing your build files of **FlexView**.
* **Custom element tag name** – tag name that you used for **Web Component** inside your **FlexView** project. Should pre prefixed with "jet-" and has dash-case. Also each of your **FlexView** should have unique tag names across your **Jet Admin** project.
* **Files to include into page** – in order for your **FlexView** to work **JS** and maybe **CSS** files should be included. You should check which files from your **zip** files should be included. The order of loading can be changed. These files will be included only once when **FlexView** should be displayed and after inclusion they must defined custom element with tag name the same as you specified for **Custom element tag name.**

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MTKcyZiEnBxoDdDTFai%2F-MTKdOgE8k8HXkTVnrsE%2Fimage.png?alt=media&token=35f29a2c-11cb-46b9-b1ee-bd8f1b9c31d7)

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MTKcyZiEnBxoDdDTFai%2F-MTKdSfzdYG2rWkSef6Y%2Fimage.png?alt=media&token=afc96174-b002-423f-9eb8-206fc7139a53)

{% hint style="success" %}
That's a wrap. Feel free to test your **FlexView** now.  
If you want to update it later, you can upload a new **.zip** file inside **Custom Component**.
{% endhint %}

# Set Custom Component Inputs

You can specify **Inputs** to pass data inside **FlexView** from **Jet Admin** if you have defined custom attributes for your **FlexView** \(Examples from GitHub include them already\).

{% hint style="warning" %}
**For Angular**: Please note that Angular changes **Inputs** names to **dash-case** when creating **Custom Element** \([https://angular.io/guide/elements\#mapping](https://angular.io/guide/elements#mapping)\)
{% endhint %}

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MTKcyZiEnBxoDdDTFai%2F-MTKeDXa-b0dCenB3J7j%2Fimage.png?alt=media&token=8be4aff6-4e14-4204-9c02-ef78ee7e9f1b)

# Use Custom Component Outputs

You can specify **Outputs** to take from your **FlexView** and use their values in other **Jet Admin** components**.** For such cases you should set **Outputs** inside your **FlexView** by sending **CustomEvent** with **Output** name and its value in **detail** field \(Examples from GitHub include it already\).

Then you can create **Output** and set its name and use them for other components \(for example set **Text Field** value to **FlexView Output**\).

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MTtq21IzkuOU6N0gmbf%2F-MTtqE0XJq9vQlNYzv6j%2Fimage.png?alt=media&token=d8eaee8f-d0be-4c94-8aa4-ae1670dd2d64)

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MTtq21IzkuOU6N0gmbf%2F-MTtqmZy52xy1vuRYNTU%2Fimage.png?alt=media&token=5976fdd4-a0df-466c-8361-673581d5f915)





