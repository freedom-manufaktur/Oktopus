Register a Google Workspace Service Account
---
Version: `5.26.0` - `2025-04-02` \
Link: [Documentation on GitHub](<https://github.com/freedom-manufaktur/Oktopus/blob/main/Documentation/Register a Google Workspace Service Account.md>)

Table of contents
---
- [Create a new project](#create-a-new-project)
- [Create a new service account](#create-a-new-service-account)
- [Configure Domain-wide Delegation (access rights)](#configure-domain-wide-delegation-access-rights)
- [Summary](#summary)
- [Use within Oktopus](#use-within-oktopus)
- [Enable service account key creation](#enable-service-account-key-creation)


# Create a new project
> Note: This step is only necessary if you haven't already done so. If you already have a project, skip to the next chapter.

1. Open the [Google Cloud > Resource Manager](https://console.cloud.google.com/cloud-resource-manager) and log in with your administrator credentials.
  ![Resource Manager](<Images/GoogleWorkspace/Google Cloud Resource Manager.png>)

2. Click on **Create project**

3. Give your project a good name like **whoosh Oktopus** and hit **Create**.
   ![New project](<Images/GoogleWorkspace/Google Cloud Resource Manager - New project.png>)


# Create a new service account
> Note: This step is only necessary if you haven't already done so. If you already have a service account, skip to the next chapter.

1. Open the [Google Cloud > IAM & Admin > Service accounts](https://console.cloud.google.com/iam-admin/serviceaccounts) and make sure the correct project (e.g. `whoosh Oktopus`) is selected.
  ![Service accounts](<Images/GoogleWorkspace/Google Cloud IAM Service Accounts.png>)

2. Click **Create service account**

3. Give your service account a name like **whoosh oktopus** and hit **Create and continue**.

4. Skip **Grant this service account access to project** and **Grant users access to this service account** and hit **Done**.
   ![Account create done](<Images/GoogleWorkspace/Google Cloud IAM Service Accounts - Create - Done.png>)

5. Open the created service account and write down the following information
   - Email (e.g. `whoosh-oktopus@whoosh-oktopus.iam.gserviceaccount.com`)
   - Unique ID / Client ID (e.g. `102673634169041257612`)
   ![Service Account Details](<Images/GoogleWorkspace/Google Cloud IAM Service Accounts - Details.png>)

6. Open the tab **Keys** and click **Add key > Create new key**.
   ![Create new key](<Images/GoogleWorkspace/Google Cloud IAM Service Accounts - Details - Keys add.png>)

7. Choose **JSON** and click **Create**.
   ![JSON Key](<Images/GoogleWorkspace/Google Cloud IAM Service Accounts - Details - Keys add JSON.png>)

8. If you are presented with `Service account key creation is disabled` and error message `The organization policy constraint 'iam.disableServiceAccountKeyCreation' is enforced on your organization.` then please follow the instructions on how to [enable service account key creation](#enable-service-account-key-creation) and retry the key creation.

9. Save the downloaded `.json` file (e.g. `whoosh-oktopus-f56aaf1480f8.json`).
   ![Successful key creation](<Images/GoogleWorkspace/Google Cloud IAM Service Accounts - Details - Keys add JSON success.png>)


# Configure Domain-wide Delegation (access rights)

1. Open the [Google Admin > Security > API Controls > Domain-wide Delegation](https://admin.google.com/ac/owl/domainwidedelegation) and make sure the correct project (e.g. `whoosh Oktopus`) is selected.

2. Under **API clients** click **Add new**.

3. Enter the *Unique ID / Client ID* from the previous chapter (e.g. `102673634169041257612`).

4. Choose which access rights (scopes) you want to grant. All available scopes can be found [here](https://developers.google.com/identity/protocols/oauth2/scopes).\
   Scopes recommended for Oktopus are (you may choose different ones as you like):
   - `https://www.googleapis.com/auth/drive.readonly`: Read-only access to Google Drive.
   - `https://www.googleapis.com/auth/drive`: Read and write access to Google Drive.
   - `https://www.googleapis.com/auth/admin.directory.user.readonly`: Read-only access to Google Admin Console.
   > Note: You should always follow the principle of least privilege (PoLP).

   ![Add a new client ID](<Images/GoogleWorkspace/Google Admin Domain Wide Delegation - Add client.png>)

5. Finally click **Authorize**.
   ![Client ID overview](<Images/GoogleWorkspace/Google Admin Domain Wide Delegation - Client.png>)


# Summary
As a result of the previous chapters you should have the following information at your disposal:
- Service Account Email (e.g. `whoosh-oktopus@whoosh-oktopus.iam.gserviceaccount.com`)
- Service Account Unique ID (e.g. `102673634169041257612`)
- Service Account Key (e.g. `whoosh-oktopus-f56aaf1480f8.json`)


# Use within Oktopus
1. You can now enter the gathered information into **whoosh Oktopus**.
   ![Oktopus Google Connection Create](<Images/GoogleWorkspace/Oktopus Google Connection Create.png>)

2. The connection should test successfully
   ![Oktopus Google Connection success](<Images/GoogleWorkspace/Oktopus Google Connection Success.png>)


# Enable service account key creation
You only need this if you need to change `iam.disableServiceAccountKeyCreation` policy.

1. Open the [Google Cloud > IAM & Admin > IAM](https://console.cloud.google.com/iam-admin/iam) and make sure that your **organisation** is selected.

2. Make sure that your current admin account has the `Organization Policy Administrator` role
   ![Policy Administrator](<Images/GoogleWorkspace/Google Cloud IAM Policy Administrator.png>)

3. Open the [Google Cloud > IAM & Admin > Organization policies](https://console.cloud.google.com/iam-admin/orgpolicies/list) and make sure the correct project (e.g. `whoosh Oktopus`) is selected.

4. Filter for `iam.disableServiceAccountKeyCreation`
   ![Disable Service Account Key policies](<Images/GoogleWorkspace/Google Cloud IAM Policies - Disable Service Account Key.png>)

5. Make sure that the state of all policies (2) is set to **Inactive**.
   ![Override policy](<Images/GoogleWorkspace/Google Cloud IAM Policies - Disable Service Account Key Override.png>)

You may now continue with your service account key creation.