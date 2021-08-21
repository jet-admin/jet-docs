If you want to use Google services such as Google Sheets, Google Drive, Google Cloud and many others, this step-by-step guide can help you with **Google OAuth 2.0** authentication.

Once you have created the project and selected the Rest API resource, you also selected the [OAuth 2.0](user-guide/integrations/rest-api/oauth-2.0) authentication method - you need to select a provider.

# Google Developers Console

## 1. Google API Console

Visit the [Google API Console](https://console.developers.google.com/) to obtain OAuth 2.0 credentials such as a `Client ID` and `Client secret` that are known to both Google and Jet Admin.

## 2. Create a new project

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-M9ovC5iyc-KFVLQs7KG%2F-M9p7If5E6K7LG6dIv5g%2Fimage.png?alt=media&token=9b9074ba-4eff-4a96-a1d1-7b5c2d1f34c6)

## 3. Specify new project details

Specify `Project name` and `Location` then click the **Create** button.

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-M9ovC5iyc-KFVLQs7KG%2F-M9p8eiPBjOvb7C6gUjl%2Fimage.png?alt=media&token=620613dd-3b92-4872-ab25-3ae21796219b)

## 4. Enable APIs and Services

In the control panel, enable the API and Services you plan to use. 

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-M9ovC5iyc-KFVLQs7KG%2F-M9pAeEW_55UuRi5c4PV%2Fimage.png?alt=media&token=f1f88867-404b-480b-8713-223a622c6cb8)

The API library looks like this. You can choose any service you are plan to use, but we will go through the Google Sheet API.

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-M9tMDyn_-Q0BabgXnbr%2F-M9tNybPxJkD2P7Meoix%2Fimage.png?alt=media&token=fddefbd3-6186-4e9b-8f0b-4eaaa477b0d4)

Once you have selected the API and services, click the **Enable** button.

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-M9ovC5iyc-KFVLQs7KG%2F-M9pC-1aPjQe0Df1w-GD%2Fimage.png?alt=media&token=9694930c-1cce-440f-a21d-e86fdb65bcdb)

## 5. Create Credentials 

To use this API, you need credentials. Go to the credentials menu to get started.

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-M9ovC5iyc-KFVLQs7KG%2F-M9pEoElGFyFHLUh8O7K%2Fimage.png?alt=media&token=988b605b-a413-4ac6-8b3f-46990dd440bf)

Сonfigure the OAuth consent screen:

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-M9ovC5iyc-KFVLQs7KG%2F-M9pFGXvGkngH2eqeuEs%2Fimage.png?alt=media&token=f90831c1-8a32-4a65-b6b4-07563594bb16)

Choose how you want to configure and register your app, including your target users. You can only associate one app with your project. Then click **Create**.

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-M9ovC5iyc-KFVLQs7KG%2F-M9pFe7y407QD1jJIQ17%2Fimage.png?alt=media&token=ad72faf9-df7c-4267-ab57-dd7c776a460c)

Specify the application name, scroll down the page, and click **Save**.

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-M9ovC5iyc-KFVLQs7KG%2F-M9pHPRpJmic17KPXIB4%2Fimage.png?alt=media&token=340b0791-e850-4384-84d9-9b0e26916b31)

Go to the credentials menu and click **Create credentials**. Then select OAuth Client ID.

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-M9ovC5iyc-KFVLQs7KG%2F-M9pIuqzFCGZp4heRqRJ%2Fimage.png?alt=media&token=78f6ed99-c153-432e-9249-1e0e9d97ebf1)

Then you need to select the application type. In the drop-down list, select Web application. Specify name, you also can add OAuth Redirect URL, then click **Create**.  
`https://api-dev.jetadmin.io/api/create_oauth_token_complete/`

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-M9ovC5iyc-KFVLQs7KG%2F-M9pLBckoSopZ8cAwSwA%2FGIF.gif?alt=media&token=accff109-7859-407f-9e1f-cb503babf597)

Congratulations, your client ID and client secret created.

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-M9ovC5iyc-KFVLQs7KG%2F-M9pN8WS_uHq3xC33zro%2Fimage.png?alt=media&token=b9ad3410-004d-4d81-9e97-2c2263b5d5fc)

## 5. Adding resource

To complete the process of adding a resource, we need to fill in the scopes field.

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-M9ovC5iyc-KFVLQs7KG%2F-M9pOEnwzFiyAXIj1Rkx%2Fimage.png?alt=media&token=30d25f4b-6939-4c55-b4e6-17bce97eccc4)

You can find the necessary information [here](https://developers.google.com/identity/protocols/oauth2/scopes#sheets). For our case, the scopes look like this.

| Scopes | Description                       |
| :--- | :--- |
| https://www.googleapis.com/auth/spreadsheets | See, edit, create, and delete your spreadsheets in Google Drive |
| https://www.googleapis.com/auth/spreadsheets.readonly | View your Google Spreadsheets |

## Conclusion 

Congratulations! Now you are ready to authenticate with Google OAuth 2.0. If you still have any questions, please contact us for help.

