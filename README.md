
# Installation Guide

This guide will walk you through the steps to set up and use the Google Drive Uploader PHP script to upload files and folders to Google Drive.

## Prerequisites

Before proceeding, ensure you have the following installed and configured:

- PHP 8
- Composer


## Installation Steps

1. **Clone the Repository:**

```bash
git clone https://github.com/ciprianoancia/gdriveuploader.git
```
Navigate to the Project Directory:

```bash
cd gdriveuploader
```
Install Dependencies:

```bash
composer install
```


## Create Google API Credentials:

### Step 1: Create a Project
Go to the Google Developer Console. https://console.developers.google.com/
Create a new project or select an existing one.

### Step 2: Enable Google Drive API
Navigate to the Library:

Click on the menu icon ☰ and select "APIs & Services" > "Library".
Search for "Google Drive API".

Click on "Google Drive API".

Click "Enable" to enable the API for your project.

### Step 3: Create Credentials
Go to the Credentials Page:

Click on the menu icon ☰ and select "APIs & Services" > "Credentials".
Click on "Create Credentials" > "Service Account".

Fill in the necessary details (Service account name, ID, etc.).
Choose the role as per your requirements (e.g., Project > Editor for full access).
For "Key type", select "JSON" and click "Create".
This will download a JSON file containing your service account credentials. Keep this file secure.

### Step 4: Save the JSON Credentials in Home folder
Save the downloaded JSON file containing your service account credentials (client_secret.json) into  ~/.auth.json
Create also an empty .token.json file in the same home folder 

### Step 5: Share Folder with Service Account
Locate the folder in Google Drive where you want to upload files. (Remember to copy id of the folder from the address bar for later use)
Right-click on the folder and choose "Share".
Enter the email address found in the service account JSON file (e.g., example@your-project-id.iam.gserviceaccount.com).
Grant necessary permissions (e.g., edit, view) to the service account.

### Step 6: Configure gdclient script: 


```php

//location of auth.json
$authConfigPath = '';

//location of your token.json
$tokenFilePath = '';

//the folder from your local machine that should be syncronised
$sourceFolderPath = '';

//the id of your Google drive folder
$destinationFolderId = '';

```

Please ping me if you have any questions

