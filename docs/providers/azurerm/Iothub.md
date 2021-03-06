# Terraform::AzureRM::Iothub

Manages an IotHub

## Properties

`Name` - (Required) Specifies the name of the IotHub resource. Changing this forces a new resource to be created.

`ResourceGroupName` - (Required) The name of the resource group under which the IotHub resource has to be created. Changing this forces a new resource to be created.

`Location` - (Required) Specifies the supported Azure location where the resource has to be createc. Changing this forces a new resource to be created.

`Sku` - (Required) A `Sku` block as defined below.

`Endpoint` - (Optional) An `Endpoint` block as defined below.

`Route` - (Optional) A `Route` block as defined below.

`FallbackRoute` - (Optional) A `FallbackRoute` block as defined below. If the fallback route is enabled, messages that don't match any of the supplied routes are automatically sent to this route. Defaults to messages/events.

`Tags` - (Optional) A mapping of tags to assign to the resource.

### Sku Properties

`Name` - (Required) The name of the sku. Possible values are `B1`, `B2`, `B3`, `F1`, `S1`, `S2`, and `S3`.

`Tier` - (Required) The billing tier for the IoT Hub. Possible values are `Basic`, `Free` or `Standard`.

`Capacity` - (Required) The number of provisioned IoT Hub units.

### Endpoint Properties

`Type` - (Required) The type of the endpoint. Possible values are `AzureIotHub.StorageContainer`, `AzureIotHub.ServiceBusQueue`, `AzureIotHub.ServiceBusTopic` or `AzureIotHub.EventHub`.

`ConnectionString` - (Required) The connection string for the endpoint.

`Name` - (Required) The name of the endpoint. The name must be unique across endpoint types. The following names are reserved:  `events`, `operationsMonitoringEvents`, `fileNotifications` and `$default`.

`BatchFrequencyInSeconds` - (Optional) Time interval at which blobs are written to storage. Value should be between 60 and 720 seconds. Default value is 300 seconds. This attribute is mandatory for endpoint type `AzureIotHub.StorageContainer`.

`MaxChunkSizeInBytes` - (Optional) Maximum number of bytes for each blob written to storage. Value should be between 10485760(10MB) and 524288000(500MB). Default value is 314572800(300MB). This attribute is mandatory for endpoint type `AzureIotHub.StorageContainer`.

`ContainerName` - (Optional) The name of storage container in the storage account. This attribute is mandatory for endpoint type `AzureIotHub.StorageContainer`.

`Encoding` - (Optional) Encoding that is used to serialize messages to blobs. Supported values are 'avro' and 'avrodeflate'. Default value is 'avro'. This attribute is mandatory for endpoint type `AzureIotHub.StorageContainer`.

`FileNameFormat` - (Optional) File name format for the blob. Default format is ``{iothub}/{partition}/{YYYY}/{MM}/{DD}/{HH}/{mm}``. All parameters are mandatory but can be reordered. This attribute is mandatory for endpoint type `AzureIotHub.StorageContainer`.

### Route Properties

`Name` - (Required) The name of the route.

`Source` - (Required) The source that the routing rule is to be applied to, such as `DeviceMessages`. Possible values include: `RoutingSourceInvalid`, `RoutingSourceDeviceMessages`, `RoutingSourceTwinChangeEvents`, `RoutingSourceDeviceLifecycleEvents`, `RoutingSourceDeviceJobLifecycleEvents`.

`Condition` - (Optional) The condition that is evaluated to apply the routing rule. If no condition is provided, it evaluates to true by default. For grammar, see: https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-query-language.

`EndpointNames` - (Required) The list of endpoints to which messages that satisfy the condition are routed.

`Enabled` - (Required) Used to specify whether a route is enabled.

### FallbackRoute Properties

`Source` - (Optional) The source that the routing rule is to be applied to, such as `DeviceMessages`. Possible values include: `RoutingSourceInvalid`, `RoutingSourceDeviceMessages`, `RoutingSourceTwinChangeEvents`, `RoutingSourceDeviceLifecycleEvents`, `RoutingSourceDeviceJobLifecycleEvents`.

`Condition` - (Optional) The condition that is evaluated to apply the routing rule. If no condition is provided, it evaluates to true by default. For grammar, see: https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-query-language.

`EndpointNames` - (Optional) The endpoints to which messages that satisfy the condition are routed. Currently only 1 endpoint is allowed.

`Enabled` - (Optional) Used to specify whether the fallback route is enabled.


## Return Values

### Fn::GetAtt

`Id` - The ID of the IoTHub.

`EventHubEventsEndpoint` -  The EventHub compatible endpoint for events data.

`EventHubEventsPath` -  The EventHub compatible path for events data.

`EventHubOperationsEndpoint` -  The EventHub compatible endpoint for operational data.

`EventHubOperationsPath` -  The EventHub compatible path for operational data.

`Hostname` - The hostname of the IotHub Resource.

`SharedAccessPolicy` - One or more `shared_access_policy` blocks as defined below.

`KeyName` - The name of the shared access policy.

`PrimaryKey` - The primary key.

`SecondaryKey` - The secondary key.

`Permissions` - The permissions assigned to the shared access policy.

## See Also

* [azurerm_iothub](https://www.terraform.io/docs/providers/azurerm/r/iothub.html) in the _Terraform Provider Documentation_