Register an Exchange Online App within Microsoft Entra ID
---
Version: `5.22.0` - `2025-02-18` \
Link: [Documentation on GitHub](<https://github.com/freedom-manufaktur/Oktopus/blob/main/Documentation/Register an Exchange Online App within Entra ID.md>)

## Register a new application
1.  Open the [Microsoft Entra admin center](https://entra.microsoft.com/#home) and sign in with your credentials

2.  Under **Entra ID**, on the left side, click **App registrations**.
    ![Entra ID App registrations](<Images/EntraID/App registrations.png>)

3.  Click on `New registration`
    - Choose a `Name` for the application you want to register. E.g. `whoosh Oktopus Exchange Online access`
    - Choose `Accounts in this organizational directory only (example.com only - Single tenant)` as the `Supported account types`
    - Under `Redirect URI` choose `Public client/native (mobile & desktop)` with the URL `https://login.microsoftonline.com/common/oauth2/nativeclient`
  
    ![Entra ID App registration](<Images/ExchangeOnlineApp/Entra ID App registration.png>)

4.  Click **Register** to register your application.
    After saving you will be redirected to the *Overview* of your registered application
    ![Entra ID App Overview](<Images/ExchangeOnlineApp/Entra ID App Overview.png>)

5. Write down the **Application ID** (e.g. `70af00a0-e4df-48b8-957f-a4e2f75a5f7e`) and **Tenant ID** (e.g. `9776b2ed-e415-439d-9582-85719af85979`).

## Configure your application
1.  Under **Manifest** change `requiredResourceAccess` to the following
    ```
    "requiredResourceAccess": [
    	{
    		"resourceAppId": "00000002-0000-0ff1-ce00-000000000000",
    		"resourceAccess": [
    			{
    				"id": "dc890d15-9560-4a4c-9b7f-a736ec74ec40",
    				"type": "Role"
    			}
    		]
    	}
    ]
    ```
2.  Click **Save**
    ![Exchange App Manifest](<Images/ExchangeOnlineApp/Exchange App Manifest.png>)

3.  Under **API permissions** use **Grant admin consent for example.com** make sure all permissions have admin consent.

4.  Under **Certificates & secrets** → **Client secrets** add a client secret and write it down (e.g. `4lf[...]`).\
    ![Entra ID Client Secret](<Images/EntraID/Entra ID Client Secret.png>)

## Summary
As a result of this chapter you should have the following information at your disposal:
* Entra ID Application ID (e.g. `70af00a0-e4df-48b8-957f-a4e2f75a5f7e`)
* Entra ID Tenant ID (e.g. `9776b2ed-e415-439d-9582-85719af85979`)
* Entra ID Client Secret (e.g. `4lf[...]`)

Now you have registered an application with all required informations.

## Support
For more information on the topic, please read the Microsoft documentation [Authenticate an EWS application by using OAuth](https://learn.microsoft.com/en-us/exchange/client-developer/exchange-web-services/how-to-authenticate-an-ews-application-by-using-oauth).