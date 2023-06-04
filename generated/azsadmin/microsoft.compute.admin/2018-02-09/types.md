# Microsoft.Compute.Admin @ 2018-02-09

## Resource Microsoft.Compute.Admin/locations/artifactTypes/publishers/offers/skus/versions@2018-02-09
* **Valid Scope(s)**: Subscription
### Properties
* **apiVersion**: '2018-02-09' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **location**: string (ReadOnly): Location of the resource.
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [PlatformImageProperties](#platformimageproperties): Platform image properties.
* **type**: 'Microsoft.Compute.Admin/locations/artifactTypes/publishers/offers/skus/versions' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.Compute.Admin/locations/artifactTypes/publishers/types/versions@2018-02-09
* **Valid Scope(s)**: Subscription
### Properties
* **apiVersion**: '2018-02-09' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **location**: string (ReadOnly): Location of the resource.
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [VMExtensionProperties](#vmextensionproperties): Properties of a Virtual Machine Extension Image.
* **type**: 'Microsoft.Compute.Admin/locations/artifactTypes/publishers/types/versions' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.Compute.Admin/locations/computeScaleUnits@2018-02-09 (ReadOnly)
* **Valid Scope(s)**: Subscription
### Properties
* **apiVersion**: '2018-02-09' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **location**: string (ReadOnly): Location of the resource.
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [ScaleUnitProperties](#scaleunitproperties) (ReadOnly): The scale unit operator view properties.
* **type**: 'Microsoft.Compute.Admin/locations/computeScaleUnits' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.Compute.Admin/locations/diskmigrationjobs@2018-02-09
* **Valid Scope(s)**: Subscription
### Properties
* **apiVersion**: '2018-02-09' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **location**: string (ReadOnly): Location of the resource.
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [DiskMigrationJobProperties](#diskmigrationjobproperties) (ReadOnly): Disk migration properties.
* **type**: 'Microsoft.Compute.Admin/locations/diskmigrationjobs' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.Compute.Admin/locations/disks@2018-02-09 (ReadOnly)
* **Valid Scope(s)**: Subscription
### Properties
* **apiVersion**: '2018-02-09' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **location**: string (ReadOnly): Location of the resource.
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [DiskProperties](#diskproperties) (ReadOnly): Disk properties.
* **type**: 'Microsoft.Compute.Admin/locations/disks' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.Compute.Admin/locations/features@2018-02-09 (ReadOnly)
* **Valid Scope(s)**: Subscription
### Properties
* **apiVersion**: '2018-02-09' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **location**: string (ReadOnly): Location of the resource.
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [FeatureProperties](#featureproperties) (ReadOnly): Feature properties.
* **type**: 'Microsoft.Compute.Admin/locations/features' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.Compute.Admin/locations/quotas@2018-02-09
* **Valid Scope(s)**: Subscription
### Properties
* **apiVersion**: '2018-02-09' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **location**: string: Location of the resource.
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [QuotaPropertiesAutoGenerated](#quotapropertiesautogenerated): Compute Quota properties.
* **type**: 'Microsoft.Compute.Admin/locations/quotas' (ReadOnly, DeployTimeConstant): The resource type

## AzureBlob
### Properties
* **uri**: string: URI to Azure or AzureStack blob.

## DataDisk
### Properties
* **lun**: int: Logical unit number.
* **uri**: string: Location of the disk template.

## DiskMigrationJobProperties
### Properties
* **creationTime**: string (ReadOnly): The job creation time.
* **endTime**: string (ReadOnly): The job end time.
* **migrationId**: string: The disk migration id.
* **startTime**: string (ReadOnly): The job start time.
* **status**: 'Canceled' | 'Failed' | 'Pending' | 'Running' | 'Succeeded' | 'Undefined' | string (ReadOnly): The current status of disk migration job.
* **subtasks**: [MigrationSubTask](#migrationsubtask)[] (ReadOnly): The list of child migration tasks.
* **targetShare**: string (ReadOnly): The target share of migration job.

## DiskProperties
### Properties
* **actualSizeGB**: int (ReadOnly): The actual size of disk in GB.
* **creationOption**: 'Copy' | 'Empty' | 'FromImage' | 'FromPreprovisioned' | 'Import' | 'RecoverFromBlob' | 'Restore' | 'Undelete' | 'Upload' | string (ReadOnly): The disk creation option.
* **creationSourceUri**: string (ReadOnly): The disk creation source uri.
* **diskId**: string: The disk id.
* **diskSku**: 'Premium_LRS' | 'StandardSSD_LRS' | 'Standard_GRS' | 'Standard_LRS' | 'Standard_RAGRS' | 'Standard_ZRS' | 'UltraSSD_LRS' | string (ReadOnly): the disk sku.
* **diskType**: 'Disk' | 'ManagedBlob' | 'RestorePoint' | 'Snapshot' | 'Undefined' | string (ReadOnly): The type of the disk resource.
* **exclusiveAllocatedSize**: int (ReadOnly): The exclusive allocated size for the disk.
* **managedBy**: string (ReadOnly): Compute resource Uri which owns this disk.
* **provisionSizeGB**: int (ReadOnly): The provision size of disk in GB.
* **sharePath**: string: The disk share path.
* **status**: 'ActiveSAS' | 'All' | 'Attached' | 'OfflineMigration' | 'OnlineMigration' | 'Recommended' | 'Reserved' | 'Unattached' | 'Undefined' | 'Unknown' | string: The disk status.
* **userResourceId**: string (ReadOnly): The disk resource Uri from user view.

## FeatureProperties
### Properties
* **enabledTenantSubscriptionIds**: string[]: List of subscription identifiers which have the feature enabled.
* **featureName**: string: The name of the feature.
* **globalFeatureSettings**: [GlobalFeatureSettings](#globalfeaturesettings): Higher-priority global feature flags.

## GlobalFeatureSettings
### Properties
* **globalFeatureState**: 'Disabled' | 'Enabled' | 'TenantSubscriptionLevel': The state of the global feature.

## ImageDetails
### Properties
* **billingPartNumber**: string: The part number is used to bill for software costs.

## MigrationSubTask
### Properties
* **migrationSubTaskId**: string (ReadOnly): The id of migration child task.
* **properties**: [MigrationSubTaskProperties](#migrationsubtaskproperties): Disk migration child task properties.

## MigrationSubTaskProperties
### Properties
* **diskId**: string (ReadOnly): The id of disk.
* **endTime**: string (ReadOnly): The task end time.
* **migrationSubtaskStatus**: 'Canceled' | 'Failed' | 'Pending' | 'Running' | 'Skipped' | 'Succeeded' | 'Undefined' | string (ReadOnly): The disk migration child task status.
* **progress**: string (ReadOnly): The progress of migration sub task which measures the percent of content migrated.
* **reason**: string (ReadOnly): The reason of task failure.
* **sourceShare**: string (ReadOnly): The source share of migration task.
* **startTime**: string (ReadOnly): The task start time.
* **targetDiskStateForMigration**: 'ActiveSAS' | 'All' | 'Attached' | 'OfflineMigration' | 'OnlineMigration' | 'Recommended' | 'Reserved' | 'Unattached' | 'Undefined' | 'Unknown' | string (ReadOnly): The disk status.
* **targetShare**: string (ReadOnly): The target share of migration task.

## NodeView
### Properties
* **lastUpdatedTime**: string: The node last update time (UTC).
* **nodeHealthState**: 'Down' | 'MaintenanceMode' | 'Unknown' | 'Up': The node health state.
* **nodeName**: string: The name of the node.
* **virtualMachines**: [VirtualMachineView](#virtualmachineview)[]: The virtual machines on the node.

## OsDisk
### Properties
* **osType**: 'Linux' | 'Unknown' | 'Windows': Operating system type.
* **uri**: string: Location of the disk.

## PlatformImageProperties
### Properties
* **dataDisks**: [DataDisk](#datadisk)[]: Data disks used by the platform image.
* **details**: [ImageDetails](#imagedetails): Information about the image.
* **osDisk**: [OsDisk](#osdisk): Operating system used for this platform image.
* **provisioningState**: 'Canceled' | 'Creating' | 'Failed' | 'Succeeded': Provisioning status of the platform image.

## QuotaPropertiesAutoGenerated
### Properties
* **availabilitySetCount**: int: Maximum number of availability sets allowed.
* **coresLimit**: int: Maximum number of cores allowed.
* **ddagpuCount**: int: Maximum number of dda gpus allowed.
* **maxAllocationPremiumManagedDisksAndSnapshots**: int: Maximum number of managed disks and snapshots of type premium allowed.
* **maxAllocationStandardManagedDisksAndSnapshots**: int: Maximum number of managed disks and snapshots of type standard allowed.
* **partitionedGpuCount**: int: Maximum number of partitioned gpus allowed.
* **virtualMachineCount**: int: Maximum number of virtual machines allowed.
* **vmScaleSetCount**: int: Maximum number of scale sets allowed.

## ScaleUnitProperties
### Properties
* **lastUpdatedTime**: string: The scale unit last update time (UTC).
* **nodes**: [NodeView](#nodeview)[]: The nodes of the scale unit.
* **scaleUnitName**: string: The name of the scale unit.

## VirtualMachineView
### Properties
* **lastProvisioningErrorMessage**: string: The virtual machine last provisioning error message.
* **powerState**: 'Paused' | 'Pausing' | 'Resuming' | 'Running' | 'SavedState' | 'Saving' | 'Starting' | 'Stopped' | 'Stopping' | 'Unknown': The fabric VM power state.
* **resourceGroupName**: string: The resource group name.
* **subscriptionId**: string: The identifier of the subscription.
* **timeOfLastConfigurationChange**: string: The time of last configuration change (UTC).
* **vmId**: string: The identifier of the virtual machine.
* **vmName**: string: The name of the virtual machine.
* **vmScaleSetName**: string: The virtual machine scale set name.
* **vmSize**: string: The virtual machine size.

## VMExtensionProperties
### Properties
* **computeRole**: string: Compute role
* **isSystemExtension**: bool: Indicates if the extension is for the system.
* **provisioningState**: 'Canceled' | 'Creating' | 'Failed' | 'Succeeded': Provisioning state of extension.
* **publisher**: string: The publisher of the VM Extension
* **sourceBlob**: [AzureBlob](#azureblob): URI to Azure or AzureStack blob.
* **supportMultipleExtensions**: bool: True if supports multiple extensions.
* **vmOsType**: 'Linux' | 'Unknown' | 'Windows': Target virtual machine operating system type necessary for deploying the extension handler.
* **vmScaleSetEnabled**: bool: Value indicating whether the extension is enabled for virtual machine scale set support.
