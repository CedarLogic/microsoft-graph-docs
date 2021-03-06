# Changelog for Microsoft Graph

This changelog covers what's changed in Microsoft Graph, including the v1.0 and beta endpoint Microsoft Graph APIs.  

## January 2017

### Outlook calendar

|**Change type**|**Endpoint**|**Description**|
|:-------------|:-----------|:--------------|
|Addition|v1.0|New action [findMeetingTimes](https://graph.microsoft.io/en-us/docs/api-reference/v1.0/api/user_findmeetingtimes) for the [user](https://graph.microsoft.io/en-us/docs/api-reference/v1.0/resources/user) resource.|
|Addition|v1.0|New complex type [attendeeBase](https://graph.microsoft.io/en-us/docs/api-reference/v1.0/resources/attendeebase) which consists of a type property for the attendee type.|
|Addition|v1.0|New complex types:<br/>[attendeeAvailability](https://graph.microsoft.io/en-us/docs/api-reference/v1.0/resources/attendeeavailability)<br/>[locationConstraint](https://graph.microsoft.io/en-us/docs/api-reference/v1.0/resources/locationconstraint) <br/>[locationConstraintItem](https://graph.microsoft.io/en-us/docs/api-reference/v1.0/resources/locationconstraintitem)<br/>[meetingTimeSuggestion](https://graph.microsoft.io/en-us/docs/api-reference/v1.0/resources/meetingtimesuggestion)<br/>[meetingTimeSuggestionsResult](https://graph.microsoft.io/en-us/docs/api-reference/v1.0/resources/meetingtimesuggestionsresult)<br/>[timeConstraint](https://graph.microsoft.io/en-us/docs/api-reference/v1.0/resources/timeconstraint)<br/>[timeSlot](https://graph.microsoft.io/en-us/docs/api-reference/v1.0/resources/timeslot)|
|Change|v1.0|The [attendee](https://graph.microsoft.io/en-us/docs/api-reference/v1.0/resources/attendee) complex type is now derived from attendeeBase, which in turn is derived from [recipient](https://graph.microsoft.io/en-us/docs/api-reference/v1.0/resources/recipient). Including the inherited properties, it consists of the same **status**, **type** and **emailAddress** properties as before.|
|Addition|Beta|hexColor added to the [calendar](https://graph.microsoft.io/en-us/docs/api-reference/beta/resources/calendar) resource.|

## December 2016

### Delta query

|**Change type**|**Endpoint**|**Description**|
|:-------------|:-----------|:--------------|
|Addition|Beta|A new delta function add to the following entities to perform [delta query](https://graph.microsoft.io/en-us/docs/concepts/delta_query_overview):<br/>contact<br/>contactFolder<br/>event<br/>group<br/>mailFolder<br/>message<br/>user<br/>See the following for examples:<br/>[Get incremental changes to groups (preview)](https://graph.microsoft.io/en-us/docs/concepts/delta_query_groups)<br/>[Get incremental changes to messages in a folder (preview)](https://graph.microsoft.io/en-us/docs/concepts/delta_query_message)<br/>[Get incremental changes to users (preview)](https://graph.microsoft.io/en-us/docs/concepts/delta_query_users)|

### Excel APIs

|**Change type**|**Endpoint**|**Description**|
|:-------------|:-----------|:--------------|
|Addition|v1.0|Added workbookPivotTable resource, refresh and refreshAll action on pivotTables, workbookRangeView resource, visibleView action on the filtered range to return workbookRangeView to the user, get rows collection and range resource off of visibleView, columnsAfter, columnsBefore, resizedRange, rowsAbove, and rowsBelow functions off of range resource, and new table properties.|

### Intune APIs

|**Change type**|**Endpoint**|**Description**|
|:-------------|:-----------|:--------------|
|Addition|Beta|Added resources and method APIs for Microsoft Intune. This is a large set of resources and methods to support the public preview of Intune on Azure Portal. For information about the Intune service, see the [Intune documentation](https://go.microsoft.com/fwlink/?linkid=836405). For information about the Intune resources and APIs, see [Working with Intune in Microsoft Graph](https://graph.microsoft.io/en-us/docs/api-reference/beta/resources/intune_graph_overview).|

## October 2016

### Authorization provider

|**Change type**|**Endpoint**|**Description**|
|:-------------|:-----------|:--------------|
|Addition|v1.0 and beta|The v2.0 auth endpoint now supports the client_credentials OAuth grant, which can be used for [daemon & long running processes in business scenarios](https://azure.microsoft.com/en-us/documentation/articles/active-directory-v2-protocols-oauth-client-creds/).|
|Addition|v1.0 and beta|The v2.0 auth endpoint now supports [permission scopes that require administrator's consent](http://graph.microsoft.io/en-us/docs/authorization/permission_scopes#permission-scope-details), via the [admin consent endpoint](https://azure.microsoft.com/en-us/documentation/articles/active-directory-v2-scopes/#admin-restricted-scopes).|
|Addition|v1.0 and beta|The v2.0 auth endpoint now supports administrative consent for all users in a tenant, via the [admin consent endpoint](https://azure.microsoft.com/en-us/documentation/articles/active-directory-v2-scopes/#admin-restricted-scopes).|

### Invitation APIs

|**Change type**|**Endpoint**|**Description**|
|:-------------|:-----------|:--------------|
|Addition|Beta|Added invitedUserType property to the invitation entity type, that defines the type of user (“Guest” or “Member”) that is invited.|
|Deletion|Beta|We will be removing the invitedToGroups property from the invitation entity-type on 11/11/2016. This means that you will no longer be able to add an invited user to a group using this API. Instead, use the [add member API](https://graph.microsoft.io/en-us/docs/api-reference/v1.0/api/group_post_members) to add a user to a group.|

## September 2016

### Azure AD application proxy

|**Change type**|**Endpoint**|**Description**|
|:--------------|:-----------|:--------------|
|Addition|Beta|Azure AD Application Proxy APIs are now available in the Microsoft Graph beta endpoint. These APIs allow for secure publishing of on-premises applications to users outside the corporate network using Azure AD as the common control plane for access. You can use the published APIs to write applications that can retrieve and update various aspects of application proxy, such as _connectors_, _connectorGroups_ and the _onPremisesPublishing_ settings of an application.|

### Drive

|**Change type**|**Endpoint**|**Description**|
|:--------------|:-----------|:--------------|
|Addition|Beta|Added _shared_ collection to allow accessing shared driveItems by shareId or sharing URL.|
|Addition|Beta|Added _search_ function to a drive, which allows searching for more items than just those in the drive’s root folder.|
  

### DriveItem

|**Change type**|**Endpoint**|**Description**|
|:--------------|:-----------|:--------------|
|Addition|Beta|Added support for _createUploadSession_, which allows uploading files larger than 4 MB to OneDrive, OneDrive for Business, and SharePoint document libraries.|
|Addition|Beta|Added _sharepointIds_ property to driveItem that returns traditional SharePoint API identifiers for driveItems stored in SharePoint.|
|Addition|Beta|Added additional properties on _remoteItem_.|
|Addition|Beta|Added the _quickXorHash_ value for files in OneDrive for Business.|
|Addition|Beta|Added scope to the _createSharingLink_ to allow creating company sharable links or anonymous sharing links.|

### Extended properties

|**Change type**|**Endpoint**|**Description**|
|:--------------|:-----------|:--------------|
|Addition|v1.0|[Extended properties](http://graph.microsoft.io/en-us/docs/api-reference/v1.0/resources/extended-properties-overview) are now supported by the following resources: message, mailFolder, event, calendar, contact, contactFolder, group event, group calendar, group post.|

### Groups

Added support for dynamic group membership through the public preview API, including the additions listed in the following table.

|**Change type**|**Endpoint**|**Description**|
|:--------------|:-----------|:--------------|
|Addition|Beta|Added **membershipRule** property contains rules that controls the memberships for this group, if the group is a dynamic group.|
|Addition|Beta|Added **membershipRuleProcessingState** property to control whether dynamic membership processing is on or paused for this group.|
|Addition|Beta|Set the **groupTypes** property to contain **"DynamicMembership"** to light up the dynamic groups capability for this group.|
|Addition|Beta|Added **preferredLanguage** property to indicate the preferred language for an Office 365 group.|
|Addition|Beta|Added **theme** property to specify an Office 365 group's color theme.|

### Hybrid deployment support

|**Change type**|**Endpoint**|**Description**|
|:--------------|:-----------|:--------------|
|Addition|v1.0|Apps can use v1.0 Outlook Mail, Calendar, and Contacts APIs to access on-premises mailboxes in a hybrid deployment with Exchange 2016 Cumulative Update 3 (CU3). Find more details about REST API support in specific [hybrid deployments](https://graph.microsoft.io/en-us/docs/overview/hybrid_rest_support). **Note:** If you're using these sets of API in v1.0, you can now find your apps, including production apps, working for on-premises mailboxes that meet the specific hybrid deployment requirements. This capability is only in preview.|

### IdentityRiskEvents

|**Change type**|**Endpoint**|**Description**|
|:--------------|:-----------|:--------------|
|Change|Beta|As part of the schema change where the type of two location properties is being replaced by a new complex type in the identityRiskEvents endpoint, the following properties are changed/added in the identityRiskEvents endpoint:</br>**location** – changed from Edm.String to ComplexType signInLocation.<br/>**previousLocation** – changed from Edm.String to ComplexType signInLocation.<br/>**signInLocation** – new ComplexType that contains city, state, countryOrRegion and geoCoordinates properties.<br/>**geoCoordinates** – new ComplexType that contains latitude and longitude properties.|

### Invitation manager

|**Change type**|**Endpoint**|**Description**|
|:--------------|:-----------|:--------------|
|Addition|Beta|Invitation manager APIs are now available in the Microsoft Graph beta endpoint. You can use invitation manager APIs to create an invite, in order to add an external user to the organization. As part of the invitation, you can also choose to add the invited user to an Office 365 group. For more details, see [invitation manager](https://graph.microsoft.io/en-us/docs/api-reference/beta/resources/invitation).|

### OneDrive

|**Change type**|**Endpoint**|**Description**|
|:--------------|:-----------|:--------------|
|Addition|v1.0|Added **CreateUploadSession** method on **driveItem**, which allows large file and resumable uploads.|
|Addition|v1.0|Added properties for tracking SharePoint IDs on items from SharePoint (**sharepointIds**) and a property to identify root folders (**root**).|
|Addition|v1.0|Added **Shares** root collection, which can be used with shareIds or sharing links to access shared items in OneDrive and SharePoint. Returns a new type, sharedDriveItem.|
|Addition|v1.0|Added **Invite** method on driveItem, which allows adding permissions to items. |
|Addition|v1.0|Added **Search** method on drive, which allows searching across items in the drive and shared items. |
|Addition|v1.0|Added **processingMetadata** property on file complex type quickXorHash property on hashes complex type. |
|Addition|v1.0|Added **quickXorHash** property on hashes complex type. |

### Outlook calendar

|**Change type**|**Endpoint**|**Description**|
|:--------------|:-----------|:--------------|
|Addition|v1.0|Added the **onlineMeetingUrl** property to the [event](http://graph.microsoft.io/en-us/docs/api-reference/v1.0/resources/event) resource.|
|Addition|Beta|Added [forward](http://graph.microsoft.io/en-us/docs/api-reference/beta/api/event_forward) action to the event resource.|
|Addition|Beta|Added the following properties to the [calendar](http://graph.microsoft.io/en-us/docs/api-reference/beta/resources/calendar) resource to support calendar sharing: **canEdit**, **canShare**, **canViewPrivateItems**, **isShared**, **isShareWithMe**, and **owner**.|

### Outlook mail

|**Change type**|**Endpoint**|**Description**|
|:--------------|:-----------|:--------------|
|Addition|v1.0|Added the [mailboxSettings](http://graph.microsoft.io/en-us/docs/api-reference/v1.0/resources/mailboxsettings) complex type, which includes the **automaticRepliesSetting**, **timeZone**, and **language** properties.|
|Addition|v1.0|Added the **mailboxSettings** property to the [user](http://graph.microsoft.io/en-us/docs/api-reference/v1.0/resources/user) resource.|
|Addition|Beta|Added support for creating, listing, getting, and deleting one or more instances of [mention](http://graph.microsoft.io/en-us/docs/api-reference/beta/resources/mention) in a message. Mentions support calling out to get the attention of other users in a message.|
|Addition|Beta|Added support for the [getMailTips](http://graph.microsoft.io/en-us/docs/api-reference/beta/api/user_getmailtips) action to get any MailTips for specific recipients. Added the following resources: automaticRepliesMailTips, mailTips, mailTipsError.|

### Query parameters

|**Change type**|**Endpoint**|**Description**|
|:--------------|:-----------|:--------------|
|Change|Beta|Query parameters without ‘$’ prefixes are supported as of 09/26/16. The ‘$’ prefix in query parameters is optional. For details, see the [Supporting query parameters without $ prefixes in Microsoft Graph](http://dev.office.com/queryparametersinMicrosoftGraph) blog post.|

### SharePoint

|**Change type**|**Endpoint**|**Description**|
|:--------------|:-----------|:--------------|
|Addition|Beta|Access to SharePoint sites and [lists by ID](http://graph.microsoft.io/en-us/docs/api-reference/beta/api/list_get) or [path/URL](http://graph.microsoft.io/en-us/docs/api-reference/beta/api/baseitem_getbyurl).|
|Addition|Beta|Support for [listing, creating, getting, and deleting instances of listItem](http://graph.microsoft.io/en-us/docs/api-reference/beta/resources/listitem).|

### Users

|**Change type**|**Endpoint**|**Description**|
|:--------------|:-----------|:--------------|
|Addition|Beta|Added **refreshTokensValidFromDateTime** read-only property to indicate when refresh or session tokens are valid from. Any tokens issued before this time are invalid, and any attempt to use them would force a new sign-in for the user.|
|Addition|Beta|Added **showInAddressList** property to control if the Outlook global address list should contain this user.|
|Addition|Beta|Added **invalidateAllRefreshTokens** service action that invalidates all of the user's refresh and session tokens issued to applications, by resetting the **refreshTokensValidFromDateTime** user property to the current date-time.|


### Webhooks

|**Change type**|**Endpoint**|**Description**|
|:--------------|:-----------|:--------------|
|Addition|Beta|Added Drive root items to Webhooks as a resource that is available to subscribe to.|

## August 2016

### Contacts

|**Change type**|**Endpoint**|**Description**|
|:--------------|:-----------|:--------------|
|Addition|Beta|As part of the schema change where a few properties are being removed and corresponding collections are being added to contacts endpoint, the following properties have been added to the contacts endpoint: _Websites – Collection(ComplexType: Website)_,_Phones – Collection (ComplexType: Phone)_, _PostalAddress – Collection(ComplexType: PhysicalAddress)_. For details, see the [Upcoming changes to Contacts and People APIs](https://blogs.msdn.microsoft.com/exchangedev/2016/06/09/upcoming-changes-to-contacts-and-people-apis/) blog post.|
|Deletion|Beta|As part of the schema change where a few properties are being removed and corresponding collections are being added to contacts endpoint, the following properties have been removed from the contacts endpoint: _BusinessHomePage_,_HomePhones_, _MobilePhone1_, _BusinessPhones_, _HomeAddress_, _BusinessAddress_, _OtherAddress_. For details, see the [Upcoming changes to Contacts and People APIs](https://blogs.msdn.microsoft.com/exchangedev/2016/06/09/upcoming-changes-to-contacts-and-people-apis/) blog post.|

### Excel APIs

|**Change type**|**Endpoint**|**Description**|
|:--------------|:-----------|:--------------|
|Addition|v1.0|Excel REST API on Microsoft Graph is generally available. Now you can build rich and deep integrations with Excel workbooks in Office 365. See the [Power your apps with the new Excel REST API on the Microsoft Graph](http://dev.office.com/blogs/power-your-apps-with-the-new-excel-rest-api) blog post for more details.|

### People

|**Change type**|**Endpoint**|**Description**|
|:--------------|:-----------|:--------------|
|Change|Beta|Property _WebSite_ is renamed to _Websites_. For details, see [Upcoming changes to Contacts and People APIs](https://blogs.msdn.microsoft.com/exchangedev/2016/06/09/upcoming-changes-to-contacts-and-people-apis/).|

### Privileged Identity Management

|**Change type**|**Endpoint**|**Description**|
|:--------------|:-----------|:--------------|
|Addition|Beta|Privileged Identity Management (PIM) REST APIs now are available in the Microsoft Graph beta endpoint. [Privileged Identity Management](https://azure.microsoft.com/en-us/documentation/articles/active-directory-privileged-identity-management-configure/) provides “just in time” activation for privileged Azure AD organizational roles such as Global Administrator, Billing Administrator, and so on. You can use the published APIs to write applications that retrieve and update privileged role assignments, and activate users into roles. For details, see [Microsoft Graph: Azure AD Privileged Identity Management Preview APIs available in Beta](http://dev.office.com/blogs/microsoft-graph-azure-ad-privileged-identity-management-apis-beta) and [Azure AD Privileged Identity Management](https://graph.microsoft.io/en-us/docs/api-reference/beta/resources/privilegedidentitymanagement_root).|
 
## July 2016
   
### Administrative Units

|**Change type**|**Endpoint**|**Description**|
|:--------------|:-----------|:--------------|
|Addition|Beta|Introduced the new Administrative Unites preview API. Administrative units allow organizations to subdivide their Azure Active Directory, and delegate administrative duties to those subdivisions. Subdivisions can represent regions, departments, cost centers, etc. This can now be managed through the Microsoft Graph API.|

## June 2016

### IdentityRiskEvents

|**Change type**|**Endpoint**|**Description**|
|:--------------|:-----------|:--------------|
|Addition|Beta|Introduced the new IdentityRiskEvents preview API. This API works in conjunction with Azure Active Directory Identity Protection. You can use it to query risk events generated by Identity Protection. For more details, see the [Introduction of a new preview API to Microsoft Graph: IdentityRiskEvents](http://dev.office.com/blogs/identityriskevents-api-preview) blog post.

### Subscriptions

|**Change type**|**Endpoint**|**Description**|
|:--------------|:-----------|:--------------|
|Addition|Beta|App-only scopes are now supported for _mail_ and _contacts_ subscriptions.|

## May 2016

### Calendar

|**Change type**|**Endpoint**|**Description**|
|:--------------|:-----------|:--------------|
|Breaking change|Beta|

### Contact

|**Change type**|**Endpoint**|**Description**|
|:--------------|:-----------|:--------------|
|Addition|v1.0|Added _extensions_, which is abstract type to support the OData v4 open type openTypeExtension.|

### Directory

|**Change type**|**Endpoint**|**Description**|
|:--------------|:-----------|:--------------|
|Breaking change|Beta|_settingTemplateId_ is renamed to _templateId_. This change will take effect May 19th, 2016.|

### Event

|**Change type**|**Endpoint**|**Description**|
|:--------------|:-----------|:--------------|
|Addition|v1.0|Added _extensions_, which is abstract type to support the OData v4 open type openTypeExtension.|

### EventMessages

|**Change type**|**Endpoint**|**Description**|
|:--------------|:-----------|:--------------|
|Addition|v1.0|Added _inferenceClassification_ and _extensions_ to _eventMessages_.|
|Addition|Beta|Added _responseRequested_ to _eventMessageRequest_.|

### Messages

|**Change type**|**Endpoint**|**Description**|
|:--------------|:-----------|:--------------|
|Addition|v1.0|Added _inferenceClassification_ and _extensions_ to _messages_.|
|Addition|Beta|Added _wellknownname_ to _contactFolder_.|Changes to _findMeetingTimes_ API. For more information, see the [Microsoft Graph findMeetingTimes API update](http://dev.office.com/microsoft-graph-findmeetingtimes-api-update) blog post. This change will take effect May 19th, 2016.|

### Post

|**Change type**|**Endpoint**|**Description**|
|:--------------|:-----------|:--------------|
|Addition|v1.0|Added _extensions_, which is abstract type to support the OData v4 open type openTypeExtension.|

### User

|**Change type**|**Endpoint**|**Description**|
|:--------------|:-----------|:--------------|
|Addition|v1.0|Added _inferenceClassification_ resource type.|
|Addition|Beta|Added _timeZone_ to _mailboxsettings_.|
|Addition|Beta|Added API _findMeetingTimesOLD _to _user_.|

## April 2016

### General

|**Change type**|**Endpoint**|**Description**|
|:--------------|:-----------|:--------------|
|Addition|v1.0 and Beta|Added support for honoring _Accept-Encoding:gzip_.|
|Addition|v1.0|Added support for cast segment in expand path. For example, 'https://graph.microsoft.com/v1.0/me/messages?$expand=microsoft.graph.eventMessage/event'.|
|Addition|Beta|Added support for PATCH request against structural properties. For example: 'PATCH /me/mailboxSettings'.|
|Addition|Beta|Azure Active Directory is now used as a fallback for /beta/users/id/photo requests when Outlook is unable to service the request, for example when the user has no mailbox license or the tenant does not have an Exchange Online subscription. NOTE: this fallback is available for both GET and PATCH.|
|Addition|Beta|Added support for cast segment in expand path. For example: 'https://graph.microsoft.com/v1.0/me/messages?$expand=microsoft.graph.eventMessage/event'.|

### OneDrive

|**Change type**|**Endpoint**|**Description**|
|:--------------|:-----------|:--------------|
|Fix|v1.0|Fixed the issue that OneDrive createLink requests failing with 500 and "Unsupported extension property type."|

## March 2016

### Calendar

|**Change type**|**Endpoint**|**Description**|
|:--------------|:-----------|:--------------|
|Addition|Beta|Added _singleValueExtendedProperties_ and _multiValueExtendedProperties_ properties.|
|Addition|Beta|Added _suggestionHint_ property to _meetingTimeCandidate _.|
|Addition|Beta|Added _locationUri_ property to _location_.|
|Addition|Beta|Added _type_ and _postOfficeBox_ to _physicalAddress _.|
|Change|Beta|_findMeetingTimes_ now takes new parameter _ReturnSuggestionHints_.|
|Change|Beta|_findMeetingTimes_ now returns a collection of _meetingTimeCandidate_.|

### Drive

|**Change type**|**Endpoint**|**Description**|
|:--------------|:-----------|:--------------|
|Addition|v1.0 and beta|Added _recent_ function to list a set of items that have been recently used by the signed in user. This list includes items that are in the user's drive as well as items they have access tofrom other drives. Example: GET /me/drive/recent.|
|Addition|v1.0 and beta|Added _sharedWithMe_ function to list the set of items that are shared with the current user. Example: GET /me/drive/sharedWithMe.|

### DriveItem

|**Change type**|**Endpoint**|**Description**|
|:--------------|:-----------|:--------------|
|Addition|v1.0 and beta|Added _remoteItem_ type to provide a link to an item in another drive.|
|Addition|v1.0 and beta|Added _sharingInvitation_ type to provide details of any associated sharing invitation for this permission.|
|Addition|v1.0 and beta|Added _delta_ function to track changes to items in a drive. Example: GET /me/drive/items/{item-id}/delta|
|Addition|v1.0 and beta|Added _copy_ that creates a copy of a _driveItem_ (including any children), under a new parent or with a new name. Example: POST /me/drive/items/{item-id}/copy.|
|Addition|v1.0 and beta|_conflictBehavior_ instance attributes is now applicable to _driveItem_.|
|Addition|Beta|Added _invite_ function to send a sharing invitation to an existing item. A sharing invitation creates a unique sharing link and sends an email to the recipient of the invitation that includes the sharing link. Example: POST /drive/items/{item-id}/invite.

### Event

|**Change type**|**Endpoint**|**Description**|
|:--------------|:-----------|:--------------|
|Addition|Beta|Added new property _onlineMeetingUrl_ and new method _cancel_.|

### Event messages

|**Change type**|**Endpoint**|**Description**|
|:--------------|:-----------|:--------------|
|Addition|Beta|Added _startDateTime_, _endDateTime_, _location_, _type_, _recurrence_, _isOutOfDate_, _conversationIndex_, _unsubscribe_, _unsubscribeData_, _unsubscribeEnabled_ and _flag_ properties to _eventmessage_ object.|
|Addition|Beta|Added _singleValueExtendedProperties_ and _multiValueExtendedProperties_ properties.|
|Addition|Beta|Added new method _unsubscribe_.|

### Excel

|**Change type**|**Endpoint**|**Description**|
|:--------------|:-----------|:--------------|
|Addition|Beta|We are adding new Excel REST APIs that let you read and modify data in an Excel workbook. It is now possible to build smart apps that allows users to get value out of the content stored in an Excel workbook by providing insights into the data. Take advantage of analytical powers of Excel, create tables and charts and extract visually appealing chart image - all from within your app. For details, see [Working with Excel in Microsoft Graph](http://graph.microsoft.io/en-us/docs/api-reference/beta/resources/excel).|

### General

|**Change type**|**Endpoint**|**Description**|
|:--------------|:-----------|:--------------|
|Addition|v1.0 and beta|Improved error message when resolving tenant alias and rejected JWT (AAD) tokens.|
|Addition|v1.0 and beta|The location of the authorization service endpoint is now returned in the _www-authenticate_ header when a request is received with an empty bearer token.|
Addition|v1.0 and beta|The ability to filter on an entity’s id property is now fixed. Example: GET https://graph.microsoft.com/v1.0/users?$filter=id+eq+'x'<br/>Previously, any POST requests to service actions and functions require prefixing the action or function name with the microsoft.graph prefix. For example: POST https://graph.microsoft.com/v1.0/me/Microsoft.Graph.getMemberGroups.<br/>The prefix is now no longer required (although it can still be specified). So the following would now also work: POST https://graph.microsoft.com/v1.0/me/getMemberGroups.|
|Change|Beta|Cleaned up subscription property names.|
|Addition|Beta|We’ve added the capability to discover (through _directorySettingTemplates_) and override the default behavior (by creating a _setting_ from the template) for entities and their associated functionality. Initially this only template provided is to control behaviors on Office groups.|

### Mail folder

|**Change type**|**Endpoint**|**Description**|
|:--------------|:-----------|:--------------|
|Addition|Beta|Added _wellKnownName_ and _userConfigurations_ properties.|
|Addition|Beta|Added _singleValueExtendedProperties_ and _multiValueExtendedProperties_ properties|

### Messages

|**Change type**|**Endpoint**|**Description**|
|:--------------|:-----------|:--------------|
|Addition|v1.0|Added _mobilePhone_ property.|
|Addition|v1.0 and beta|Added _internetMessageId_ property. The message ID in the format specified by [RFC2822](http://www.ietf.org/rfc/rfc2822.txt).|
|Change|Beta|Renamed _mobilePhone1_ property to _mobilePhone_.|
|Change|Beta|_createReply_ and _createReplyAll _take new parameter _Message_ and _comment_.|
|Change|Beta|_createForward _takes new parameter _Message _, _ToRecipients_ and _comment_.|
|Change|Beta|_reply_, _replyAll_and _forward_ take new parameter _Message_.|

### Permission

|**Change type**|**Endpoint**|**Description**|
|:--------------|:-----------|:--------------|
|Addition|v1.0 and beta|Added _sharingInvitation_ property to provide details of any associated sharing invitation for this permission.|

### Person

|**Change type**|**Endpoint**|**Description**|
|:--------------|:-----------|:--------------|
|Addition|Beta|Added new properties _birthday_, _personNotes_, _isFavorite_, _phones_, _permission_, _postalAddresses_,_websites_,_yomiCompany_, _department_, _profession_, _mailboxType_ and _personType_.|
|Addition|Beta|Added new enum types _physicalAddressType_, _webSite _, _phone_ and _webSiteType_.|

### Reference attachment

|**Change type**|**Endpoint**|**Description**|
|:--------------|:-----------|:--------------|
|Addition|Beta|Added new properties _sourceUrl_, _providerType_, _thumbnailUrl_, _previewUrl_, _permission_ and _isFolder_.|
|Addition|Beta|Added _singleValueExtendedProperties_ and _multiValueExtendedProperties_ properties.|
|Addition|Beta|Added new enum types _referenceAttachmentProvider _and _referenceAttachmentPermission_.|

### Subscriptions

|**Change type**|**Endpoint**|**Description**|
|:--------------|:-----------|:--------------|
|Addition|v1.0|Webhooks are now GA on V1.0 endpoint via the _/Subscriptions_ resource. Create, Read, Renew and Delete subscriptions to receive notifications on data from Outlook and Office 365 group conversations.|

### User

|**Change type**|**Endpoint**|**Description**|
|:--------------|:-----------|:--------------|
|Addition|Beta|Added _mailboxSettings_ property and corresponding types.|

## February 2016

### DriveItem

|**Change type**|**Endpoint**|**Description**|
|:--------------|:-----------|:--------------|
|Addition|v1.0 and beta|New _remoteItem_ property on driveItem for Microsoft accounts.|

### General

|**Change type**|**Endpoint**|**Description**|
|:--------------|:-----------|:--------------|
|Change|v1.0 and beta|-_/me/drive_ now works for both Microsoft accounts and Work and School accounts.|
|Change|v1.0 and beta|Drive requests for accounts whose OneDrive storage was provisioned on demand work more reliably and work in more scenarios where tenant default SharePoint sites use non-standard names.|
|Deletion|Beta|Removed various unimplemented types from the beta schema to more closely match the 1.0 schema.|

### Subscriptions

|**Change type**|**Endpoint**|**Description**|
|:--------------|:-----------|:--------------|
|Addition|Beta|notificationUrl validation on subscription creation. For details, see[Microsoft Graph WebHooks Update - January 2016](http://dev.office.com/blogs/Microsoft-Graph-WebHooks-Update-January-2016).|
|Addition|Beta|Subscription entities can now be deleted: DELETE https://graph.microsoft.com/beta/subscriptions/|

### Users

|**Change type**|**Endpoint**|**Description**|
|:--------------|:-----------|:--------------|
|Change|v1.0 and beta|_displayName_ is now returned for Microsoft accounts.|

## January 2016

### Contacts

|**Change type**|**Endpoint**|**Description**|
|:--------------|:-----------|:--------------|
|Addition|v1.0|Added mobilePhone property to personal contacts entity-set.|

### directoryObjects

|**Change type**|**Endpoint**|**Description**|
|:--------------|:-----------|:--------------|
|Fix|v1.0 and beta|Fixed calling actions that are bound to directoryObjects, which were failing with the following error: “The return type from the operation is not possible with the given entity set.”. This applies to the following actions: _microsoft.graph.checkMemberObjects_, _microsoft.graph.getMemberObjects_, _microsoft.graph.checkMemberGroups_, _microsoft.graph.assignLicense_, _microsoft.graph.changePassword_.|

## December 2015

### Contacts

|**Change type**|**Endpoint**|**Description**|
|:--------------|:-----------|:--------------|
|Addition|Beta|Added mobilePhone property to personal contacts entity-set.|

### General

|**Change type**|**Endpoint**|**Description**|
|:--------------|:-----------|:--------------|
|Fix|v1.0 and beta|Fixed requests using $filter expressions that specified the same property more than once, which were failing with the following 500 error: “An item with the same key has already been added”.|
|Fix|v1.0 and beta|Fixed case insensitivity for action parameter names and values.|
|Fix|v1.0 and beta|Fixed request processing for payloads containing null values for some embedded complex properties, which were failing with a null reference exception.|
|Addition|v1.0 and beta|Added support for complex type property sorting and filtering.|
|Addition|v1.0 and beta|Added authorization_uri property in the www-authenticate header on a 401 response. This uri can be used to start the token acquisition flow.|
|Addition|v1.0 and beta|Improved error messages across users and groups.|

### Groups

|**Change type**|**Endpoint**|**Description**|
|:--------------|:-----------|:--------------|
|Fix|v1.0 and beta|Fixed calling the following group actions: _microsoft.graph.addFavorite_, _microsoft.graph.removeFavorite_ and _microsoft.graph.resetUnseenCount_.|

### Messages

|**Change type**|**Endpoint**|**Description**|
|:--------------|:-----------|:--------------|
|Addition|Beta|Added eventMessageRequest subtype of eventMessage and startDateTime, endDateTime, location, type, recurrence and isOutOfDate properties to eventMessage type.|

### Users

|**Change type**|**Endpoint**|**Description**|
|:--------------|:-----------|:--------------|
|Fix|v1.0 and beta|Fixed being able to select certain user properties on other users, when referencing the user by user principal name (UPN). For example: https://graph.microsoft.com/v1.0/users/anotherUser@contoso.com?$select=aboutMe|
|Fix|v1.0 and beta|Fixed calling the _microsoft.graph.reminderView_ user bound function, which was failing with the following error: “Could not find a property named ‘businessPhones’ on type ‘Microsoft.OutlookServices.Reminder’“.|
|Fix|v1.0 and beta|Fixed user creation and update (POST/PATCH /v1.0/users), which was failing with a 400 error.|


