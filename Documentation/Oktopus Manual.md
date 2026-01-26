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
1. In the *Workflow Studio*, choose *Import*.
2. Upload the previously exported `.json` file.
3. Review configurations (for example connections and credentials) and adjust them as necessary.

## Export
1. Open the *Workflow Studio* and select the workflow you want to export.
2. Click *Export* and save the resulting `.json` file.

Note: Imports may miss dependencies such as references to credentials or external services. Verify these after import and test the workflow in a safe environment.

# Activate user management
In many installations, user management is disabled by default. To enable and configure it:

1. Sign in as an administrator to the *Server Settings*.
2. Open the settings for the target environment and go to *Security / Users*.
3. Enable *User management*.
4. Create roles and assign permissions (for example `Administrator`, `Editor`, `Viewer`).
5. Optional: Configure external identity providers (e.g. Microsoft Entra ID) under *Authentication*.

Note: After enabling user management, create at least one administrator account to ensure access control.

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
