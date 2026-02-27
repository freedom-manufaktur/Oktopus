USU Service Manager (USM) Connection Configuration
---
Version: `6.15.0` - `2026-02-26` \
Link: [Documentation on GitHub](<https://github.com/freedom-manufaktur/Oktopus/blob/main/Documentation/USU Service Manager Connection Configuration.md>)

Table of contents
---
- [1. Create an API User (Service Account)](#1-create-an-api-user-service-account)
- [2. Create a web service client](#2-create-a-web-service-client)
- [Summary](#summary)
- [Use within Oktopus](#use-within-oktopus)


# 1. Create an API User (Service Account)
> Note: This step is only necessary if you haven't already done so. If you already have a user, skip to the next chapter.

> Note: **Keycloak is supported**, but not covered in this manual.

1. Open the *USU Service Management* → *User manager*

2. Click on **Create** and enter the required fields. Here are some examples:
   - ID: `OKTOPUS`
   - First name: `Oktopus`
   - Last name: `Service`
   - Password (example): `kYMaLc9KPAk.HRRRJ9-74Kig9a!kxL`
   - Rich client usage: `Disabled`
   - Updatable by interface: `false`
   
   ![Create user](<Images/USM/User manager Create.png>)

3. Disable MFA (if enabled).

4. Navigate to *Role mapping* and select **OKTOPUS - Oktopus Service** and map **-ws.administrator** role. This allows for the easiest setup. Feel free to configure your own roles and permissions.

   ![Role mapping](<Images/USM/User manager Role mapping.png>)

5. Navigate to *Client mapping*, select **OKTOPUS - Oktopus Service** and make sure that a client (e.g. `01`) is mapped.

   ![Client mapping](<Images/USM/User mananger Client mapping.png>)

6. Assign a *Person* to the API User
   > This step is not required, but recommended as ticket creation typically requires a *Person*. We suggest naming the *Person* *Oktopus Service*, just like the user.

# 2. Create a web service client
> Note: This step is only necessary if you haven't already done so.

> Note: After making changes to a *Web service client*, you must restart *Tomcat*, as the settings are cached.

1. Navigate to the **Web service clients** catalog and click **Create**.
   
   ![Web service clients](<Images/USM/Web service clients.png>)

2. Enter the required fields. Here are some examples:
   - Name: `whoosh Oktopus`
   - Access token: `RTPu@pK-heYnN2AuGnNTP3RYdnU2Lj`
   - Description  : `Allow whoosh Oktopus to access USM. Note: Which of the Web services are actually used, is based on the workflows used inside of Oktopus.`
   - Assign the following *Web services* (the *Service ID* **must** match the USM default)
     - `ChangeObject` - Allows you to change any object.
     - `CreateObject` - Allows you to create any object.
     - `CreateTicket` - Allows you to create a ticket (a convenient wrapper around `CreateObject`).
     - `GetObject` - Allows you to get any object.
     - `GetObjects` - Allows you to get multiple objects at once (search).
     - `GetObjectTypes` - Optional: Allows Oktopus to get metadata, like a available object attributes, which is very helpful for development.
     > Note: All web services are limited to the service accounts permissions (roles).
   - Open the *Users* tab and assign `OKTOPUS` as a user.
   
   ![Web service client create](<Images/USM/Web service client Create.png>)


# Summary
As a result of the previous chapters you should have the following information at your disposal:
- Service Account Username (e.g. `OKTOPUS`)
- Service Account Password ID (e.g. `kYMaLc9KPAk.HRRRJ9-74Kig9a!kxL`)
- Web service client Access token (e.g. `RTPu@pK-heYnN2AuGnNTP3RYdnU2Lj`)


# Use within Oktopus
1. You can now enter the gathered information into **whoosh Oktopus**.

   ![Oktopus USM Connection Create](<Images/USM/Oktopus Connection Create.png>)
