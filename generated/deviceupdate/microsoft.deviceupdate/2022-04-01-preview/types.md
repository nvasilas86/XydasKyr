# Microsoft.DeviceUpdate @ 2022-04-01-preview

## Resource Microsoft.DeviceUpdate/accounts@2022-04-01-preview
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2022-04-01-preview' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **identity**: [ManagedServiceIdentity](#managedserviceidentity): Managed service identity (system assigned and/or user assigned identities)
* **location**: string (Required): The geo-location where the resource lives
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [AccountProperties](#accountproperties): Device Update account properties.
* **systemData**: [SystemData](#systemdata) (ReadOnly): Metadata pertaining to creation and last modification of the resource.
* **tags**: [TrackedResourceTags](#trackedresourcetags): Resource tags.
* **type**: 'Microsoft.DeviceUpdate/accounts' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.DeviceUpdate/accounts/instances@2022-04-01-preview
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2022-04-01-preview' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **location**: string (Required): The geo-location where the resource lives
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [InstanceProperties](#instanceproperties) (Required): Device Update instance properties.
* **systemData**: [SystemData](#systemdata) (ReadOnly): Metadata pertaining to creation and last modification of the resource.
* **tags**: [TrackedResourceTags](#trackedresourcetags): Resource tags.
* **type**: 'Microsoft.DeviceUpdate/accounts/instances' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.DeviceUpdate/accounts/privateEndpointConnectionProxies@2022-04-01-preview
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2022-04-01-preview' (ReadOnly, DeployTimeConstant): The resource api version
* **eTag**: string (ReadOnly): ETag from NRP.
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [PrivateEndpointConnectionProxyProperties](#privateendpointconnectionproxyproperties): Private endpoint connection proxy object property bag.
* **remotePrivateEndpoint**: [RemotePrivateEndpoint](#remoteprivateendpoint): Remote private endpoint details.
* **status**: string: Operation status.
* **systemData**: [SystemData](#systemdata) (ReadOnly): Metadata pertaining to creation and last modification of the resource.
* **type**: 'Microsoft.DeviceUpdate/accounts/privateEndpointConnectionProxies' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.DeviceUpdate/accounts/privateEndpointConnections@2022-04-01-preview
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2022-04-01-preview' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [PrivateEndpointConnectionProperties](#privateendpointconnectionproperties) (Required): Properties of the PrivateEndpointConnectProperties.
* **systemData**: [SystemData](#systemdata) (ReadOnly): Metadata pertaining to creation and last modification of the resource.
* **type**: 'Microsoft.DeviceUpdate/accounts/privateEndpointConnections' (ReadOnly, DeployTimeConstant): The resource type

## ManagedServiceIdentity
### Properties
* **principalId**: string (ReadOnly): The service principal ID of the system assigned identity. This property will only be provided for a system assigned identity.
* **tenantId**: string (ReadOnly): The tenant ID of the system assigned identity. This property will only be provided for a system assigned identity.
* **type**: 'None' | 'SystemAssigned' | 'SystemAssigned,UserAssigned' | 'UserAssigned' | string (Required): Type of managed service identity (where both SystemAssigned and UserAssigned types are allowed).
* **userAssignedIdentities**: [UserAssignedIdentities](#userassignedidentities): The set of user assigned identities associated with the resource. The userAssignedIdentities dictionary keys will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}. The dictionary values can be empty objects ({}) in requests.

## UserAssignedIdentities
### Properties
### Additional Properties
* **Additional Properties Type**: [UserAssignedIdentity](#userassignedidentity)

## UserAssignedIdentity
### Properties
* **clientId**: string (ReadOnly): The client ID of the assigned identity.
* **principalId**: string (ReadOnly): The principal ID of the assigned identity.

## AccountProperties
### Properties
* **hostName**: string (ReadOnly): API host name.
* **locations**: [Location](#location)[] (ReadOnly): Device Update account primary and failover location details
* **privateEndpointConnections**: [PrivateEndpointConnection](#privateendpointconnection)[]: List of private endpoint connections associated with the account.
* **provisioningState**: 'Accepted' | 'Canceled' | 'Creating' | 'Deleted' | 'Failed' | 'Succeeded' | string (ReadOnly): Provisioning state.
* **publicNetworkAccess**: 'Disabled' | 'Enabled' | string: Whether or not public network access is allowed for the account.
* **sku**: 'Free' | 'Standard' | string: Device Update Sku

## Location
### Properties
* **name**: string
* **role**: 'Failover' | 'Primary' | string: Whether the location is primary or failover

## PrivateEndpointConnection
### Properties
* **id**: string (ReadOnly): Fully qualified resource ID for the resource. Ex - /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/{resourceProviderNamespace}/{resourceType}/{resourceName}
* **name**: string (ReadOnly): The name of the resource
* **properties**: [PrivateEndpointConnectionProperties](#privateendpointconnectionproperties) (Required): Properties of the PrivateEndpointConnectProperties.
* **systemData**: [SystemData](#systemdata) (ReadOnly): Metadata pertaining to creation and last modification of the resource.
* **type**: string (ReadOnly): The type of the resource. E.g. "Microsoft.Compute/virtualMachines" or "Microsoft.Storage/storageAccounts"

## PrivateEndpointConnectionProperties
### Properties
* **groupIds**: string[]: Array of group IDs.
* **privateEndpoint**: [PrivateEndpoint](#privateendpoint): The Private Endpoint resource.
* **privateLinkServiceConnectionState**: [PrivateLinkServiceConnectionState](#privatelinkserviceconnectionstate) (Required): A collection of information about the state of the connection between service consumer and provider.
* **provisioningState**: 'Creating' | 'Deleting' | 'Failed' | 'Succeeded' | string (ReadOnly): The current provisioning state.

## PrivateEndpoint
### Properties
* **id**: string (ReadOnly): The ARM identifier for Private Endpoint

## PrivateLinkServiceConnectionState
### Properties
* **actionsRequired**: string: A message indicating if changes on the service provider require any updates on the consumer.
* **description**: string: The reason for approval/rejection of the connection.
* **status**: 'Approved' | 'Pending' | 'Rejected' | string: The private endpoint connection status.

## SystemData
### Properties
* **createdAt**: string: The timestamp of resource creation (UTC).
* **createdBy**: string: The identity that created the resource.
* **createdByType**: 'Application' | 'Key' | 'ManagedIdentity' | 'User' | string: The type of identity that created the resource.
* **lastModifiedAt**: string: The timestamp of resource last modification (UTC)
* **lastModifiedBy**: string: The identity that last modified the resource.
* **lastModifiedByType**: 'Application' | 'Key' | 'ManagedIdentity' | 'User' | string: The type of identity that created the resource.

## TrackedResourceTags
### Properties
### Additional Properties
* **Additional Properties Type**: string

## InstanceProperties
### Properties
* **accountName**: string (ReadOnly): Parent Device Update Account name which Instance belongs to.
* **diagnosticStorageProperties**: [DiagnosticStorageProperties](#diagnosticstorageproperties): Customer-initiated diagnostic log collection storage properties
* **enableDiagnostics**: bool: Enables or Disables the diagnostic logs collection
* **iotHubs**: [IotHubSettings](#iothubsettings)[]: List of IoT Hubs associated with the account.
* **provisioningState**: 'Accepted' | 'Canceled' | 'Creating' | 'Deleted' | 'Failed' | 'Succeeded' | string (ReadOnly): Provisioning state.

## DiagnosticStorageProperties
### Properties
* **authenticationType**: 'KeyBased' | string (Required): Authentication Type
* **connectionString**: string: ConnectionString of the diagnostic storage account
* **resourceId**: string (Required): ResourceId of the diagnostic storage account

## IotHubSettings
### Properties
* **resourceId**: string (Required): IoTHub resource ID

## TrackedResourceTags
### Properties
### Additional Properties
* **Additional Properties Type**: string

## PrivateEndpointConnectionProxyProperties
### Properties
* **provisioningState**: 'Creating' | 'Deleting' | 'Failed' | 'Succeeded' | string (ReadOnly): The current provisioning state.

## RemotePrivateEndpoint
### Properties
* **connectionDetails**: [ConnectionDetails](#connectiondetails)[]: List of connection details.
* **id**: string: Remote endpoint resource ID.
* **immutableResourceId**: string: Original resource ID needed by Microsoft.Network.
* **immutableSubscriptionId**: string: Original subscription ID needed by Microsoft.Network.
* **location**: string: ARM location of the remote private endpoint.
* **manualPrivateLinkServiceConnections**: [PrivateLinkServiceConnection](#privatelinkserviceconnection)[]: List of private link service connections that need manual approval.
* **privateLinkServiceConnections**: [PrivateLinkServiceConnection](#privatelinkserviceconnection)[]: List of automatically approved private link service connections.
* **privateLinkServiceProxies**: [PrivateLinkServiceProxy](#privatelinkserviceproxy)[]: List of private link service proxies.
* **vnetTrafficTag**: string: Virtual network traffic tag.

## ConnectionDetails
### Properties
* **groupId**: string (ReadOnly): Group ID.
* **id**: string (ReadOnly): Connection details ID.
* **linkIdentifier**: string (ReadOnly): Link ID.
* **memberName**: string (ReadOnly): Member name.
* **privateIpAddress**: string (ReadOnly): Private IP address.

## PrivateLinkServiceConnection
### Properties
* **groupIds**: string[]: List of group IDs.
* **name**: string: Private link service connection name.
* **requestMessage**: string: Request message.

## PrivateLinkServiceProxy
### Properties
* **groupConnectivityInformation**: [GroupConnectivityInformation](#groupconnectivityinformation)[]: Group connectivity information.
* **id**: string: NRP resource ID.
* **remotePrivateEndpointConnection**: [PrivateLinkServiceProxyRemotePrivateEndpointConnection](#privatelinkserviceproxyremoteprivateendpointconnection): Remote private endpoint connection details.
* **remotePrivateLinkServiceConnectionState**: [PrivateLinkServiceConnectionState](#privatelinkserviceconnectionstate): A collection of information about the state of the connection between service consumer and provider.

## GroupConnectivityInformation
### Properties
* **customerVisibleFqdns**: string[]: List of customer visible FQDNs.
* **groupId**: string (ReadOnly): Group ID.
* **internalFqdn**: string (ReadOnly): Internal FQDN.
* **memberName**: string (ReadOnly): Member name.
* **privateLinkServiceArmRegion**: string: PrivateLinkService ARM region.
* **redirectMapId**: string: Redirect map ID.

## PrivateLinkServiceProxyRemotePrivateEndpointConnection
### Properties
* **id**: string (ReadOnly): Remote private endpoint connection ID.
