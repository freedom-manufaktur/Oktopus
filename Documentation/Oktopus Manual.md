whoosh Oktopus Manual
---
Version: `6.11.0` - `2026-01-26` \
Author: [oktopus@freedom-manufaktur.com](mailto:oktopus@freedom-manufaktur.com) \
Link: [Documentation on GitHub](<https://github.com/freedom-manufaktur/Oktopus/blob/main/Documentation/Oktopus Manual.md>)

Table of contents
---
<!--TOC-->
- [Introduction](#introduction)
- [Import / export workflows](#import--export-workflows)
  - [Import](#import)
  - [Export](#export)
- [Activate user management](#activate-user-management)
- [Manage Oktopus API key](#manage-oktopus-api-key)
<!--/TOC-->

# Introduction
This guide explains the day-to-day use of *whoosh Oktopus* and describes key administrative tasks.

# Import / export workflows
Workflows can be imported and exported to support migrations, backups, or sharing between instances.

## Import
1. In the *Workflow Studio* navigate to the *Workflows* page.
2. Click the *Import workflow* button.
3. Select the previously exported `.json` file(s).
4. This will import all selected files as workflows.
   > Note: If one of the workflows already exists (by name), you will be asked whether you want to overwrite the existing ones or rename them on import.
5. Review workflow configuration. Workflows exports do **not** contain any sensitive connection credentials (only the name). If a connection with the same name already exists, it will be selected automatically, if not you must update all steps with missing connections.

## Export
1. In the *Workflow Studio* navigate to the *Workflows* page.
2. Select any number of workflows or workflow groups.
3. Open the context menu und choose *Export*.
4. Save the resulting `.json` file(s) in any folder of your choosing.

# Activate user management
When installing Oktopus for the first time, user management is disabled. Any user with access to the Oktopus Server endpoint can sign in as **anonymous user**. As one of the first steps your **should** enable user management and protect your Oktopus instance against unauthorized access.

1. Sign in to the *Workflow Studio* as anonymous user.
2. Navigate to the *Settings* page.
3. Create a new user with the role of administrator.
4. Click the **Sign in as administrator to enable** button. You should be signed out and back at the sign in page.
5. Sign in as the user you have previously created.
6. Click **Enable** in the user management section.

# Manage Oktopus API key
*Oktopus* provides an API for automation and integration with external systems. Manage API keys as follows:

1. In the Workflow Studio or Server Settings, navigate to *API / Keys*.
2. Create a new key and give it a descriptive name (e.g. `CI/CD Access`, `ServiceNow Integration`).
3. Select the required permissions and set an expiration if needed.
4. Copy the key securely and store it in a safe location. After closing the dialog the key is usually not fully visible again.
5. Keys can be disabled or deleted at any time if needed.

Security tip: Use short-lived keys for integrations and rotate keys regularly.

---
If you have further questions about using *whoosh Oktopus*, contact us at [oktopus@freedom-manufaktur.com](mailto:oktopus@freedom-manufaktur.com).
