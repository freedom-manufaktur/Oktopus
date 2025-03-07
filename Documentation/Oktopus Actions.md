List of whoosh Oktopus actions
---
Version: `5.23.0` - `2025-03-07` \
Link: [Documentation on GitHub](https://github.com/freedom-manufaktur/Oktopus/blob/main/Documentation/Oktopus%20Actions.md)

# Technologies
- [Active Directory](#-active-Directory)
- [Azure DevOps](#-azure-devops)
- [CSV](#-csv)
- [Debug](#-debug)
- [DocuSign](#-docusign)
- [Exchange Server](#-exchange-server)
- [File compression](#-file-compression)
- [File System](#-file-system)
- [Google Admin Console](#-google-admin-console)
- [Google Drive](#-google-drive)
- [HTTP](#-http)
- [IGEL Technology](#-igel-technology)
- [Image](#-image)
- [IMAP](#-imap)
- [Ivanti Service Manager](#-ivanti-neurons-for-itsm--ivanti-service-manager-ism)
- [Jira](#-jira)
- [JSON](#-json)
- [LeanIX](#-leanix)
- [LexOffice](#) - *Work in progress*
- [Mail](#-mail)
- [Microsoft 365](#-microsoft-365)
- [Microsoft 365 Contacts](#-microsoft-365-contacts)
- [Microsoft Excel](#-microsoft-excel)
- [Microsoft OneDrive / SharePoint](#-microsoft-onedrive--sharepoint)
- [Microsoft SQL Server](#-microsoft-sql-server)
- [Microsoft Teams](#-microsoft-teams)
- [Microsoft Word](#-microsoft-word)
- [NetBox](#-netbox)
- [Ninox](#-ninox)
- [Oktopus](#-oktopus)
- [PDF](#-pdf)
- [Power BI](#-power-bi)
- [ReyVentory Data Hub](#-reyventory-data-hub)
- [Shopware](#-shopware)
- [SMAX](#-smax)
- [Text](#-text)
- [Timer](#-timer)
- [Timewax](#) - *Work in progress*
- [USM (Preview)](#-usm-preview)
- [Webhook](#-webhook)


## <img src="Images/TechnologyIcons/Active%20Directory.svg" width="24"> Active Directory
### Actions
- [Add a principal to groups](#add-a-principal-to-groups)
- [Create User](#create-user)
- [Delete principal](#delete-principal)
- [Find User](#find-user)
- [Remove a principal from groups](#remove-a-principal-from-groups)
- [Reset user password](#reset-user-password)
- [Update User](#update-user)

#### Add a principal to groups
Add a User, Group or Computer to any number of groups.

#### Create User
Create a new user account

#### Delete principal
Delete a User, Group or Computer.

#### Find User
Finds a user by name.

#### Remove a principal from groups
Remove a User, Group or Computer from any number of groups.

#### Reset user password
Resets a users password.

#### Update User
Update a User With a selection of properties.

[⬆️ Back to top](#technologies)


## <img src="Images/TechnologyIcons/Azure%20DevOps.svg" width="24"> Azure DevOps
### Actions
- [Add attachments to Work Item](#add-attachments-to-work-item)
- [Create Work Item](#create-work-item)
- [Delete build(s)](#delete-builds)
- [Get Work Item](#get-work-item)
- [List builds](#list-builds)
- [Update Work Item](#update-work-item)
- [Users: Add User](#users-add-user)
- [Users: List Users](#users-list-users)
- [Users: Remove User](#users-remove-user)

#### Add attachments to Work Item
Adds any number of attachments to a Work Item.

#### Create Work Item
Create a new work item.

#### Delete build(s)
Delete one or more builds by ID.

#### Get Work Item
Get work item by ID.

#### List builds
List all builds.

#### Update Work Item
Update a work item.

#### Users: Add User
Adds a user to an organization.

#### Users: List Users
Lists all users in an organization.

#### Users: Remove User
Removes a user from an organization.

[⬆️ Back to top](#technologies)


## <img src="Images/TechnologyIcons/Text.svg" width="24"> CSV
### Actions
- [Parse CSV text](#parse-csv-text)

#### Parse CSV text
Parses the given CSV text and stores the object result.

[⬆️ Back to top](#technologies)


## <img src="Images/TechnologyIcons/Debug.svg" width="24"> Debug
### Actions
- [Print Expression](#print-expression)

#### Print Expression
Prints the expression to the log file.

[⬆️ Back to top](#technologies)

## <img src="Images/TechnologyIcons/DocuSign.svg" width="24"> DocuSign
### Actions
- [Get envelope](#get-envelope)
- [Get envelope audit events](#get-envelope-audit-events)
- [Sign Document](#sign-document)

#### Get envelope
Get information about a document signing request (envelope).

#### Get envelope audit events
Get the audit events of a document signing request (envelope).

#### Sign Document
Notify People about a document signing request.

[⬆️ Back to top](#technologies)


## <img src="Images/TechnologyIcons/ServerMail.svg" width="24"> Exchange Server
### Actions
- [Cancel Meeting](#cancel-meeting)
- [Create Meeting](#create-meeting)
- [Delete item](#delete-item)
- [Mark email as read](#mark-email-as-read)
- [Move item](#move-item)
- [Send Email](#send-email)
- [Update Meeting](#update-meeting)

#### Cancel Meeting
Cancel an existing meeting.

#### Create Meeting
Send a meeting invitation.

#### Delete item
Deletes an item (mail, appointment, meeting).

#### Mark email as read
Marks an email as read.

#### Move item
Moves an item (mail, appointment, meeting) to a different folder.

#### Send Email
Sends an email.

#### Update Meeting
Update an existing meeting.

[⬆️ Back to top](#technologies)


## <img src="Images/TechnologyIcons/Compress.svg" width="24"> File compression
### Actions
- [Create archive](#create-archive)

#### Create archive
Creates an archive file (typically .zip).

[⬆️ Back to top](#technologies)


## <img src="Images/TechnologyIcons/FolderDocument.svg" width="24"> File System
### Actions
- [Copy file](#copy-file)
- [Delete file](#delete-file)
- [Move file](#move-file)
- [Read file](#read-file)
- [Save file](#save-file)

#### Copy file
Copies a file from one location to another.

#### Delete file
Delete a file.

#### Move file
Moves a file from one location to another.

#### Read file
Reads the content of a file to a variable.

#### Save file
Writes the given file variable or data to a file.

[⬆️ Back to top](#technologies)


## <img src="Images/TechnologyIcons/GoogleAdminConsole.svg" width="24"> Google Admin Console
### Actions
- [Get a User](#google-admin---get-a-user)

#### Google Admin - Get a User
Gets the information about a user.

[⬆️ Back to top](#technologies)


## <img src="Images/TechnologyIcons/GoogleDrive.svg" width="24"> Google Drive
### Actions
- [Get drive](#google-drive---get-drive)
- [Find drives](#google-drive---find-drives)
- [Get file](#google-drive---get-file)
- [Download file](#google-drive---download-file)
- [Find files/folders](#google-drive---find-filesfolders)

#### Google Drive - Get drive
Gets a drive by name.

#### Google Drive - Find drives
Finds all drives by query.

#### Google Drive - Get file
Gets a file by name.

#### Google Drive - Download file
Download a file.
Gets a file by name.

#### Google Drive - Find files/folders
Finds all files and folders by query.

[⬆️ Back to top](#technologies)


## <img src="Images/TechnologyIcons/Http.svg" width="24"> HTTP
### Actions
- [Send HTTP request](#send-http-request)
- [Send HTTP request (preview)](#send-http-request-preview)

#### Send HTTP request
Call any HTTP endpoint.

#### Send HTTP request (preview)
Call any HTTP endpoint multiple times.
Note: This is a preview step, wich is not production ready and will change in th efuture.

[⬆️ Back to top](#technologies)


## <img src="Images/TechnologyIcons/Igel.svg" width="24"> IGEL Technology
### Actions
- [Get firmwares](#get-firmwares)
- [Get thin clients](#get-thin-clients)

#### Get firmwares
Get all firmwares.

#### Get thin clients
Get all thin clients.

[⬆️ Back to top](#technologies)


## <img src="Images/TechnologyIcons/PhotoLandscape.svg" width="24"> Image

### Actions
- [Convert image](#convert-image)

#### Convert image
Converts a number of images to a target format.

[⬆️ Back to top](#technologies)


## <img src="Images/TechnologyIcons/MailCloud.svg" width="24"> IMAP
### Actions
- [Delete mail](#delete-mail)
- [Move mail](#move-mail)

#### Delete mail
Delete an email.

#### Move mail
Move an email to a different folder.

[⬆️ Back to top](#technologies)


## <img src="Images/TechnologyIcons/Ivanti.svg" width="24"> Ivanti Neurons for ITSM / Ivanti Service Manager (ISM)
### Actions
- [Add attachment](#add-attachment)
- [Create Business Object](#create-business-object)
- [Create or update Business Obejct(s)](#create-or-update-business-obejcts)
- [Delete Busines Object](#delete-busines-object)
- [Find Business Objects (by field)](#find-business-objects-by-field)
- [Find Business Objects (by query)](#find-business-objects-by-query)
- [Find Employees](#find-employees)
- [Get attachment](#get-attachment)
- [Get Business Object (by field)](#get-business-object-by-field)
- [Get Business Object (by query)](#get-business-object-by-query)
- [Get Business Object (by field values)](#get-business-object-by-field-values)
- [Get request offering](#get-request-offering)
- [Update Business Object](#update-business-object)

#### Add attachment
Adds an attachment to a specific Business Object.

#### Create Business Object
Creates a new Business Object.

#### Create or update Business Obejct(s)
Create or update (upsert) a Single Business Object or many at once.

#### Delete Busines Object
Deletes a Business Object.

#### Find Business Objects (by field)
Finds Business Objects With a specific field value.

#### Find Business Objects (by query)
Finds Business Objects With a combination of conditions.

#### Find Employees
Finds employee objects (Employee#) by ID. This is a handy shortcut when transforming LoginlD to ReclD or ice versa.

#### Get attachment
Gets an attachment Object and downloads the content.

#### Get Business Object (by field)
Gets the oldest Business Object With a specific field value.

#### Get Business Object (by query)
Gets the oldest Business Object With a combination of conditions.

#### Get Business Object (by field values)
Gets the oldest Business Objects for each specific field value.

#### Get request offering
Get the request data - including parameters - associated with a service request (ServiceReq).

#### Update Business Object
Updates a Business Object.

[⬆️ Back to top](#technologies)


## <img src="Images/TechnologyIcons/Jira%20Software.svg" width="24"> Jira
### Actions
- [Add Attachment](#add-attachment)
- [Add Comment](#add-comment)
- [Add web link](#add-web-link)
- [Create Issue](#create-issue)
- [Delete Issue](#delete-issue)
- [Do Transition](#do-transition)
- [Find Issue (JQL)](#find-issue-jql)
- [Find User](#find-user)
- [Get Attachment](#get-attachment)
- [Get Issue](#get-issue)
- [Get Issues](#get-issues)
- [Get Project Roles](#get-project-roles)
- [Set Project Role users](#set-project-role-users)
- [Trigger issue updated](#trigger-issue-updated)
- [Update Comment](#update-comment)
- [Update Issue](#update-issue)

#### Add Attachment
Adds a new attachment to an issue.

#### Add Comment
Adds a new comment to an issue.

#### Add web link
Adds a new link to a specified URL.

#### Create Issue
Creates a new issue.

#### Delete Issue
Deletes an existing issue.

#### Do Transition
Transition an issue from one State to the next. Also allows multiple transitions at once.

#### Find Issue (JQL)
Get the first issue that matches the specified Jira query (JQL).

#### Find User
Finds a user by ID, email or name.

#### Get Attachment
Get a specific attachment.

#### Get Issue
Get a specific issue.

#### Get Issues
Get specific issues.

#### Get Project Roles
Gets all available project roles and their users.

#### Set Project Role users
Replaces all assigned users and groups With a new set of users/groups.

#### Trigger issue updated
Triggers an Oktopus workflow With 'Issue created/updated (Webhook) trigger.

#### Update Comment
Updates an existing comment.

#### Update Issue
Updates an existing issue.

[⬆️ Back to top](#technologies)


## <img src="Images/TechnologyIcons/Material-CodeJson.svg" width="24"> JSON
### Actions
- [Parse JSON text](#parse-json-text)

#### Parse JSON text
Parses the given JSON text and stores the object result.

[⬆️ Back to top](#technologies)


## <img src="Images/TechnologyIcons/LeanIX.svg" width="24"> LeanIX
### Actions
- [Get fact sheets](#get-fact-sheets)
- [Get metadata (language)](#get-metadata-language)
- [GraphQL query](#graphql-query)

#### Get fact sheets
Gets all fact sheets. You may choose specific types like 'Applicationl.

### Get metadata (language)
Gets the metadata (e.g. about fact sheets) for a specific language. This is handy to translate field values.

### GraphQL query
Executes an arbitrary query With any result.

[⬆️ Back to top](#technologies)


## <img src="Images/TechnologyIcons/Mail.svg" width="24"> Mail
### Actions
- [Parse EML](#parse-eml)

#### Parse EML
Parses an EML file into its individual parts.

[⬆️ Back to top](#technologies)


## <img src="Images/TechnologyIcons/Microsoft%20Exchange.svg" width="24"> Microsoft 365
### Actions
- [Delete mail](#delete-mail)
- [Move mail](#move-mail)
- [Send mail](#send-mail)

### Entra ID App
[How to register an App within Microsoft Entra ID](Register%20an%20App%20within%20Entra%20ID.md)

#### Delete mail
Delete an email.

#### Move mail
Move an email to a different folder.

#### Send mail
Send a mail.

[⬆️ Back to top](#technologies)


## <img src="Images/TechnologyIcons/Google%20Contacts.svg" width="24"> Microsoft 365 Contacts
### Actions
- [Create contact](#create-contact)
- [Create or update (upsert) contacts](#create-or-update-upsert-contacts)
- [Get contact](#get-contact)
- [Get contact folders](#get-contact-folders)
- [Update contact](#update-contact)

#### Create contact
Create contact for the current or a specific user.

#### Create or update (upsert) contacts
Create or update (upsert) multiple contacts of the current or specific users.

#### Get contact
Get contact for the current or a specific user.

#### Get contact folders
Get all contact folders for the current or a specific user.

#### Update contact
Update a contact of the current or a specific user.

[⬆️ Back to top](#technologies)


## <img src="Images/TechnologyIcons/Microsoft%20Excel.svg" width="24"> Microsoft Excel
### Actions
- [Data import](#excel---data-import)

#### Excel - Data import
Take an Excel template and import any amount of rows and columns into the speadsheet.

[⬆️ Back to top](#technologies)


## <img src="Images/TechnologyIcons/Microsoft%20OneDrive.svg" width="24"> Microsoft OneDrive / SharePoint
### Actions
- [Delete file](#delete-file)
- [Download file](#download-file)
- [Upload file](#upload-file)

#### Delete file
Deletes a file from OneDrive.

#### Download file
Downloads a file from OneDrive.

#### Upload file
Uploads a file to OneDrive.

[⬆️ Back to top](#technologies)


## <img src="Images/TechnologyIcons/Microsoft%20SQL%20Server.svg" width="24"> Microsoft SQL Server
### Actions
- [Query](#query)

#### Query
Executes a user specified query.

[⬆️ Back to top](#technologies)


## <img src="Images/TechnologyIcons/Microsoft%20Teams.svg" width="24"> Microsoft Teams
### Actions
- [Create Team](#create-team)
- [Get 1:1 chat](#get-11-chat)
- [Get channel messages](#get-channel-messages)
- [Get chat messages](#get-chat-messages)
- [Get User](#get-user)
- [Send channel message](#send-channel-message)
- [Send chat message](#send-chat-message)

#### Create Team
Creates a team (including the Microsoft 365 Group).
[How to register an App within Microsoft Entra ID](Register%20an%20App%20within%20Entra%20ID.md)

#### Get 1:1 chat
Starts or resumes a chat from the service account With another person.

#### Get channel messages
Gets the most recent 50 messages in a channel.

#### Get chat messages
Gets the most recent 50 messages in a Chat.

#### Get User
Gets the information about a certain user.

#### Send channel message
Sends a message to a channel inside a team.

#### Send chat message
Sends a message to a Chat.

[⬆️ Back to top](#technologies)


## <img src="Images/TechnologyIcons/Microsoft%20Word.svg" width="24"> Microsoft Word
### Actions
- [Convert documents to PDF](#convert-documents-to-pdf)
- [Convert to PDF](#convert-to-pdf)
- [Mail Merge](#mail-merge)
- [Modify document](#modify-document)

#### Convert documents to PDF
Convert multiple documents to PDF.

#### Convert to PDF
Convert a single documents to PDF.

#### Mail Merge
Fill a document that contains placeholders with an actual value.

#### Modify document
Modify a document by removing certain paragraphs.

[⬆️ Back to top](#technologies)


## <img src="Images/TechnologyIcons/Netbox.svg" width="24"> NetBox
### Actions
- [Get devices](#get-devices)
- [Get IP prefixes](#get-ip-prefixes)
- [Get sites](#get-sites)
- [Get support contracts](#get-support-contracts)
- [Get tenants](#get-tenants)
- [Get virtual machines](#get-virtual-machines)
- [Get VLANs](#get-vlans)

#### Get devices
Get all devices.

#### Get IP prefixes
Get all IP prefixes.

#### Get sites
Get all Sites.

#### Get support contracts
Get all support contracts. This requires a NetBox plugin.

#### Get tenants
Get all tenants.

#### Get virtual machines
Get all virtual machines.

#### Get VLANs
Get all VLANs.

[⬆️ Back to top](#technologies)


## <img src="Images/TechnologyIcons/Ninox.svg" width="24"> Ninox
### Actions
- [Create or update record(s)](#create-or-update-records)
- [Create record](#create-record)
- [Delete attachment](#delete-attachment)
- [Delete record](#delete-record)
- [Download attechment](#download-attechment)
- [Download attechments](#download-attechments)
- [Download various attechments](#download-various-attechments)
- [Find record](#find-record)
- [Find records](#find-records)
- [Get record](#get-record)
- [Get records](#get-records)
- [Update record](#update-record)
- [Update attachment](#update-attachment)
- [Update attachments](#update-attachments)

### Help
In following link u have information about the filters in get requests.
https://docs.ninox.com/en/api/introduction/tables-fields-records

#### Create or update record(s)
Create or update (upsert) a Single record or many at once.

#### Create record
Create a new record within a table.

#### Delete attachment
Deletes a specific attachment from a record.

#### Delete record
Delete a record.

#### Download attechment
Downloads a specific attachment from a record.

#### Download attechments
Downloads all attachments from a record.

#### Download various attechments
Downloads specific attachments from specific records.

#### Find record
Finds a specific record within a table.

#### Find records
Finds records within a table.

#### Get record
Gets a specific record by ID.

#### Get records
Gets specific records by ID.

#### Update record
Update certain fields of a record.

#### Update attachment
Uploads an attachment to a record.

#### Update attachments
Uploads attachments to a record.

[⬆️ Back to top](#technologies)


## <img src="Images/TechnologyIcons/Oktopus%20Icon%20Orange.svg" width="24"> Oktopus
### Actions
- [Evaluate script](#evaluate-script)

#### Evaluate script
Evaluate a more or less comples script which generates variables or influences the workflow state.

[⬆️ Back to top](#technologies)


## <img src="Images/TechnologyIcons/PDF.svg" width="24"> PDF
### Actions
- [Merge PDFs](#merge-pdfs)

#### Merge PDFs
Merge multiple PDF files into one PDF file.

[⬆️ Back to top](#technologies)


## <img src="Images/TechnologyIcons/Microsoft%20Power%20BI.svg" width="24"> Power BI
### Actions
- [Add rows to push dataset](#add-rows-to-push-dataset)
- [Create push dataset](#create-push-dataset)
- [Delete rows from push dataset](#delete-rows-from-push-dataset)
- [Execute Data Analysis Expression](#execute-data-analysis-expression)
- [Get dataset](#get-dataset)
- [Get datasets](#get-datasets)
- [Get push dataset tables](#get-push-dataset-tables)
- [Refresh dataset](#refresh-dataset)

#### Add rows to push dataset
Adds any number of new rows to a push dataset.

#### Create push dataset
Creates a new push dataset.

#### Delete rows from push dataset
Deletes all rows from a pusgh dataset.

#### Execute Data Analysis Expression
Executes a Data Analysis Expression (DAX).

#### Get dataset
Gets a specific dataset.

#### Get datasets
Gets all available datasets (available to the connection account).

#### Get push dataset tables
Gets all tables inside a oush dataset. Push dataset are very limited in ther functionality.

#### Refresh dataset
Refreshes a dataset.

[⬆️ Back to top](#technologies)


## <img src="Images/TechnologyIcons/RayVentory.svg" width="24"> ReyVentory Data Hub
### Actions
- [Get table data](#get-table-data)

#### Get table data
Gets all rows from table.

[⬆️ Back to top](#technologies)


## <img src="Images/TechnologyIcons/Shopware.svg" width="24"> Shopware
### Actions
- [Create product](#create-product)
- [Create product cross selling](#create-product-cross-selling)
- [Delete product](#delete-product)
- [Delete product cross selling](#delete-product-cross-selling)
- [Get product](#get-product)
- [Get product cross selling](#get-product-cross-selling)
- [Translate categories](#translate-categories)
- [Translate product](#translate-product)
- [Update product](#update-product)
- [Update product cross selling](#update-product-cross-selling)

#### Create product
Creates products in your shop.

#### Create product cross selling
Adds new cross selling to specific product.

#### Delete product
Deletes specific product from the shop.

#### Delete product cross selling
Deletes the cross selling entity for a given product.

#### Get product
Get a specific product.

#### Get product cross selling
Gets all cross selling entities of a specific product.

#### Translate categories
Adds translated texts to given categories in the specified language.

#### Translate product
Adds translated texts to a specific product.

#### Update product
Updates a specific product.

#### Update product cross selling
Updates a given cross selling entity of a specific product.

[⬆️ Back to top](#technologies)


## <img src="Images/TechnologyIcons/SMAX.svg" width="24"> SMAX
### Actions
- [Add comment](#add-comment)
- [Create record](#create-record)
- [Delete comment](#delete-comment)
- [Delete record](#delete-record)
- [Find record](#find-record)
- [Find records](#find-records)
- [Get record](#get-record)
- [Update comment](#update-comment)
- [Update record](#update-record)

#### Add comment
Adds one or more attechments to a record.

#### Create record
Adds a new comment to a record.

#### Delete comment
Deletes anm existing comment.

#### Delete record
Deletes anm existing record.

#### Find record
Find a record by query.

#### Find records
Find records by query.

#### Get record
Get a record by ID.

#### Update comment
Updates an existing comment.

#### Update record
Updates an existing record.

[⬆️ Back to top](#technologies)


## <img src="Images/TechnologyIcons/Text.svg" width="24"> Text
### Actions
- [Create file](#create-file)
- [Create file (from Base64)](#create-file-from-Base64)
- [Create text](#create-text)
- [Generate password](#generate-password)
- [Map single value](#map-single-value)
- [Read file](#read-file)
- [Split text](#split-text)

#### Create file
Combine variables and static text into a file.

#### Create file (from Base64)
Converts Base64 text into a file.

#### Create text
Combine variables and static text into a new text document.

#### Generate password
Generates a random sewuence of characters with a given length and character set.

#### Map single value
Takes any input text, mapped against a table with a specific output selected.

#### Read file
Reads the content of a file variable.

#### Split text
Takes any input text and split it by any given separator.

[⬆️ Back to top](#technologies)


## <img src="Images/TechnologyIcons/Timer.svg" width="24"> Timer
### Actions
- [Delay](#delay)

#### Delay
Waits a certain amount of time.\
Enter the time span between each execution (format `h:mm:ss`).

##### Example
`0:2:30` (2.5 minutes)

[⬆️ Back to top](#technologies)


## <img src="Images/TechnologyIcons/USM.svg" width="24"> USM (Preview)
### Actions
- [Change Object](#change-object)
- [Create Object](#create-object)
- [Create Ticket](#create-ticket)
- [Find Objects](#find-objects)
- [Get Object](#get-object)
- [Get Object by field](#get-object-by-field)

#### Change Object
Changes (updates) an existing Business Object.

#### Create Object
Creates a new Business Object.

#### Create Ticket
Creates a new ticket (Incident, Problem, ...).

#### Find Objects
Finds a specific bbusiness object.

#### Get Object
Fet a specific business object.

#### Get Object by field
Get the first business object by field.

[⬆️ Back to top](#technologies)


## <img src="Images/TechnologyIcons/Webhook.svg" width="24"> Webhook
### Actions
- [Webhook Response](#webhook-response)

#### Webhook Response
Customize the webhook response sent when immediatly executing a workflow via webhook.\
The response content. This can be a variety of text and variables.

##### Example
JSON: `{{ { Id: Ticket.Id, Messages: [ "Thanks Oktopus" ] } }}`\
File: `{{AFileVariable}}`\
Text: `Hello from my workflow.`\
HTML: `<a href="https://freedom-manufaktur.com">Thanks Oktopus</a>`

[⬆️ Back to top](#technologies)
