Documentation for whoosh Oktopus triggers
---
Version: `5.18.0` - `2024-10-16` \
Link: [Documentation on GitHub](https://github.com/freedom-manufaktur/Oktopus/main/Oktopus%20Triggers.md)

# Overview
This document describes the triggers available in whoosh Oktopus.

- [Azure DevOps](#-azure-devops)
- [DocuSign](#-docusign)
- [Error Handling](#-error-handling)
- [Exchange Server](#-exchange-server)
- [File System](#-file-system)
- [IMAP](#-imap)
- [Ivanti Service Manager](#-ivanti-service-manager)
- [Jira](#-jira)
- [Microsoft 365](#-microsoft-365)
- [Microsoft 365 Contacts](#-microsoft-365-contacts)
- [Ninox](#-ninox)
- [Timer](#-timer)
- [USM (Preview)](#-usm-preview)
- [Webhook](#-webhook)


## <img src="Images/TechnologyIcons/Azure%20DevOps.svg" width=32px> Azure DevOps
### Triggers
- [Work Item trigger (Webhook)](#work-item-trigger-Webhook)

#### Work Item trigger (Webhook)
Triggers when a work item created or updated webhook is received.

[:top:](#overview)


## <img src="Images/TechnologyIcons/DocuSign.svg" width=32px> DocuSign
### Triggers
- [Envelope status changed](#envelope-status-changed)

#### Envelope status changed
Triggers when the status of an envelope changes.

[:top:](#overview)


## <img src="Images/TechnologyIcons/Debug.svg" width=32px> Error Handling
### Triggers
- [Workflow failed](#workflow-failed)

#### Workflow failed
Triggers when a workflow failed with an error.

[:top:](#overview)


### <img src="Images/TechnologyIcons/ServerMail.svg" width=32px> Exchange Server
### Triggers
- [Email received](#email-received)
- [Meeting accepted](#meeting-accepted)
- [Meeting accepted tentatively](#meeting-accepted-tentatively)
- [Meeting declined](#meeting-declined)
- [Meeting response](#meeting-response)

#### Email received
Triggers whenever an email was received in the users inbox (unread).

#### Meeting accepted
Triggers whenever a meeting accepted response was received in the users inbox (unread).

#### Meeting accepted tentatively
Triggers whenever a meeting accepted tentatively response was received in the users inbox (unread).

#### Meeting declined
Triggers whenever a meeting declined response was received in the users inbox (unread).

#### Meeting response
Triggers whenever a meeting response was received in the users inbox (unread).

[:top:](#overview)


## <img src="Images/TechnologyIcons/FolderDocument.svg" width=32px> File System
### Triggers
- [Watch folder for files](#watch-folder-for-files)

#### Watch folder for files
Triggers when a file is found in a certain directory.

[:top:](#overview)


## <img src="Images/TechnologyIcons/MailCloud.svg" width=32px> IMAP
### Triggers
- [Mail recieved](#mail-recieved)

#### Mail recieved
Triggers when receving an email.

[:top:](#overview)


## <img src="Images/TechnologyIcons/Ivanti.svg" width=32px> Ivanti Service Manager
### Triggers
- [Business Object found](#business-object-found)

#### Business Object found
Triggers when a Business Object with a specific field value is found.

[:top:](#overview)


## <img src="Images/TechnologyIcons/Jira%20Software.svg" width=32px> Jira
### Triggers
- [Attachment added/deleted (Webhook)](#attachment-addeddeleted-webhook)
- [Comment created/updated (Webhook)](#Comment-createdupdated-webhook)
- [Issue created/updated (Webhook)](#issue-createdupdated-webhook)
- [Issue found (JQL)](#issue-found-jql)
- [Jira Automation (Webhook)](#jira-automation-webhook)

#### Attachment added/deleted Webhook
Triggers whenever an attachment was added or deleted with webhook notification. 

#### Comment created/updated Webhook
Triggers whenever a comment was created or updated with webhook notification.

#### Issue created/updated Webhook
Triggers whenever an issue was created or updated with webhook notification.

#### Issue found JQL
Triggers whenever an issue was found by the specified Jira query (JQL).

#### Jira Automation Webhook
Triggers whenever a notification is sent to this Webhook. The content is determinded by your Jira Automation 
settings.

[:top:](#overview)


## <img src="Images/TechnologyIcons/Microsoft%20Exchange.svg" width=32px> Microsoft 365
### Triggers
- [Mail received](#mail-received)

#### Mail received
Triggers when a mail is present in a given mailbox.

[:top:](#overview)


## <img src="Images/TechnologyIcons/Google%20Contacts.svg" width=32px> Microsoft 365 Contacts
### Triggers
- [Contact delta detected](#contact-delta-detected)

#### Contact delta detected
Triggers when a contact was created or updated.

[:top:](#overview)


## <img src="Images/TechnologyIcons/Ninox.svg" width=32px> Ninox
### Triggers
- [Record found](#record-found)

#### Record found
Triggers when a record matches a specified criteria.

##### Examples
My Field,"Max, Mustermann"

[:top:](#overview)


## <img src="Images/TechnologyIcons/Timer.svg" width=32px> Timer
### Triggers
- [CRON Schedule](#cron-schedule)
- [Interval](#interval)
- [Manual](#manual)

#### CRON Schedule
Enter a [CRON expression](https://en.wikipedia.org/wiki/Cron#CRON_expression). Time is calculated in UTC.

##### Examples
- `15 3 * * *` (daily at 03:15)
- `* * * * 1` (every monday)

#### Interval
Enter the time span between each execution (format d.hh:mm:ss).

##### Examples
`0:2:30` (2.5 minutes) or `1.0:0:0` (1 day)

#### Manual
Triggers only when the user explicitly requests execution.

[:top:](#overview)


## <img src="Images/TechnologyIcons/USM.svg" width=32px> USM (Preview)
### Triggers
- [Object found](#object-found)

#### Object found
Triggers whenever a business object matches the given criteria.

[:top:](#overview)


## <img src="Images/TechnologyIcons/Webhook.svg" width=32px> Webhook
### Triggers
- [Receive Webhook](#object-found)

#### Object found
Wait for an HTTP call to the endpoint.

[:top:](#overview)


