---
title: Upload offline account data for reporting and simulations
description: Learn how to upload offline account data manually or to an [!DNL Amazon] [!DNL S3] bucket for reporting and simulation support. Log files track the progress of upload jobs.
---
# Upload offline account data for reporting and simulations

*Advertisers who are enabled for account data uploads*

Upload campaign content and offline cost, click, and conversion data for an account without API support for reporting and performance simulations.

You can track the progress of your upload jobs using the [!UICONTROL Upload Logs] feature:

* View a list of each file uploaded for the account. Information about each file upload job includes the filename, upload channel (*[!UICONTROL Cloud Storage]* or *[!UICONTROL Drag & Drop]*), the sync date and status, and reasons for incomplete uploads. 

* Download a file with the account entities and related metrics that were uploaded for any job. The files are in comma-separated values (CSV) format.

## Upload account data manually

You can populate an account with campaign content and cost, click, and conversion data by manually uploading the data in a file.

<!--
See "XXX" for information about supported ad networks and account structures.

[supported ad networks and campaign types](/help/search-social-commerce/introduction/supported-inventory.md)
-->

1. In the main menu, click **[!UICONTROL Setup]** \> **[!UICONTROL Accounts]**.

1. Do either of the following:

   * (From the [!UICONTROL Accounts] view):
   
     1. Select the check box next to the account name, and then click **[!UICONTROL Upload]** in the bulk actions toolbar.

     1. Either drag a file into the box or click **[!UICONTROL Browse Files]** and choose a file from your device or network.

     1. Click **[!UICONTROL Upload Files]**.

   * (From the account settings):
   
     1. Select the account in either of the following ways:
     
        * Hold the cursor over the account name, click **...**, and then click **[!UICONTROL Edit]**.
        
        * Select the check box next to the account name, and then click **[!UICONTROL Edit]** in the bulk actions toolbar.
        
     1. Click the **[!UICONTROL Upload File]** tab.
     
     1. Either drag a file into the box or click **[!UICONTROL Browse Files]** and choose a file from your device or network.

     1. Click **[!UICONTROL Save]**.

# Upload account data to an [!DNL Amazon] [!DNL S3] bucket {#data-upload-s3}

You can populate an account with campaign content and cost, click, and conversion data by uploading the data to a Search, Social, & Commerce-assigned folder in an [!DNL Amazon Web Services] (AWS) [!DNL Simple Storage Service] ([!DNL S3]) bucket.

<!--
See "XXX" for information about supported ad networks and account structures.

[supported ad networks and campaign types](/help/search-social-commerce/introduction/supported-inventory.md)
-->

>[!PREREQUISITES]
>
>* Contact your Adobe Account Team to enable account data uploads for your Search, Social, & Commerce advertiser account. The team will facilitate the creation of an organization-specific folder in an [!DNL S3] bucket, and they'll let you know when it's completed.<!-- Add more context about the bucket we'll use here or in the intro. Do we have one bucket (potentially with multiple folders) per client, or do we share them (if so, do we need to state how in docs? -->
>* Retrieve the [!DNL S3] cloud storage path, access key ID, and secret access key for your account. The same access key ID and secret access key are used for all of the organization's data-upload <!-- naming convention?--> accounts.

1. In the main menu, click **[!UICONTROL Setup]** \> **[!UICONTROL Accounts]**.

1. Do either of the following:

   * (From the [!UICONTROL Accounts] view):
   
     1. Select the check box next to the account name, and then click **[!UICONTROL Upload]** in the bulk actions toolbar.

     1. In the [!UICONTROL Cloud Storage Link] box, click **[!UICONTROL Go to the Link]**.
     
     1. Click **[!UICONTROL Show Access Key and Secret]**.
     
     1. Next to the [!UICONTROL Storage Link] field, click **[!UICONTROL Copy]** to copy the link to your clipboard, and store the link in a secure place.
     
     1. Similarly, copy and securely store the [!UICONTROL Access Key] and the [!UICONTROL Secret Key] values.
     
     1. Click **[!UICONTROL Done]**.

   * (From the account settings):
   
     1. Select the account in either of the following ways:
     
        * Hold the cursor over the account name, click **...**, and then click **[!UICONTROL Edit]**.
        
        * Select the check box next to the account name, and then click **[!UICONTROL Edit]** in the bulk actions toolbar.
        
     1. Click the **[!UICONTROL Upload File]** tab.
     
     1. In the [!UICONTROL Cloud Storage Link] box, click **[!UICONTROL Go to the Link]**.
     
     1. Click **[!UICONTROL Show Access Key and Secret]**.
     
     1. Next to the [!UICONTROL Storage Link] field, click **[!UICONTROL Copy]** to copy the link to your clipboard, and store the link in a secure place.
     
     1. Similarly, copy and securely store the [!UICONTROL Access Key] and the [!UICONTROL Secret Key] values.
     
     1. Click **[!UICONTROL Done]**.

     1. Click **[!UICONTROL Save]**.

1. (Once per organization) Set up your local AWS environment:

   1. Download and install [!DNL AWS Command Line Interface] (AWS CLI), from the following location: [https://docs.aws.amazon.com/cli/latest/userguide/getting-started-install.html](https://docs.aws.amazon.com/cli/latest/userguide/getting-started-install.html).

   1. Configure your AWS credentials:

      1. Create a plaintext file and name it `~/.aws/credentials` (without a file extension).
      
      1. Open the file in any text editor and enter the organization's access key ID and secret access key as follows:
      
         ```
         [default]
         aws_access_key_id = <Access key copied in Step 2>
         aws_secret_access_key = <Secret key copied in Step 2>
         ```

1. Download your account data report from the ad network and save it.

1. In AWS CLI, run the following command to upload your account data to your [!DNL S3] cloud location.

   ```
   aws s3 cp <local-report-file-location <S3-cloud-location-associated-with-your-account>
   ```

   Example:  `aws s3 cp filename.txt s3://cloud-location/`

## View a log of uploaded account data files

1. In the main menu, click **[!UICONTROL Setup]** \> **[!UICONTROL Accounts]**.

1. Hold the cursor over the account name, click **...**, and then click **[!UICONTROL Upload Logs]**.

1. (Optional) To download the data for an uploaded file, click ![Download](/help/search-social-commerce/assets/download.png "Download") in the [!UICONTROL Download] column and download the file according to your browser's normal procedure.

## Required data

The data must follow the data requirements for the ad network. The data fields for each entity may vary by ad network.
