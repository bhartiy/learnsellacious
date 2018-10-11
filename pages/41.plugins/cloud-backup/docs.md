---
title: 'Cloud Backup'
media_order: 'cloud.png,cloud1.png,cloud2.png,cloud3.png,cloud4.png,cloud5.png,cloud6.png,cloud7.png,cloud8.png'
visible: true
---

##### **Introduction**

Dropbox is a Cloud Backup plugin that is used to store backup your site and database to your Dropbox. To use it you need to install Cloud Backup component and Cloud Backup system plugin.

##### **Configure Dropbox API**

To store your backup to Dropbox you will need to create an APP at Dropbox. After it you will get the API keys that will be used for configuration of the Cloud Backup Extension.

**STEP-1:** First of all go to Dropbox APP console: https://www.dropbox.com/developers.

click on My apps and create app button.

![](cloud.png)

**STEP-2:** Then select Dropbox API in 'Choose an API', Full Dropbox in 'Choose the type of access you need', enter APP name and click create button.

![](cloud1.png)

**STEP-3:** Now you will get App Key and App Secret that will be used in app configuration. Then you need to enter Redirect URIs in OAuth2. This is Very Important Part as it control API permission.

Redirect URI should be like this: http://www.yourdomain.com/cloud/administrator/index.php?option=com_cloudbackup&task=config.receivetoken

![](cloud2.png)

This is done for Dropbox API. Now need to configure Cloud Backup API access.

Configure Cloud Backup API access<br>
Follow these steps to configure your Cloud Backup access:<br>
**STEP-1:** Go to admin panel of your site yourdomain.com/administrator. Go to Components > Cloud Backup. Click on Dropbox Setting.

![](cloud3.png)

**STEP-2:** Enter your App key and secret and click on Retrieve button to get Dropbox token.

![](cloud4.png)

This will redirect you to Dropbox API Request Authorization page to allow to store your files in your Dropbox.

![](cloud5.png)

Click Allow to get token.

![](cloud6.png)

Dropbox access API is configured to Cloud Backup. Now we need to create profile for backup.

##### **Configure Cloud Backup Profile**

Cloud Backup will create a backup of your site and database for that we required to create profile with required settings.<br>
STEP-1: Go to Components > Cloud Backup > Profiles.

![](cloud7.png)

Then Fill all required fields as your requirement.

![](cloud8.png)

1) Enter your profile name.<br>
2) Select backup interval from the list.<br>
3) Select the type of backup, i.e. Database only, Files only or Both Files and Database.<br>
4) Enter the name of destination folder on Cloud storage (e.g. Cloud Backup Demo).<br>
5) Files and folders that should be excluded from the backup done with this profile.<br>
Each files and folders specified here should be separated with a new line.<br>
The file and folder names should be all relative to your Joomla site root (where the main index.php
is located). For example:<br>
images<br>
cache<br>
6) Tables that should be excluded from the backup done with this profile.<br>
For example:<br>
session<br>
banners<br>
7) Then click Save & close to save profile.

Now it will take backup as you set interval on your Dropbox in given Folder.

You can also download backup files stored in Dropbox from Cloud Backups view.