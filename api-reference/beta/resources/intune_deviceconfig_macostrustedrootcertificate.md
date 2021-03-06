﻿# macOSTrustedRootCertificate resource type

> **Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.

OS X Trusted Root Certificate configuration profile.

Inherits from [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)

### Methods
|Method|Return Type|Description|
|---|---|---|
|[List macOSTrustedRootCertificates](../api/intune_deviceconfig_macostrustedrootcertificate_list.md)|[macOSTrustedRootCertificate](../resources/intune_deviceconfig_macostrustedrootcertificate.md) collection|List properties and relationships of the [macOSTrustedRootCertificate](../resources/intune_deviceconfig_macostrustedrootcertificate.md) objects.|
|[Get macOSTrustedRootCertificate](../api/intune_deviceconfig_macostrustedrootcertificate_get.md)|[macOSTrustedRootCertificate](../resources/intune_deviceconfig_macostrustedrootcertificate.md)|Read properties and relationships of the [macOSTrustedRootCertificate](../resources/intune_deviceconfig_macostrustedrootcertificate.md) object.|
|[Create macOSTrustedRootCertificate](../api/intune_deviceconfig_macostrustedrootcertificate_create.md)|[macOSTrustedRootCertificate](../resources/intune_deviceconfig_macostrustedrootcertificate.md)|Create a new [macOSTrustedRootCertificate](../resources/intune_deviceconfig_macostrustedrootcertificate.md) object.|
|[Delete macOSTrustedRootCertificate](../api/intune_deviceconfig_macostrustedrootcertificate_delete.md)|None|Deletes a [macOSTrustedRootCertificate](../resources/intune_deviceconfig_macostrustedrootcertificate.md).|
|[Update macOSTrustedRootCertificate](../api/intune_deviceconfig_macostrustedrootcertificate_update.md)|[macOSTrustedRootCertificate](../resources/intune_deviceconfig_macostrustedrootcertificate.md)|Update the properties of a [macOSTrustedRootCertificate](../resources/intune_deviceconfig_macostrustedrootcertificate.md) object.|
|[List deviceConfigurationGroupAssignments](../api/intune_deviceconfig_macostrustedrootcertificate_list_deviceconfigurationgroupassignment.md)|[deviceConfigurationGroupAssignment](../resources/intune_deviceconfig_deviceconfigurationgroupassignment.md) collection|Get the deviceConfigurationGroupAssignments from the groupAssignments navigation property.|
|[List deviceConfigurationDeviceStatuses](../api/intune_deviceconfig_macostrustedrootcertificate_list_deviceconfigurationdevicestatus.md)|[deviceConfigurationDeviceStatus](../resources/intune_deviceconfig_deviceconfigurationdevicestatus.md) collection|Get the deviceConfigurationDeviceStatuses from the deviceStatuses navigation property.|
|[List deviceConfigurationUserStatuses](../api/intune_deviceconfig_macostrustedrootcertificate_list_deviceconfigurationuserstatus.md)|[deviceConfigurationUserStatus](../resources/intune_deviceconfig_deviceconfigurationuserstatus.md) collection|Get the deviceConfigurationUserStatuses from the userStatuses navigation property.|
|[Get deviceConfigurationDeviceOverview](../api/intune_deviceconfig_macostrustedrootcertificate_get_deviceconfigurationdeviceoverview.md)|[deviceConfigurationDeviceOverview](../resources/intune_deviceconfig_deviceconfigurationdeviceoverview.md)|Get the [deviceConfigurationDeviceOverview](../resources/intune_deviceconfig_deviceconfigurationdeviceoverview.md) from the deviceStatusOverview navigation property.|

### Properties
|Property|Type|Description|
|---|---|---|
|id|String|Key of the entity. Inherited from [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)|
|lastModifiedDateTime|DateTimeOffset|DateTime the object was last modified. Inherited from [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)|
|createdDateTime|DateTimeOffset|DateTime the object was created. Inherited from [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)|
|description|String|Admin provided description of the Device Configuration. Inherited from [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)|
|displayName|String|Admin provided name of the device configuration. Inherited from [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)|
|version|Int32|Version of the device configuration. Inherited from [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)|
|trustedRootCertificate|Binary|Trusted Root Certificate.|
|certFileName|String|File name to display in UI.|

### Relationships
|Relationship|Type|Description|
|---|---|---|
|groupAssignments|[deviceConfigurationGroupAssignment](../resources/intune_deviceconfig_deviceconfigurationgroupassignment.md) collection|The list of group assignments for the device configuration profile. Inherited from [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)|
|deviceStatuses|[deviceConfigurationDeviceStatus](../resources/intune_deviceconfig_deviceconfigurationdevicestatus.md) collection|Device configuration installation stauts by device. Inherited from [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)|
|userStatuses|[deviceConfigurationUserStatus](../resources/intune_deviceconfig_deviceconfigurationuserstatus.md) collection|Device configuration installation stauts by user. Inherited from [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)|
|deviceStatusOverview|[deviceConfigurationDeviceOverview](../resources/intune_deviceconfig_deviceconfigurationdeviceoverview.md)|Device Configuration devices status overview Inherited from [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)|

### JSON Representation
Here is a JSON representation of the resource.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.macOSTrustedRootCertificate"
}
-->
```json
{
  "@odata.type": "#microsoft.graph.macOSTrustedRootCertificate",
  "id": "String (identifier)",
  "lastModifiedDateTime": "String (timestamp)",
  "createdDateTime": "String (timestamp)",
  "description": "String",
  "displayName": "String",
  "version": 1024,
  "trustedRootCertificate": "binary",
  "certFileName": "String"
}
```



