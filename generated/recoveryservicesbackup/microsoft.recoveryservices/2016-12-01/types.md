# Microsoft.RecoveryServices @ 2016-12-01

## Resource Microsoft.RecoveryServices/vaults/backupEngines@2016-12-01 (ReadOnly)
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2016-12-01' (ReadOnly, DeployTimeConstant): The resource api version
* **eTag**: string (ReadOnly): Optional ETag.
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **location**: string (ReadOnly): Resource location.
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [BackupEngineBase](#backupenginebase) (ReadOnly): BackupEngineBaseResource properties
* **tags**: [ResourceTags](#resourcetags) (ReadOnly): Resource tags.
* **type**: 'Microsoft.RecoveryServices/vaults/backupEngines' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.RecoveryServices/vaults/backupFabrics/protectionContainers@2016-12-01
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2016-12-01' (ReadOnly, DeployTimeConstant): The resource api version
* **eTag**: string: Optional ETag.
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **location**: string: Resource location.
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [ProtectionContainer](#protectioncontainer): ProtectionContainerResource properties
* **tags**: [ResourceTags](#resourcetags): Resource tags.
* **type**: 'Microsoft.RecoveryServices/vaults/backupFabrics/protectionContainers' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.RecoveryServices/vaults/backupFabrics/protectionContainers/operationResults@2016-12-01 (ReadOnly)
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2016-12-01' (ReadOnly, DeployTimeConstant): The resource api version
* **eTag**: string (ReadOnly): Optional ETag.
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **location**: string (ReadOnly): Resource location.
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [ProtectionContainer](#protectioncontainer) (ReadOnly): ProtectionContainerResource properties
* **tags**: [ResourceTags](#resourcetags) (ReadOnly): Resource tags.
* **type**: 'Microsoft.RecoveryServices/vaults/backupFabrics/protectionContainers/operationResults' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.RecoveryServices/vaults/backupstorageconfig@2016-12-01
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2016-12-01' (ReadOnly, DeployTimeConstant): The resource api version
* **eTag**: string: Optional ETag.
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **location**: string: Resource location.
* **name**: 'vaultstorageconfig' (Required, DeployTimeConstant): The resource name
* **properties**: [BackupResourceConfig](#backupresourceconfig): BackupResourceConfigResource properties
* **tags**: [ResourceTags](#resourcetags): Resource tags.
* **type**: 'Microsoft.RecoveryServices/vaults/backupstorageconfig' (ReadOnly, DeployTimeConstant): The resource type

## AzureWorkloadContainerExtendedInfo
### Properties
* **hostServerName**: string: Host Os Name in case of Stand Alone and Cluster Name in case of distributed container.
* **inquiryInfo**: [InquiryInfo](#inquiryinfo): Inquiry Status for the container.
* **nodesList**: [DistributedNodesInfo](#distributednodesinfo)[]: List of the nodes in case of distributed container.

## BackupEngineBase
* **Discriminator**: backupEngineType

### Base Properties
* **azureBackupAgentVersion**: string: Backup agent version
* **backupEngineId**: string: ID of the backup engine.
* **backupEngineState**: string: Status of the backup engine with the Recovery Services Vault. = {Active/Deleting/DeleteFailed}
* **backupManagementType**: 'AzureBackupServer' | 'AzureIaasVM' | 'AzureSql' | 'AzureStorage' | 'AzureWorkload' | 'DPM' | 'DefaultBackup' | 'Invalid' | 'MAB' | string: Type of backup management for the backup engine.
* **canReRegister**: bool: Flag indicating if the backup engine be registered, once already registered.
* **dpmVersion**: string: Backup engine version
* **extendedInfo**: [BackupEngineExtendedInfo](#backupengineextendedinfo): Extended info of the backupengine
* **friendlyName**: string: Friendly name of the backup engine.
* **healthStatus**: string: Backup status of the backup engine.
* **isAzureBackupAgentUpgradeAvailable**: bool: To check if backup agent upgrade available
* **isDpmUpgradeAvailable**: bool: To check if backup engine upgrade available
* **registrationStatus**: string: Registration status of the backup engine with the Recovery Services Vault.

### AzureBackupServerEngine
#### Properties
* **backupEngineType**: 'AzureBackupServerEngine' (Required): Type of the backup engine.

### DpmBackupEngine
#### Properties
* **backupEngineType**: 'DpmBackupEngine' (Required): Type of the backup engine.


## BackupEngineExtendedInfo
### Properties
* **availableDiskSpace**: int: Disk space currently available in the backup engine.
* **azureProtectedInstances**: int: Protected instances in the backup engine.
* **databaseName**: string: Database name of backup engine.
* **diskCount**: int: Number of disks in the backup engine.
* **protectedItemsCount**: int: Number of protected items in the backup engine.
* **protectedServersCount**: int: Number of protected servers in the backup engine.
* **refreshedAt**: string: Last refresh time in the backup engine.
* **usedDiskSpace**: int: Disk space used in the backup engine.

## BackupResourceConfig
### Properties
* **storageModelType**: 'GeoRedundant' | 'Invalid' | 'LocallyRedundant' | string: Storage type
* **storageType**: 'GeoRedundant' | 'Invalid' | 'LocallyRedundant' | string: Storage type.
* **storageTypeState**: 'Invalid' | 'Locked' | 'Unlocked' | string: Locked or Unlocked. Once a machine is registered against a resource, the storageTypeState is always Locked.

## ContainerIdentityInfo
### Properties
* **aadTenantId**: string: Protection container identity - AAD Tenant
* **audience**: string: Protection container identity - Audience
* **servicePrincipalClientId**: string: Protection container identity - AAD Service Principal
* **uniqueName**: string: Unique name of the container

## DistributedNodesInfo
### Properties
* **errorDetail**: [ErrorDetail](#errordetail): Error Details if the Status is non-success.
* **nodeName**: string: Name of the node under a distributed container.
* **status**: string: Status of this Node.
Failed | Succeeded

## DPMContainerExtendedInfo
### Properties
* **lastRefreshedAt**: string: Last refresh time of the DPMContainer.

## ErrorDetail
### Properties
* **code**: string (ReadOnly): Error code.
* **message**: string (ReadOnly): Error Message related to the Code.
* **recommendations**: string[] (ReadOnly): List of recommendation strings.

## GenericContainerExtendedInfo
### Properties
* **containerIdentityInfo**: [ContainerIdentityInfo](#containeridentityinfo): Container identity information
* **rawCertData**: string: Public key of container cert
* **serviceEndpoints**: [GenericContainerExtendedInfoServiceEndpoints](#genericcontainerextendedinfoserviceendpoints): Azure Backup Service Endpoints for the container

## GenericContainerExtendedInfoServiceEndpoints
### Properties
### Additional Properties
* **Additional Properties Type**: string

## InquiryInfo
### Properties
* **errorDetail**: [ErrorDetail](#errordetail): Error Details if the Status is non-success.
* **inquiryDetails**: [WorkloadInquiryDetails](#workloadinquirydetails)[]: Inquiry Details which will have workload specific details.
For e.g. - For SQL and oracle this will contain different details.
* **status**: string: Inquiry Status for this container such as
InProgress | Failed | Succeeded

## InquiryValidation
### Properties
* **additionalDetail**: string (ReadOnly): Error Additional Detail in case the status is non-success.
* **errorDetail**: [ErrorDetail](#errordetail): Error Detail in case the status is non-success.
* **status**: string: Status for the Inquiry Validation.

## MabContainerExtendedInfo
### Properties
* **backupItems**: string[]: List of backup items associated with this container.
* **backupItemType**: 'AzureFileShare' | 'AzureSqlDb' | 'Client' | 'Exchange' | 'FileFolder' | 'GenericDataSource' | 'Invalid' | 'SAPAseDatabase' | 'SAPHanaDatabase' | 'SQLDB' | 'SQLDataBase' | 'Sharepoint' | 'SystemState' | 'VM' | 'VMwareVM' | string: Type of backup items associated with this container.
* **lastBackupStatus**: string: Latest backup status of this container.
* **lastRefreshedAt**: string: Time stamp when this container was refreshed.
* **policyName**: string: Backup policy associated with this container.

## MABContainerHealthDetails
### Properties
* **code**: int: Health Code
* **message**: string: Health Message
* **recommendations**: string[]: Health Recommended Actions
* **title**: string: Health Title

## ProtectionContainer
* **Discriminator**: containerType

### Base Properties
* **backupManagementType**: 'AzureBackupServer' | 'AzureIaasVM' | 'AzureSql' | 'AzureStorage' | 'AzureWorkload' | 'DPM' | 'DefaultBackup' | 'Invalid' | 'MAB' | string: Type of backup management for the container.
* **friendlyName**: string: Friendly name of the container.
* **healthStatus**: string: Status of health of the container.
* **registrationStatus**: string: Status of registration of the container with the Recovery Services Vault.

### AzureBackupServerContainer
#### Properties
* **canReRegister**: bool: Specifies whether the container is re-registrable.
* **containerId**: string: ID of container.
* **containerType**: 'AzureBackupServerContainer' (Required): Type of the container. The value of this property for: 1. Compute Azure VM is Microsoft.Compute/virtualMachines 2.
Classic Compute Azure VM is Microsoft.ClassicCompute/virtualMachines 3. Windows machines (like MAB, DPM etc) is
Windows 4. Azure SQL instance is AzureSqlContainer. 5. Storage containers is StorageContainer. 6. Azure workload
Backup is VMAppContainer
* **dpmAgentVersion**: string: Backup engine Agent version
* **dpmServers**: string[]: List of BackupEngines protecting the container
* **extendedInfo**: [DPMContainerExtendedInfo](#dpmcontainerextendedinfo): Extended Info of the container.
* **protectedItemCount**: int: Number of protected items in the BackupEngine
* **protectionStatus**: string: Protection status of the container.
* **upgradeAvailable**: bool: To check if upgrade available

### AzureSqlContainer
#### Properties
* **containerType**: 'AzureSqlContainer' (Required): Type of the container. The value of this property for: 1. Compute Azure VM is Microsoft.Compute/virtualMachines 2.
Classic Compute Azure VM is Microsoft.ClassicCompute/virtualMachines 3. Windows machines (like MAB, DPM etc) is
Windows 4. Azure SQL instance is AzureSqlContainer. 5. Storage containers is StorageContainer. 6. Azure workload
Backup is VMAppContainer

### GenericContainer
#### Properties
* **containerType**: 'GenericContainer' (Required): Type of the container. The value of this property for: 1. Compute Azure VM is Microsoft.Compute/virtualMachines 2.
Classic Compute Azure VM is Microsoft.ClassicCompute/virtualMachines 3. Windows machines (like MAB, DPM etc) is
Windows 4. Azure SQL instance is AzureSqlContainer. 5. Storage containers is StorageContainer. 6. Azure workload
Backup is VMAppContainer
* **extendedInformation**: [GenericContainerExtendedInfo](#genericcontainerextendedinfo): Extended information (not returned in List container API calls)
* **fabricName**: string: Name of the container's fabric

### AzureIaaSClassicComputeVMContainer
#### Properties
* **containerType**: 'Microsoft.ClassicCompute/virtualMachines' (Required): Type of the container. The value of this property for: 1. Compute Azure VM is Microsoft.Compute/virtualMachines 2.
Classic Compute Azure VM is Microsoft.ClassicCompute/virtualMachines 3. Windows machines (like MAB, DPM etc) is
Windows 4. Azure SQL instance is AzureSqlContainer. 5. Storage containers is StorageContainer. 6. Azure workload
Backup is VMAppContainer
* **resourceGroup**: string: Resource group name of Recovery Services Vault.
* **virtualMachineId**: string: Fully qualified ARM url of the virtual machine represented by this Azure IaaS VM container.
* **virtualMachineVersion**: string: Specifies whether the container represents a Classic or an Azure Resource Manager VM.

### AzureIaaSComputeVMContainer
#### Properties
* **containerType**: 'Microsoft.Compute/virtualMachines' (Required): Type of the container. The value of this property for: 1. Compute Azure VM is Microsoft.Compute/virtualMachines 2.
Classic Compute Azure VM is Microsoft.ClassicCompute/virtualMachines 3. Windows machines (like MAB, DPM etc) is
Windows 4. Azure SQL instance is AzureSqlContainer. 5. Storage containers is StorageContainer. 6. Azure workload
Backup is VMAppContainer
* **resourceGroup**: string: Resource group name of Recovery Services Vault.
* **virtualMachineId**: string: Fully qualified ARM url of the virtual machine represented by this Azure IaaS VM container.
* **virtualMachineVersion**: string: Specifies whether the container represents a Classic or an Azure Resource Manager VM.

### AzureSqlagWorkloadContainerProtectionContainer
#### Properties
* **containerType**: 'SQLAGWorkLoadContainer' (Required): Type of the container. The value of this property for: 1. Compute Azure VM is Microsoft.Compute/virtualMachines 2.
Classic Compute Azure VM is Microsoft.ClassicCompute/virtualMachines 3. Windows machines (like MAB, DPM etc) is
Windows 4. Azure SQL instance is AzureSqlContainer. 5. Storage containers is StorageContainer. 6. Azure workload
Backup is VMAppContainer
* **extendedInfo**: [AzureWorkloadContainerExtendedInfo](#azureworkloadcontainerextendedinfo): Additional details of a workload container.
* **lastUpdatedTime**: string: Time stamp when this container was updated.
* **operationType**: 'Invalid' | 'Register' | 'Reregister' | string: Re-Do Operation
* **sourceResourceId**: string: ARM ID of the virtual machine represented by this Azure Workload Container
* **workloadType**: 'AzureFileShare' | 'AzureSqlDb' | 'Client' | 'Exchange' | 'FileFolder' | 'GenericDataSource' | 'Invalid' | 'SAPAseDatabase' | 'SAPHanaDatabase' | 'SQLDB' | 'SQLDataBase' | 'Sharepoint' | 'SystemState' | 'VM' | 'VMwareVM' | string: Workload type for which registration was sent.

### AzureStorageContainer
#### Properties
* **containerType**: 'StorageContainer' (Required): Type of the container. The value of this property for: 1. Compute Azure VM is Microsoft.Compute/virtualMachines 2.
Classic Compute Azure VM is Microsoft.ClassicCompute/virtualMachines 3. Windows machines (like MAB, DPM etc) is
Windows 4. Azure SQL instance is AzureSqlContainer. 5. Storage containers is StorageContainer. 6. Azure workload
Backup is VMAppContainer
* **protectedItemCount**: int: Number of items backed up in this container.
* **resourceGroup**: string: Resource group name of Recovery Services Vault.
* **sourceResourceId**: string: Fully qualified ARM url.
* **storageAccountVersion**: string: Storage account version.

### AzureVMAppContainerProtectionContainer
#### Properties
* **containerType**: 'VMAppContainer' (Required): Type of the container. The value of this property for: 1. Compute Azure VM is Microsoft.Compute/virtualMachines 2.
Classic Compute Azure VM is Microsoft.ClassicCompute/virtualMachines 3. Windows machines (like MAB, DPM etc) is
Windows 4. Azure SQL instance is AzureSqlContainer. 5. Storage containers is StorageContainer. 6. Azure workload
Backup is VMAppContainer
* **extendedInfo**: [AzureWorkloadContainerExtendedInfo](#azureworkloadcontainerextendedinfo): Additional details of a workload container.
* **lastUpdatedTime**: string: Time stamp when this container was updated.
* **operationType**: 'Invalid' | 'Register' | 'Reregister' | string: Re-Do Operation
* **sourceResourceId**: string: ARM ID of the virtual machine represented by this Azure Workload Container
* **workloadType**: 'AzureFileShare' | 'AzureSqlDb' | 'Client' | 'Exchange' | 'FileFolder' | 'GenericDataSource' | 'Invalid' | 'SAPAseDatabase' | 'SAPHanaDatabase' | 'SQLDB' | 'SQLDataBase' | 'Sharepoint' | 'SystemState' | 'VM' | 'VMwareVM' | string: Workload type for which registration was sent.

### MabContainer
#### Properties
* **agentVersion**: string: Agent version of this container.
* **canReRegister**: bool: Can the container be registered one more time.
* **containerHealthState**: string: Health state of mab container.
* **containerId**: int: ContainerID represents the container.
* **containerType**: 'Windows' (Required): Type of the container. The value of this property for: 1. Compute Azure VM is Microsoft.Compute/virtualMachines 2.
Classic Compute Azure VM is Microsoft.ClassicCompute/virtualMachines 3. Windows machines (like MAB, DPM etc) is
Windows 4. Azure SQL instance is AzureSqlContainer. 5. Storage containers is StorageContainer. 6. Azure workload
Backup is VMAppContainer
* **extendedInfo**: [MabContainerExtendedInfo](#mabcontainerextendedinfo): Additional information for this container
* **mabContainerHealthDetails**: [MABContainerHealthDetails](#mabcontainerhealthdetails)[]: Health details on this mab container.
* **protectedItemCount**: int: Number of items backed up in this container.


## ResourceTags
### Properties
### Additional Properties
* **Additional Properties Type**: string

## ResourceTags
### Properties
### Additional Properties
* **Additional Properties Type**: string

## ResourceTags
### Properties
### Additional Properties
* **Additional Properties Type**: string

## ResourceTags
### Properties
### Additional Properties
* **Additional Properties Type**: string

## WorkloadInquiryDetails
### Properties
* **inquiryValidation**: [InquiryValidation](#inquiryvalidation): Inquiry validation such as permissions and other backup validations.
* **itemCount**: int: Contains the protectable item Count inside this Container.
* **type**: string: Type of the Workload such as SQL, Oracle etc.

