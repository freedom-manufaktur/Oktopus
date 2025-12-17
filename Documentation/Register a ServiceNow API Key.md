Register a ServiceNow API Key
---
Version: `6.9.0` - `2025-12-17` \
Link: [Documentation on GitHub](<https://github.com/freedom-manufaktur/Oktopus/blob/main/Documentation/Register a ServiceNow API Key.md>)

Table of contents
---
- [Check Auth Parameters](#check-auth-parameters)
- [Create a new service account](#create-a-new-service-account)
- [Create a new API Key](#create-a-new-api-key)
- [Create a new Authentication Profile](#create-a-new-authentication-profile)
- [Add API Access Policies](#add-api-access-policies)
- [Summary](#summary)
- [Use within Oktopus](#use-within-oktopus)


# Check Auth Parameters
> Note: The required Auth Parameter exists by default. This step is only necessary to be sure.

1. Open the workspace [System Web Services → API Auth Scopes → REST API Auth Scope](https://{instance}.service-now.com/now/nav/ui/classic/params/target/sys_token_auth_parameter_list.do) and log in with your administrator credentials.
  ![Auth Parameters](<Images/ServiceNow/Auth Parameters.png>)

2. Make sure the `x-sn-apikey` (Auth Header) exists.


# Create a new service account
> Note: This step is only necessary if you haven't already done so. If you already have a service account, skip to the next chapter.

1. Open the [User Administration → Users](https://{instance}.service-now.com/now/nav/ui/classic/params/target/sys_user_list.do).
  ![Service accounts](<Images/ServiceNow/Users.png>)

1. Click **New** record

2. Give your service account a name like **Oktopus**, mark it as **active** with *Identity type* **Machine**.
   ![User Oktopus](<Images/ServiceNow/UserOktopusNew.png>)

3. Under Roles, add **admin** as role.
   > Note: For now, we need administrator role to query application metadata. You may select fewer permissions, but need to test thoroughly.

4. Click **Submit**


# Create a new API Key
> Note: This step is only necessary if you haven't already done so. If you already have a service account, skip to the next chapter.

1. Open the [System Web Services → API Access Policies → REST API Key](https://{instance}.service-now.com/now/nav/ui/classic/params/target/api_key_list.do).
  ![Users](<Images/ServiceNow/ApiKeys.png>)

2. Click **New** record

3. Give your API key a name like **Oktopus**, select the previously created user **Oktopus Service** and choose the *Auth Scope* **useraccount**.
   ![API Key Oktopus](<Images/ServiceNow/ApiKeyOktopusNew.png>)

4. Click **Submit**

5. Open the created **Oktopus** record and copy the **Token** value.
   Example: `now_YZUzn44[...]`


# Create a new Authentication Profile
> Note: This step is only necessary if you haven't already done so. If you already have a service account, skip to the next chapter.

1. Open the [System Web Services → API Access Policies → Inbound Authentication Profile](https://{instance}.service-now.com/now/nav/ui/classic/params/target/inbound_auth_profile_list.do).
  ![Auth Profiles](<Images/ServiceNow/AuthProfiles.png>)

1. Click **New** record

2. Choose **Create API Key authentication profiles**

3. Give your profile a name like **Oktopus** and select the previously created auth parameter **Header for API Key**.
   ![Auth Profile Oktopus](<Images/ServiceNow/AuthProfileOktopusNew.png>)

4. Click **Submit**


# Add API Access Policies
> Note: This step is only necessary if you haven't already done so. If you already added the required access policies, skip to the next chapter.

1. Open the [System Web Services → API Access Policies → REST API Access Policies](https://{instance}.service-now.com/now/nav/ui/classic/params/target/sys_api_access_policy_list.do).
  ![Access Policies](<Images/ServiceNow/AccessPolicies.png>)

2. Click **New** record

3. Give your policy a name like **Table API Full access** and select **Table API** as REST API and the previously created authentication profile **Oktopus**. Make sure that **Apply to all methods**, **Apply to all resources**, **Apply to all versions** and **Apply to all tables** is selected.
   ![Table API Access Policy](<Images/ServiceNow/AccessPolicyTableApiNew.png>)

4. Click **Submit**

5. Click **New** record

6. Give your policy a name like **UI API (Read-only)** and select **UI GlideRecord API** as REST API and the previously created authentication profile **Oktopus**. Make sure that **Apply to all methods** is unselected and choose **GET** (or use **Apply to all methods**), **Apply to all resources** and **Apply to all versions** is selected.
   ![UI API Access Policy](<Images/ServiceNow/AccessPolicyUIApiNew.png>)

7. Click **Submit**


# Summary
As a result of the previous chapters you should have the following information at your disposal:
- URL (e.g. `https://dev252607.service-now.com`)
- API Key (e.g. `now_YZUzn44[...]`)


# Use within Oktopus
You can now enter the gathered information into **whoosh Oktopus**.
![Oktopus ServiceNow Connection success](<Images/ServiceNow/OktopusServiceNowConnection.png>)
