Before you set to creating your tool, you will want to have your data in place. For the purposes of getting you familiar with Jet Admin, we provide a [Google Spreadsheet](https://docs.google.com/spreadsheets/d/1tTGjOz8dEfLoPwYCxkScwP68mUGSD39FW_Kfbbb0TAU/edit?usp=sharing) with customers and transactions data. 

You can use your own database of choice though \(e.g. [PostgreSQL](user-guide/integrations/postgresql-integration), [Google Sheets](user-guide/integrations/google-sheets), [Firebase](user-guide/integrations/firebase-firestore), etc.\), provided the data it stores can be used as a basic table with customers and transactions records. Below you can see an example of such table:

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MGD_WB57CE_Ex8csIKI%2F-MGEH5VUE7sXX8XaUmWr%2Fimage.png?alt=media&token=c0e0e1c1-ed2e-480d-8e25-9b7c92457d08)

Each customer with a unique `id` is associated with a list of its transactions stored in our database or in [Stripe](user-guide/integrations/stripe). Stripe stores transactions with such data columns: `amount`, `currency`, `status`, `description`, `customer`, `date`, etc.

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MFafCsXeCS0Nh_r8I5Q%2F-MFbN-N1Yg0RnQjnAKro%2Fimage.png?alt=media&token=15794643-3c2d-49b8-a64a-b7263ca134b6)

Now you are ready to create your first tool. 

{% page-ref page="getting-started/quickstart/creating-your-first-tool" %}

