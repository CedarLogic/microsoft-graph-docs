﻿# defaultDeviceEnrollmentRestrictions resource type

> **Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.

Device Enrollment Restrictions
### Properties
|Property|Type|Description|
|---|---|---|
|iosRestrictions|[deviceEnrollmentPlatformRestrictions](../resources/intune_onboarding_deviceenrollmentplatformrestrictions.md)|Restrictions on iOS enrollment|
|windowsRestrictions|[deviceEnrollmentPlatformRestrictions](../resources/intune_onboarding_deviceenrollmentplatformrestrictions.md)|Restrictions on Android enrollment|
|windowsMobileRestrictions|[deviceEnrollmentPlatformRestrictions](../resources/intune_onboarding_deviceenrollmentplatformrestrictions.md)|Restrictions on Windows Mobile enrollment|
|androidRestrictions|[deviceEnrollmentPlatformRestrictions](../resources/intune_onboarding_deviceenrollmentplatformrestrictions.md)|Restrictions on Windows Desktop enrollment|
|macRestrictions|[deviceEnrollmentPlatformRestrictions](../resources/intune_onboarding_deviceenrollmentplatformrestrictions.md)|Restrictions on Mac enrollment|

### Relationships
None
### JSON Representation
Here is a JSON representation of the resource.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.defaultDeviceEnrollmentRestrictions"
}
-->
```json
{
  "@odata.type": "#microsoft.graph.defaultDeviceEnrollmentRestrictions",
  "iosRestrictions": {
    "@odata.type": "microsoft.graph.deviceEnrollmentPlatformRestrictions",
    "platformBlocked": true,
    "personalDeviceEnrollmentBlocked": true
  },
  "windowsRestrictions": {
    "@odata.type": "microsoft.graph.deviceEnrollmentPlatformRestrictions",
    "platformBlocked": true,
    "personalDeviceEnrollmentBlocked": true
  },
  "windowsMobileRestrictions": {
    "@odata.type": "microsoft.graph.deviceEnrollmentPlatformRestrictions",
    "platformBlocked": true,
    "personalDeviceEnrollmentBlocked": true
  },
  "androidRestrictions": {
    "@odata.type": "microsoft.graph.deviceEnrollmentPlatformRestrictions",
    "platformBlocked": true,
    "personalDeviceEnrollmentBlocked": true
  },
  "macRestrictions": {
    "@odata.type": "microsoft.graph.deviceEnrollmentPlatformRestrictions",
    "platformBlocked": true,
    "personalDeviceEnrollmentBlocked": true
  }
}
```



