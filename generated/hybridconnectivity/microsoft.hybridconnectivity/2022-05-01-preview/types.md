# Microsoft.HybridConnectivity @ 2022-05-01-preview

## Resource Microsoft.HybridConnectivity/endpoints@2022-05-01-preview
* **Valid Scope(s)**: Unknown
### Properties
* **apiVersion**: '2022-05-01-preview' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [EndpointProperties](#endpointproperties): Endpoint details
* **systemData**: [SystemData](#systemdata) (ReadOnly): Metadata pertaining to creation and last modification of the resource.
* **type**: 'Microsoft.HybridConnectivity/endpoints' (ReadOnly, DeployTimeConstant): The resource type

## Function listCredentials (Microsoft.HybridConnectivity/endpoints@2022-05-01-preview)
* **Resource**: Microsoft.HybridConnectivity/endpoints
* **ApiVersion**: 2022-05-01-preview
* **Output**: [EndpointAccessResource](#endpointaccessresource)

## Function listManagedProxyDetails (Microsoft.HybridConnectivity/endpoints@2022-05-01-preview)
* **Resource**: Microsoft.HybridConnectivity/endpoints
* **ApiVersion**: 2022-05-01-preview
* **Input**: [ManagedProxyRequest](#managedproxyrequest)
* **Output**: [ManagedProxyResource](#managedproxyresource)

## EndpointProperties
### Properties
* **provisioningState**: string (ReadOnly): The resource provisioning state.
* **resourceId**: string: The resource Id of the connectivity endpoint (optional).
* **type**: 'custom' | 'default' | string (Required): The type of endpoint.

## SystemData
### Properties
* **createdAt**: string: The timestamp of resource creation (UTC).
* **createdBy**: string: The identity that created the resource.
* **createdByType**: 'Application' | 'Key' | 'ManagedIdentity' | 'User' | string: The type of identity that created the resource.
* **lastModifiedAt**: string: The timestamp of resource last modification (UTC)
* **lastModifiedBy**: string: The identity that last modified the resource.
* **lastModifiedByType**: 'Application' | 'Key' | 'ManagedIdentity' | 'User' | string: The type of identity that created the resource.

## EndpointAccessResource
### Properties
* **relay**: [RelayNamespaceAccessProperties](#relaynamespaceaccessproperties) (ReadOnly): Azure relay hybrid connection access properties

## RelayNamespaceAccessProperties
### Properties
* **accessKey**: string (ReadOnly): Access key for hybrid connection.
* **expiresOn**: int (ReadOnly): The expiration of access key in unix time.
* **hybridConnectionName**: string (ReadOnly): Azure Relay hybrid connection name for the resource.
* **namespaceName**: string (ReadOnly): The namespace name.
* **namespaceNameSuffix**: string (ReadOnly): The suffix domain name of relay namespace.

## ManagedProxyRequest
### Properties
* **hostname**: string (WriteOnly): The target host name.
* **service**: string (Required, WriteOnly): The name of the service.

## ManagedProxyResource
### Properties
* **expiresOn**: int (ReadOnly): The expiration time of short lived proxy name in unix epoch.
* **proxy**: string (ReadOnly): The short lived proxy name.
