# Microsoft.AppPlatform @ 2022-04-01

## Resource Microsoft.AppPlatform/Spring@2022-04-01
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2022-04-01' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **location**: string: The GEO location of the resource.
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [ClusterResourceProperties](#clusterresourceproperties): Service properties payload
* **sku**: [Sku](#sku): Sku of Azure Spring Apps
* **systemData**: [SystemData](#systemdata) (ReadOnly): Metadata pertaining to creation and last modification of the resource.
* **tags**: [TrackedResourceTags](#trackedresourcetags): Tags of the service which is a list of key value pairs that describe the resource.
* **type**: 'Microsoft.AppPlatform/Spring' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.AppPlatform/Spring/apps@2022-04-01
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2022-04-01' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **identity**: [ManagedIdentityProperties](#managedidentityproperties): Managed identity properties retrieved from ARM request headers.
* **location**: string: The GEO location of the application, always the same with its parent resource
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [AppResourceProperties](#appresourceproperties): App resource properties payload
* **systemData**: [SystemData](#systemdata) (ReadOnly): Metadata pertaining to creation and last modification of the resource.
* **type**: 'Microsoft.AppPlatform/Spring/apps' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.AppPlatform/Spring/apps/bindings@2022-04-01
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2022-04-01' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [BindingResourceProperties](#bindingresourceproperties): Binding resource properties payload
* **systemData**: [SystemData](#systemdata) (ReadOnly): Metadata pertaining to creation and last modification of the resource.
* **type**: 'Microsoft.AppPlatform/Spring/apps/bindings' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.AppPlatform/Spring/apps/deployments@2022-04-01
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2022-04-01' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [DeploymentResourceProperties](#deploymentresourceproperties): Deployment resource properties payload
* **sku**: [Sku](#sku): Sku of Azure Spring Apps
* **systemData**: [SystemData](#systemdata) (ReadOnly): Metadata pertaining to creation and last modification of the resource.
* **type**: 'Microsoft.AppPlatform/Spring/apps/deployments' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.AppPlatform/Spring/apps/domains@2022-04-01
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2022-04-01' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [CustomDomainProperties](#customdomainproperties): Custom domain of app resource payload.
* **systemData**: [SystemData](#systemdata) (ReadOnly): Metadata pertaining to creation and last modification of the resource.
* **type**: 'Microsoft.AppPlatform/Spring/apps/domains' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.AppPlatform/Spring/buildServices/agentPools@2022-04-01
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2022-04-01' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [BuildServiceAgentPoolProperties](#buildserviceagentpoolproperties): Build service agent pool properties
* **systemData**: [SystemData](#systemdata) (ReadOnly): Metadata pertaining to creation and last modification of the resource.
* **type**: 'Microsoft.AppPlatform/Spring/buildServices/agentPools' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.AppPlatform/Spring/buildServices/builders@2022-04-01
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2022-04-01' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [BuilderProperties](#builderproperties): KPack Builder properties payload
* **systemData**: [SystemData](#systemdata) (ReadOnly): Metadata pertaining to creation and last modification of the resource.
* **type**: 'Microsoft.AppPlatform/Spring/buildServices/builders' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.AppPlatform/Spring/buildServices/builders/buildpackBindings@2022-04-01
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2022-04-01' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [BuildpackBindingProperties](#buildpackbindingproperties): Properties of a buildpack binding
* **systemData**: [SystemData](#systemdata) (ReadOnly): Metadata pertaining to creation and last modification of the resource.
* **type**: 'Microsoft.AppPlatform/Spring/buildServices/builders/buildpackBindings' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.AppPlatform/Spring/buildServices/builds@2022-04-01
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2022-04-01' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [BuildProperties](#buildproperties): Build resource properties payload
* **systemData**: [SystemData](#systemdata) (ReadOnly): Metadata pertaining to creation and last modification of the resource.
* **type**: 'Microsoft.AppPlatform/Spring/buildServices/builds' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.AppPlatform/Spring/certificates@2022-04-01
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2022-04-01' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [CertificateProperties](#certificateproperties): Certificate resource payload.
* **systemData**: [SystemData](#systemdata) (ReadOnly): Metadata pertaining to creation and last modification of the resource.
* **type**: 'Microsoft.AppPlatform/Spring/certificates' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.AppPlatform/Spring/configServers@2022-04-01
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2022-04-01' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **name**: 'default' (Required, DeployTimeConstant): The resource name
* **properties**: [ConfigServerProperties](#configserverproperties): Config server git properties payload
* **systemData**: [SystemData](#systemdata) (ReadOnly): Metadata pertaining to creation and last modification of the resource.
* **type**: 'Microsoft.AppPlatform/Spring/configServers' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.AppPlatform/Spring/configurationServices@2022-04-01
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2022-04-01' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [ConfigurationServiceProperties](#configurationserviceproperties): Application Configuration Service properties payload
* **systemData**: [SystemData](#systemdata) (ReadOnly): Metadata pertaining to creation and last modification of the resource.
* **type**: 'Microsoft.AppPlatform/Spring/configurationServices' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.AppPlatform/Spring/monitoringSettings@2022-04-01
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2022-04-01' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **name**: 'default' (Required, DeployTimeConstant): The resource name
* **properties**: [MonitoringSettingProperties](#monitoringsettingproperties): Monitoring Setting properties payload
* **systemData**: [SystemData](#systemdata) (ReadOnly): Metadata pertaining to creation and last modification of the resource.
* **type**: 'Microsoft.AppPlatform/Spring/monitoringSettings' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.AppPlatform/Spring/serviceRegistries@2022-04-01
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2022-04-01' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [ServiceRegistryProperties](#serviceregistryproperties) (ReadOnly): Service Registry properties payload
* **systemData**: [SystemData](#systemdata) (ReadOnly): Metadata pertaining to creation and last modification of the resource.
* **type**: 'Microsoft.AppPlatform/Spring/serviceRegistries' (ReadOnly, DeployTimeConstant): The resource type

## Function listTestKeys (Microsoft.AppPlatform/Spring@2022-04-01)
* **Resource**: Microsoft.AppPlatform/Spring
* **ApiVersion**: 2022-04-01
* **Output**: [TestKeys](#testkeys)

## AddonProfile
### Properties
### Additional Properties
* **Additional Properties Type**: any

## AddonProfile
### Properties
### Additional Properties
* **Additional Properties Type**: any

## ApplicationInsightsAgentVersions
### Properties
* **java**: string (ReadOnly): Indicates the version of application insight java agent

## AppResourceProperties
### Properties
* **addonConfigs**: [AppResourcePropertiesAddonConfigs](#appresourcepropertiesaddonconfigs): Collection of addons
* **enableEndToEndTLS**: bool: Indicate if end to end TLS is enabled.
* **fqdn**: string: Fully qualified dns Name.
* **httpsOnly**: bool: Indicate if only https is allowed.
* **loadedCertificates**: [LoadedCertificate](#loadedcertificate)[]: Collection of loaded certificate resources list and a possible link for next page.
* **persistentDisk**: [PersistentDisk](#persistentdisk): Persistent disk payload
* **provisioningState**: 'Creating' | 'Deleting' | 'Failed' | 'Succeeded' | 'Updating' | string (ReadOnly): Provisioning state of the App
* **public**: bool: Indicates whether the App exposes public endpoint
* **temporaryDisk**: [TemporaryDisk](#temporarydisk): Temporary disk payload
* **url**: string (ReadOnly): URL of the App

## AppResourcePropertiesAddonConfigs
### Properties
### Additional Properties
* **Additional Properties Type**: [AddonProfile](#addonprofile)

## BindingResourceProperties
### Properties
* **bindingParameters**: [BindingResourcePropertiesBindingParameters](#bindingresourcepropertiesbindingparameters): Binding parameters of the Binding resource
* **createdAt**: string (ReadOnly): Creation time of the Binding resource
* **generatedProperties**: string (ReadOnly): The generated Spring Boot property file for this binding. The secret will be deducted.
* **key**: string: The key of the bound resource
* **resourceId**: string: The Azure resource id of the bound resource
* **resourceName**: string (ReadOnly): The name of the bound resource
* **resourceType**: string (ReadOnly): The standard Azure resource type of the bound resource
* **updatedAt**: string (ReadOnly): Update time of the Binding resource

## BindingResourcePropertiesBindingParameters
### Properties
### Additional Properties
* **Additional Properties Type**: any

## BuilderProperties
### Properties
* **buildpackGroups**: [BuildpacksGroupProperties](#buildpacksgroupproperties)[]: Builder buildpack groups.
* **provisioningState**: 'Creating' | 'Deleting' | 'Failed' | 'Succeeded' | 'Updating' | string (ReadOnly): Builder provision status.
* **stack**: [StackProperties](#stackproperties): KPack ClusterStack properties payload

## BuildpackBindingLaunchProperties
### Properties
* **properties**: [BuildpackBindingLaunchProperties](#buildpackbindinglaunchproperties): Non-sensitive properties for launchProperties
* **secrets**: [BuildpackBindingLaunchPropertiesSecrets](#buildpackbindinglaunchpropertiessecrets): Sensitive properties for launchProperties

## BuildpackBindingLaunchProperties
### Properties
### Additional Properties
* **Additional Properties Type**: string

## BuildpackBindingLaunchPropertiesSecrets
### Properties
### Additional Properties
* **Additional Properties Type**: string

## BuildpackBindingProperties
### Properties
* **bindingType**: 'ApacheSkyWalking' | 'AppDynamics' | 'ApplicationInsights' | 'Dynatrace' | 'ElasticAPM' | 'NewRelic' | string: Buildpack Binding Type
* **launchProperties**: [BuildpackBindingLaunchProperties](#buildpackbindinglaunchproperties): Buildpack Binding Launch Properties
* **provisioningState**: 'Creating' | 'Deleting' | 'Failed' | 'Succeeded' | 'Updating' | string (ReadOnly): State of the Buildpack Binding.

## BuildpackProperties
### Properties
* **id**: string: Id of the buildpack

## BuildpacksGroupProperties
### Properties
* **buildpacks**: [BuildpackProperties](#buildpackproperties)[]: Buildpacks in the buildpack group
* **name**: string: Buildpack group name

## BuildProperties
### Properties
* **agentPool**: string: The resource id of agent pool
* **builder**: string: The resource id of builder to build the source code
* **env**: [BuildPropertiesEnv](#buildpropertiesenv): The environment variables for this build
* **provisioningState**: 'Creating' | 'Deleting' | 'Failed' | 'Succeeded' | 'Updating' | string (ReadOnly): Provisioning state of the KPack build result
* **relativePath**: string: The relative path of source code
* **triggeredBuildResult**: [TriggeredBuildResult](#triggeredbuildresult) (ReadOnly): The build result triggered by a build

## BuildPropertiesEnv
### Properties
### Additional Properties
* **Additional Properties Type**: string

## BuildServiceAgentPoolProperties
### Properties
* **poolSize**: [BuildServiceAgentPoolSizeProperties](#buildserviceagentpoolsizeproperties): Build service agent pool size properties
* **provisioningState**: string (ReadOnly): Provisioning state of the build service agent pool

## BuildServiceAgentPoolSizeProperties
### Properties
* **cpu**: string (ReadOnly): The cpu property of build service agent pool size
* **memory**: string (ReadOnly): The memory property of build service agent pool size
* **name**: string: The name of build service agent pool size

## CertificateProperties
* **Discriminator**: type

### Base Properties
* **activateDate**: string (ReadOnly): The activate date of certificate.
* **dnsNames**: string[] (ReadOnly): The domain list of certificate.
* **expirationDate**: string (ReadOnly): The expiration date of certificate.
* **issuedDate**: string (ReadOnly): The issue date of certificate.
* **issuer**: string (ReadOnly): The issuer of certificate.
* **subjectName**: string (ReadOnly): The subject name of certificate.
* **thumbprint**: string (ReadOnly): The thumbprint of certificate.
### ContentCertificateProperties
#### Properties
* **content**: string (WriteOnly): The content of uploaded certificate.
* **type**: 'ContentCertificate' (Required): The type of the certificate source.

### KeyVaultCertificateProperties
#### Properties
* **certVersion**: string: The certificate version of key vault.
* **excludePrivateKey**: bool: Optional. If set to true, it will not import private key from key vault.
* **keyVaultCertName**: string (Required): The certificate name of key vault.
* **type**: 'KeyVaultCertificate' (Required): The type of the certificate source.
* **vaultUri**: string (Required): The vault uri of user key vault.


## ClusterResourceProperties
### Properties
* **fqdn**: string (ReadOnly): Fully qualified dns name of the service instance
* **networkProfile**: [NetworkProfile](#networkprofile): Service network profile payload
* **provisioningState**: 'Creating' | 'Deleted' | 'Deleting' | 'Failed' | 'MoveFailed' | 'Moved' | 'Moving' | 'Starting' | 'Stopping' | 'Succeeded' | 'Updating' | string (ReadOnly): Provisioning state of the Service
* **serviceId**: string (ReadOnly): ServiceInstanceEntity GUID which uniquely identifies a created resource
* **version**: int (ReadOnly): Version of the Service
* **zoneRedundant**: bool

## ConfigServerGitProperty
### Properties
* **hostKey**: string: Public sshKey of git repository.
* **hostKeyAlgorithm**: string: SshKey algorithm of git repository.
* **label**: string: Label of the repository
* **password**: string: Password of git repository basic auth.
* **privateKey**: string: Private sshKey algorithm of git repository.
* **repositories**: [GitPatternRepository](#gitpatternrepository)[]: Repositories of git.
* **searchPaths**: string[]: Searching path of the repository
* **strictHostKeyChecking**: bool: Strict host key checking or not.
* **uri**: string (Required): URI of the repository
* **username**: string: Username of git repository basic auth.

## ConfigServerProperties
### Properties
* **configServer**: [ConfigServerSettings](#configserversettings): The settings of config server.
* **error**: [Error](#error): The error code compose of code and message.
* **provisioningState**: 'Deleted' | 'Failed' | 'NotAvailable' | 'Succeeded' | 'Updating' | string (ReadOnly): State of the config server.

## ConfigServerSettings
### Properties
* **gitProperty**: [ConfigServerGitProperty](#configservergitproperty): Property of git.

## ConfigurationServiceGitProperty
### Properties
* **repositories**: [ConfigurationServiceGitRepository](#configurationservicegitrepository)[]: Repositories of Application Configuration Service git property.

## ConfigurationServiceGitRepository
### Properties
* **hostKey**: string: Public sshKey of git repository.
* **hostKeyAlgorithm**: string: SshKey algorithm of git repository.
* **label**: string (Required): Label of the repository
* **name**: string (Required): Name of the repository
* **password**: string: Password of git repository basic auth.
* **patterns**: string[] (Required): Collection of patterns of the repository
* **privateKey**: string: Private sshKey algorithm of git repository.
* **searchPaths**: string[]: Searching path of the repository
* **strictHostKeyChecking**: bool: Strict host key checking or not.
* **uri**: string (Required): URI of the repository
* **username**: string: Username of git repository basic auth.

## ConfigurationServiceInstance
### Properties
* **name**: string (ReadOnly): Name of the Application Configuration Service instance
* **status**: string (ReadOnly): Status of the Application Configuration Service instance

## ConfigurationServiceProperties
### Properties
* **instances**: [ConfigurationServiceInstance](#configurationserviceinstance)[] (ReadOnly): Collection of instances belong to Application Configuration Service.
* **provisioningState**: 'Creating' | 'Deleting' | 'Failed' | 'Succeeded' | 'Updating' | string (ReadOnly): State of the Application Configuration Service.
* **resourceRequests**: [ConfigurationServiceResourceRequests](#configurationserviceresourcerequests) (ReadOnly): Resource request payload of Application Configuration Service
* **settings**: [ConfigurationServiceSettings](#configurationservicesettings): The settings of Application Configuration Service.

## ConfigurationServiceResourceRequests
### Properties
* **cpu**: string (ReadOnly): Cpu allocated to each Application Configuration Service instance
* **instanceCount**: int (ReadOnly): Instance count of the Application Configuration Service
* **memory**: string (ReadOnly): Memory allocated to each Application Configuration Service instance

## ConfigurationServiceSettings
### Properties
* **gitProperty**: [ConfigurationServiceGitProperty](#configurationservicegitproperty): Property of git environment.

## CustomDomainProperties
### Properties
* **appName**: string (ReadOnly): The app name of domain.
* **certName**: string: The bound certificate name of domain.
* **thumbprint**: string: The thumbprint of bound certificate.

## DeploymentInstance
### Properties
* **discoveryStatus**: string (ReadOnly): Discovery status of the deployment instance
* **name**: string (ReadOnly): Name of the deployment instance
* **reason**: string (ReadOnly): Failed reason of the deployment instance
* **startTime**: string (ReadOnly): Start time of the deployment instance
* **status**: string (ReadOnly): Status of the deployment instance
* **zone**: string (ReadOnly): Availability zone information of the deployment instance

## DeploymentResourceProperties
### Properties
* **active**: bool: Indicates whether the Deployment is active
* **deploymentSettings**: [DeploymentSettings](#deploymentsettings): Deployment settings payload
* **instances**: [DeploymentInstance](#deploymentinstance)[] (ReadOnly): Collection of instances belong to the Deployment
* **provisioningState**: 'Creating' | 'Failed' | 'Succeeded' | 'Updating' | string (ReadOnly): Provisioning state of the Deployment
* **source**: [UserSourceInfo](#usersourceinfo): Source information for a deployment
* **status**: 'Running' | 'Stopped' | string (ReadOnly): Status of the Deployment

## DeploymentSettings
### Properties
* **addonConfigs**: [DeploymentSettingsAddonConfigs](#deploymentsettingsaddonconfigs): Collection of addons
* **environmentVariables**: [DeploymentSettingsEnvironmentVariables](#deploymentsettingsenvironmentvariables): Collection of environment variables
* **resourceRequests**: [ResourceRequests](#resourcerequests): Deployment resource request payload

## DeploymentSettingsAddonConfigs
### Properties
### Additional Properties
* **Additional Properties Type**: [AddonProfile](#addonprofile)

## DeploymentSettingsEnvironmentVariables
### Properties
### Additional Properties
* **Additional Properties Type**: string

## Error
### Properties
* **code**: string: The code of error.
* **message**: string: The message of error.

## GitPatternRepository
### Properties
* **hostKey**: string: Public sshKey of git repository.
* **hostKeyAlgorithm**: string: SshKey algorithm of git repository.
* **label**: string: Label of the repository
* **name**: string (Required): Name of the repository
* **password**: string: Password of git repository basic auth.
* **pattern**: string[]: Collection of pattern of the repository
* **privateKey**: string: Private sshKey algorithm of git repository.
* **searchPaths**: string[]: Searching path of the repository
* **strictHostKeyChecking**: bool: Strict host key checking or not.
* **uri**: string (Required): URI of the repository
* **username**: string: Username of git repository basic auth.

## LoadedCertificate
### Properties
* **loadTrustStore**: bool: Indicate whether the certificate will be loaded into default trust store, only work for Java runtime.
* **resourceId**: string (Required): Resource Id of loaded certificate

## ManagedIdentityProperties
### Properties
* **principalId**: string: Principal Id of system-assigned managed identity.
* **tenantId**: string: Tenant Id of system-assigned managed identity.
* **type**: 'None' | 'SystemAssigned' | 'SystemAssigned,UserAssigned' | 'UserAssigned' | string: Type of the managed identity

## MonitoringSettingProperties
### Properties
* **appInsightsAgentVersions**: [ApplicationInsightsAgentVersions](#applicationinsightsagentversions): Application Insights agent versions properties payload
* **appInsightsInstrumentationKey**: string: Target application insight instrumentation key, null or whitespace include empty will disable monitoringSettings
* **appInsightsSamplingRate**: int: Indicates the sampling rate of application insight agent, should be in range [0.0, 100.0]
* **error**: [Error](#error): The error code compose of code and message.
* **provisioningState**: 'Failed' | 'NotAvailable' | 'Succeeded' | 'Updating' | string (ReadOnly): State of the Monitoring Setting.
* **traceEnabled**: bool: Indicates whether enable the trace functionality, which will be deprecated since api version 2020-11-01-preview. Please leverage appInsightsInstrumentationKey to indicate if monitoringSettings enabled or not

## NetworkProfile
### Properties
* **appNetworkResourceGroup**: string: Name of the resource group containing network resources for customer apps in Azure Spring Apps
* **appSubnetId**: string: Fully qualified resource Id of the subnet to host customer apps in Azure Spring Apps
* **outboundIPs**: [NetworkProfileOutboundIPs](#networkprofileoutboundips) (ReadOnly): Desired outbound IP resources for Azure Spring Apps resource.
* **requiredTraffics**: [RequiredTraffic](#requiredtraffic)[] (ReadOnly): Required inbound or outbound traffics for Azure Spring Apps resource.
* **serviceCidr**: string: Azure Spring Apps service reserved CIDR
* **serviceRuntimeNetworkResourceGroup**: string: Name of the resource group containing network resources of Azure Spring Apps Service Runtime
* **serviceRuntimeSubnetId**: string: Fully qualified resource Id of the subnet to host Azure Spring Apps Service Runtime

## NetworkProfileOutboundIPs
### Properties
* **publicIPs**: string[] (ReadOnly): A list of public IP addresses.

## PersistentDisk
### Properties
* **mountPath**: string: Mount path of the persistent disk
* **sizeInGB**: int: Size of the persistent disk in GB
* **usedInGB**: int (ReadOnly): Size of the used persistent disk in GB

## RequiredTraffic
### Properties
* **direction**: 'Inbound' | 'Outbound' | string (ReadOnly): The direction of required traffic
* **fqdns**: string[] (ReadOnly): The FQDN list of required traffic
* **ips**: string[] (ReadOnly): The ip list of required traffic
* **port**: int (ReadOnly): The port of required traffic
* **protocol**: string (ReadOnly): The protocol of required traffic

## ResourceRequests
### Properties
* **cpu**: string: Required CPU. 1 core can be represented by 1 or 1000m. This should be 500m or 1 for Basic tier, and {500m, 1, 2, 3, 4} for Standard tier.
* **memory**: string: Required memory. 1 GB can be represented by 1Gi or 1024Mi. This should be {512Mi, 1Gi, 2Gi} for Basic tier, and {512Mi, 1Gi, 2Gi, ..., 8Gi} for Standard tier.

## ServiceRegistryInstance
### Properties
* **name**: string (ReadOnly): Name of the Service Registry instance
* **status**: string (ReadOnly): Status of the Service Registry instance

## ServiceRegistryProperties
### Properties
* **instances**: [ServiceRegistryInstance](#serviceregistryinstance)[] (ReadOnly): Collection of instances belong to Service Registry.
* **provisioningState**: 'Creating' | 'Deleting' | 'Failed' | 'Succeeded' | 'Updating' | string (ReadOnly): State of the Service Registry.
* **resourceRequests**: [ServiceRegistryResourceRequests](#serviceregistryresourcerequests) (ReadOnly): Resource request payload of Service Registry

## ServiceRegistryResourceRequests
### Properties
* **cpu**: string (ReadOnly): Cpu allocated to each Service Registry instance
* **instanceCount**: int (ReadOnly): Instance count of the Service Registry
* **memory**: string (ReadOnly): Memory allocated to each Service Registry instance

## Sku
### Properties
* **capacity**: int: Current capacity of the target resource
* **name**: string: Name of the Sku
* **tier**: string: Tier of the Sku

## StackProperties
### Properties
* **id**: string: Id of the ClusterStack.
* **version**: string: Version of the ClusterStack

## SystemData
### Properties
* **createdAt**: string: The timestamp of resource creation (UTC).
* **createdBy**: string: The identity that created the resource.
* **createdByType**: 'Application' | 'Key' | 'ManagedIdentity' | 'User' | string: The type of identity that created the resource.
* **lastModifiedAt**: string: The timestamp of resource modification (UTC).
* **lastModifiedBy**: string: The identity that last modified the resource.
* **lastModifiedByType**: 'Application' | 'Key' | 'ManagedIdentity' | 'User' | string: The type of identity that last modified the resource.

## TemporaryDisk
### Properties
* **mountPath**: string: Mount path of the temporary disk
* **sizeInGB**: int: Size of the temporary disk in GB

## TestKeys
### Properties
* **enabled**: bool (ReadOnly): Indicates whether the test endpoint feature enabled or not
* **primaryKey**: string (ReadOnly): Primary key
* **primaryTestEndpoint**: string (ReadOnly): Primary test endpoint
* **secondaryKey**: string (ReadOnly): Secondary key
* **secondaryTestEndpoint**: string (ReadOnly): Secondary test endpoint

## TrackedResourceTags
### Properties
### Additional Properties
* **Additional Properties Type**: string

## TriggeredBuildResult
### Properties
* **id**: string: The unique build id of this build result

## UserSourceInfo
* **Discriminator**: type

### Base Properties
* **version**: string: Version of the source
### BuildResultUserSourceInfo
#### Properties
* **buildResultId**: string: Resource id of an existing succeeded build result under the same Spring instance.
* **type**: 'BuildResult' (Required): Type of the source uploaded

### JarUploadedUserSourceInfo
#### Properties
* **jvmOptions**: string: JVM parameter
* **runtimeVersion**: string: Runtime version of the Jar file
* **type**: 'Jar' (Required): Type of the source uploaded

### NetCoreZipUploadedUserSourceInfo
#### Properties
* **netCoreMainEntryPath**: string: The path to the .NET executable relative to zip root
* **runtimeVersion**: string: Runtime version of the .Net file
* **type**: 'NetCoreZip' (Required): Type of the source uploaded

### SourceUploadedUserSourceInfo
#### Properties
* **artifactSelector**: string: Selector for the artifact to be used for the deployment for multi-module projects. This should be
the relative path to the target module/project.
* **runtimeVersion**: string: Runtime version of the source file
* **type**: 'Source' (Required): Type of the source uploaded

