Register an application within Microsoft Entra ID
---
Version: `5.18.0` - `2024-10-15` \
Link: [Documentation on GitHub](https://github.com/freedom-manufaktur/Oktopus/blob/main/Documentation/Register%20an%20App%20within%20Entra%20ID.md)

## Step 1 
- Open the [`Microsoft Entra admin center`](https://entra.microsoft.com/#home) and log in with your credentials
  <img src="Images/EntraID/Entra_Home.png" width=2000px>

## Step 2
- Now click on `Applications` on the left side
- Click on `App registrations`
  <img src="Images/EntraID/Entra_App%20registrations.png" width=2000px>

## Step 3
- Click on `New registration`
- Choose a `Name` for the application you want to register. E.g. `whoosh Oktopus access`
- Choose `Accounts in this organizational directory only (example.com only - Single tenant)` as the `Supported account types`
- `Redirect URI` is optional and not needed 
  <img src="Images/EntraID/Entra_register%20an%20application.png" width=2000px>

## Step 4 
- Click on `Save` to register your application
- After saving you will be redirected to the `Overview` of your registered application
  <img src="Images/EntraID/Entra_App.png" width=2000px>

## Step 5 
- Click on `API permissions`
- Click on `+ Add a permission`
- The list of API's will be displayed for you to choose your permissions
  <img src="Images/EntraID/Entra_Add%20a%20permission.png" width=2000px>

## Step 6 
- Click on `Microsoft Graph`
- Click on `Delegated permissions`
- Choose your desired permissions you want to register for your application
- Click on `Add permissions` to save your changes
  <img src="Images/EntraID/Entra_MS%20Graph%20Delegated%20permissions.png" width=2000px>

## Step 7 
- Click on `Authentication`
- Under `Advanced settings` turn on `Enable the following mobile and desktop flows`
  <img src="Images/EntraID/Entra_App%20authentication.png" width=2000px>

## Step 8 
- Click on `Certificates & secrets`
- Click on `+ New client secret`
- Choose the `Description` for the client secret and when it `Expires`
- Click on `Add` to save your changes
  <img src="Images/EntraID/Entra_App%20Certificates%20%26%20secret_Add%20a%20client%20secret.png" width=2000px>

## Step 9
- Copy and save the `Value` of the secret key
  ![Entra ID Client Secret](<Images/EntraID/Entra ID Client Secret.png>)

Now you have registered an application with all required informations.