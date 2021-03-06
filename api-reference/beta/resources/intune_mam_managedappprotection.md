﻿# managedAppProtection resource type

> **Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.

Policy used to configure detailed management settings for a specified set of apps

Inherits from [managedAppPolicy](../resources/intune_mam_managedapppolicy.md)

### Methods
|Method|Return Type|Description|
|---|---|---|
|[List managedAppProtections](../api/intune_mam_managedappprotection_list.md)|[managedAppProtection](../resources/intune_mam_managedappprotection.md) collection|List properties and relationships of the [managedAppProtection](../resources/intune_mam_managedappprotection.md) objects.|
|[Get managedAppProtection](../api/intune_mam_managedappprotection_get.md)|[managedAppProtection](../resources/intune_mam_managedappprotection.md)|Read properties and relationships of the [managedAppProtection](../resources/intune_mam_managedappprotection.md) object.|
|[List mobileAppIdentifierDeployments](../api/intune_mam_managedappprotection_list_mobileappidentifierdeployment.md)|[mobileAppIdentifierDeployment](../resources/intune_mam_mobileappidentifierdeployment.md) collection|Get the mobileAppIdentifierDeployments from the mobileAppIdentifierDeployments navigation property.|
|[Get managedAppPolicyDeploymentSummary](../api/intune_mam_managedappprotection_get_managedapppolicydeploymentsummary.md)|[managedAppPolicyDeploymentSummary](../resources/intune_mam_managedapppolicydeploymentsummary.md)|Get the [managedAppPolicyDeploymentSummary](../resources/intune_mam_managedapppolicydeploymentsummary.md) from the deploymentSummary navigation property.|

### Properties
|Property|Type|Description|
|---|---|---|
|displayName|String|Policy display name. Inherited from [managedAppPolicy](../resources/intune_mam_managedapppolicy.md)|
|description|String|The policy's description. Inherited from [managedAppPolicy](../resources/intune_mam_managedapppolicy.md)|
|lastModifiedTime|DateTimeOffset|Last time the policy was modified. Inherited from [managedAppPolicy](../resources/intune_mam_managedapppolicy.md)|
|deployedAppCount|Int32|Count of apps to which the current policy is deployed. Inherited from [managedAppPolicy](../resources/intune_mam_managedapppolicy.md)|
|id|String|Key of the entity. Inherited from [managedAppPolicy](../resources/intune_mam_managedapppolicy.md)|
|version|String|Version of the entity. Inherited from [managedAppPolicy](../resources/intune_mam_managedapppolicy.md)|
|periodOfflineBeforeAccessCheck|Duration|The period after which access is checked when the device is not connected to the internet.|
|periodOnlineBeforeAccessCheck|Duration|The period after which access is checked when the device is connected to the internet.|
|allowedInboundDataTransferSources|String|Sources from which data is allowed to be transferred. Possible values are: `allApps`, `managedApps`, `none`.|
|allowedOutboundDataTransferDestinations|String|Destinations to which data is allowed to be transferred. Possible values are: `allApps`, `managedApps`, `none`.|
|organizationalCredentialsRequired|Boolean|Indicates whether organizational credentials are required for app use.|
|allowedOutboundClipboardSharingLevel|String|The level to which the clipboard may be shared between apps on the managed device. Possible values are: `allApps`, `managedAppsWithPasteIn`, `managedApps`, `blocked`.|
|dataBackupBlocked|Boolean|Indicates whether the backup of a managed app's data is blocked.|
|deviceComplianceRequired|Boolean|Indicates whether device compliance is required.|
|managedBrowserToOpenLinksRequired|Boolean|Indicates whether internet links should be opened in the managed browser app.|
|saveAsBlocked|Boolean|Indicates whether users may use the "Save As" menu item to save a copy of protected files.|
|periodOfflineBeforeWipeIsEnforced|Duration|The amount of time an app is allowed to remain disconnected from the internet before all managed data it is wiped.|
|pinRequired|Boolean|Indicates whether an app-level pin is required.|
|maximumPinRetries|Int32|Maximum number of incorrect pin retry attempts before the managed app is wiped.|
|simplePinBlocked|Boolean|Indicates whether simplePin is blocked.|
|minimumPinLength|Int32|Minimum pin length required for an app-level pin if PinRequired is set to True|
|pinCharacterSet|String|Character set which may be used for an app-level pin if PinRequired is set to True. Possible values are: `any`, `numeric`, `alphanumeric`, `alphanumericAndSymbol`.|
|allowedDataStorageLocations|String collection|Data storage locations where a user may store managed data.|
|contactSyncBlocked|Boolean|Indicates whether contacts can be synced to the user's device.|
|printBlocked|Boolean|Indicates whether printing is allowed from managed apps.|
|fingerprintBlocked|Boolean|Indicates whether use of the fingerprint reader is allowed in place of a pin if PinRequired is set to True.|

### Relationships
|Relationship|Type|Description|
|---|---|---|
|mobileAppIdentifierDeployments|[mobileAppIdentifierDeployment](../resources/intune_mam_mobileappidentifierdeployment.md) collection|List of apps to which the policy is deployed. Inherited from [managedAppPolicy](../resources/intune_mam_managedapppolicy.md)|
|deploymentSummary|[managedAppPolicyDeploymentSummary](../resources/intune_mam_managedapppolicydeploymentsummary.md)|Navigation property to deployment summary of the configuration. Inherited from [managedAppPolicy](../resources/intune_mam_managedapppolicy.md)|

### JSON Representation
Here is a JSON representation of the resource.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.managedAppProtection"
}
-->
```json
{
  "@odata.type": "#microsoft.graph.managedAppProtection",
  "displayName": "String",
  "description": "String",
  "lastModifiedTime": "String (timestamp)",
  "deployedAppCount": 1024,
  "id": "String (identifier)",
  "version": "String",
  "periodOfflineBeforeAccessCheck": "String (duration)",
  "periodOnlineBeforeAccessCheck": "String (duration)",
  "allowedInboundDataTransferSources": "String",
  "allowedOutboundDataTransferDestinations": "String",
  "organizationalCredentialsRequired": true,
  "allowedOutboundClipboardSharingLevel": "String",
  "dataBackupBlocked": true,
  "deviceComplianceRequired": true,
  "managedBrowserToOpenLinksRequired": true,
  "saveAsBlocked": true,
  "periodOfflineBeforeWipeIsEnforced": "String (duration)",
  "pinRequired": true,
  "maximumPinRetries": 1024,
  "simplePinBlocked": true,
  "minimumPinLength": 1024,
  "pinCharacterSet": "String",
  "allowedDataStorageLocations": [
    "String"
  ],
  "contactSyncBlocked": true,
  "printBlocked": true,
  "fingerprintBlocked": true
}
```



