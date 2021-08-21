In order to be able to use Amazon S3 storage in Jet, you need to set it up. Follow the steps below to successfully integrate S3 with Jet.

## Making a new S3 IAM user

Head over to [IAM](https://console.aws.amazon.com/iam/home), add a new user and call it `jetadmin-uploader`, enable _**programmatic access**_ only. 

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MVqqN468_usz2PipzN5%2F-MW-0ukG5AJm7EGGyiwT%2FGIF196.gif?alt=media&token=80732e20-1ae0-4d1b-8966-5b4338305874)

Hit _**next**_ to grant the account permissions. The easiest way is granting full S3 permissions, but if you want, you can further restrict the permissions. You'll need to create a new policy, then attach the policy to the created user.

## Configuring Permissions

{% hint style="info" %}
### IAM Permissions: best practices

While the simplest way to get JetAdmin working with S3 is to give JetAdmin full S3 access, the best practice is to restrict access to buckets on an as-needed basis.
{% endhint %}

Here's an example JSON IAM policy: you'll need to change the `YOUR_STATEMENT_ID` variable, as well as the `YOUR_BUCKET_NAME_HERE` variable. 

{% hint style="info" %}
Keep both the `YOUR_BUCKET_NAME_HERE/*` and `YOUR_BUCKET_NAME_HERE` - as they're both required.
{% endhint %}

```javascript
{
    "Version": "2012-10-17",
    "Statement": [
        {
            "Effect": "Allow",
            "Action": [
                "s3:GetBucketAcl",
                "s3:GetBucketCORS",
                "s3:GetBucketLocation",
                "s3:GetBucketLogging",
                "s3:GetBucketNotification",
                "s3:GetBucketPolicy",
                "s3:GetBucketWebsite",
                "s3:GetObject",
                "s3:GetObjectAcl",
                "s3:GetObjectVersion",
                "s3:GetObjectVersionAcl",
                "s3:PutObject",
                "s3:PutObjectAcl",
                "s3:PutObjectTagging",
                "s3:PutObjectVersionAcl",
                "s3:PutObjectVersionTagging"
            ],
            "Resource": [
                "arn:aws:s3:::BUCKET_NAME",
                "arn:aws:s3:::BUCKET_NAME/*"
            ]
        }
    ]
}
```

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MW-8gVUDc2IipmrzWe1%2F-MW-CU6I1hxGkyu7ckn-%2FGIF198.gif?alt=media&token=087fd941-7cce-4934-bbfe-c03e78a5412d)

{% hint style="success" %}
**Minimum Grants for Uploading Files:**

```javascript
"s3:GetBucketLocation"
"s3:PutObject"
```
{% endhint %}

## Configuring CORS

Since we upload directly from your browser, you'll need to configure [CORS](https://docs.aws.amazon.com/AmazonS3/latest/dev/cors.html). Open up the S3 bucket, click the Permissions tab, and then click CORS configuration, and paste in the following JSON, which will let JetAdmin upload directly into your S3 bucket from the browser.

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MW-8gVUDc2IipmrzWe1%2F-MW-E0SWdeA38kEFUiSC%2FGIF199.gif?alt=media&token=e8f8c6eb-c254-48c3-8080-080a762d41df)

```javascript
[
  {
    "AllowedOrigins": [
    "https://*.jetadmin.io"
    ],
    "AllowedMethods": [
    "PUT",
    "POST",
    "DELETE"
    ],
    "AllowedHeaders": ["*"]
  },
  {
    "AllowedOrigins": ["*"],
    "AllowedMethods": ["GET"]
  }
]
```

## Integrate S3 with Jet

Select Amazon S3 from the list of available storages and enter the `access key` and `secret` generated for your IAM user obtained [here](https://console.aws.amazon.com/iam/home#/users). Jet will automatically get a list of all your buckets and integrate each bucket with Jet.

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MVqqN468_usz2PipzN5%2F-MW-5ae0GKlM9H17zU6T%2Fimage.png?alt=media&token=70f670ec-bcd8-43e9-a571-04df8019e716)

Once you have integrated S3 with Jet, you will see a Storage File Viewer that you'll use to access your data.

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MW-6hpo34t5teVdGCcb%2F-MW-8SxZZWejzGZUrxw_%2FGIF197.gif?alt=media&token=238f7147-d861-48b5-afc6-cdf3d526c1fe)

