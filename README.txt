Creating Amazon S3 Bucket and Cognito Pool ID.

Go to https://console.aws.amazon.com/cognito/ and create a new identity pool. Make sure to enable access to unauthenticated identities and use the default roles.
Download the starter code at the last step of the wizard.
The starter code, has your Identity Pool ID. Keep this, you will need to add it to the sample later.
After above


Go to https://console.aws.amazon.com/iam/home/ and select "Roles".
Select the unauthenticated role you just created
Select "Attach Policy", then find "AmazonS3FullAccess" and attach it it to the role.
Note: This will grant users in the identity pool full access to all buckets and operations in S3. In a real app, you should restrict users to only have access to the resources they need.


Go to https://console.aws.amazon.com/s3/home
Create a bucket with a name you want.In our case it is "cloudcomputing-phase1"


Import the project as Android project into your Android Studio.
Open com.example.dayanandasaraswathi.cloud.S3Utils.java
Update "COGNITO_POOL_ID" with the value you have.
Open com.example.dayanandasaraswathi.cloud.UploadActivity.java
Open com.example.dayanandasaraswathi.cloud.Filedownload.java
Update "BUCKET_NAME" with the value you have;


You can download the newest AWS Android SDK from http://aws.amazon.com/mobile/sdk/ and copy following jars into libs directory. Include the following jars
aws-android-sdk-core-<version>.jar
extras/aws-android-sdk-cognito-<version>.jar
aws-android-sdk-s3-<version>.jar