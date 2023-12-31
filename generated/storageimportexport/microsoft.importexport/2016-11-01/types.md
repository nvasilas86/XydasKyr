# Microsoft.ImportExport @ 2016-11-01

## Resource Microsoft.ImportExport/jobs@2016-11-01
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2016-11-01' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **identity**: [IdentityDetails](#identitydetails) (ReadOnly): Specifies the job identity details
* **location**: string: Specifies the supported Azure location where the job should be created
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [JobDetails](#jobdetails): Specifies the job properties
* **systemData**: [SystemData](#systemdata) (ReadOnly): SystemData of ImportExport Jobs.
* **tags**: any: Specifies the tags that will be assigned to the job.
* **type**: 'Microsoft.ImportExport/jobs' (ReadOnly, DeployTimeConstant): The resource type

## Function listBitLockerKeys (Microsoft.ImportExport/jobs@2016-11-01)
* **Resource**: Microsoft.ImportExport/jobs
* **ApiVersion**: 2016-11-01
* **Output**: [GetBitLockerKeysResponse](#getbitlockerkeysresponse)

## DeliveryPackageInformation
### Properties
* **carrierName**: string (Required): The name of the carrier that is used to ship the import or export drives.
* **driveCount**: int: The number of drives included in the package.
* **shipDate**: string: The date when the package is shipped.
* **trackingNumber**: string (Required): The tracking number of the package.

## DriveBitLockerKey
### Properties
* **bitLockerKey**: string: BitLocker recovery key or password
* **driveId**: string: Drive ID

## DriveStatus
### Properties
* **bitLockerKey**: string: The BitLocker key used to encrypt the drive.
* **bytesSucceeded**: int: Bytes successfully transferred for the drive.
* **copyStatus**: string: Detailed status about the data transfer process. This field is not returned in the response until the drive is in the Transferring state.
* **driveHeaderHash**: string: The drive header hash value.
* **driveId**: string: The drive's hardware serial number, without spaces.
* **errorLogUri**: string: A URI that points to the blob containing the error log for the data transfer operation.
* **manifestFile**: string: The relative path of the manifest file on the drive.
* **manifestHash**: string: The Base16-encoded MD5 hash of the manifest file on the drive.
* **manifestUri**: string: A URI that points to the blob containing the drive manifest file.
* **percentComplete**: int: Percentage completed for the drive.
* **state**: 'Completed' | 'CompletedMoreInfo' | 'NeverReceived' | 'Received' | 'ShippedBack' | 'Specified' | 'Transferring' | string: The drive's current state.
* **verboseLogUri**: string: A URI that points to the blob containing the verbose log for the data transfer operation.

## EncryptionKeyDetails
### Properties
* **kekType**: 'CustomerManaged' | 'MicrosoftManaged' | string: The type of kek encryption key
* **kekUrl**: string: Specifies the url for kek encryption key.
* **kekVaultResourceID**: string: Specifies the keyvault resource id for kek encryption key.

## Export
### Properties
* **blobList**: [ExportBlobList](#exportbloblist): A list of the blobs to be exported.
* **blobListBlobPath**: string: The relative URI to the block blob that contains the list of blob paths or blob path prefixes as defined above, beginning with the container name. If the blob is in root container, the URI must begin with $root.

## ExportBlobList
### Properties
* **blobPath**: string[]: A collection of blob-path strings.
* **blobPathPrefix**: string[]: A collection of blob-prefix strings.

## GetBitLockerKeysResponse
### Properties
* **value**: [DriveBitLockerKey](#drivebitlockerkey)[]: drive status

## IdentityDetails
### Properties
* **principalId**: string (ReadOnly): Specifies the principal id for the identity for the job.
* **tenantId**: string (ReadOnly): Specifies the tenant id for the identity for the job.
* **type**: 'None' | 'SystemAssigned' | 'UserAssigned' | string: The type of identity

## JobDetails
### Properties
* **backupDriveManifest**: bool: Default value is false. Indicates whether the manifest files on the drives should be copied to block blobs.
* **cancelRequested**: bool: Indicates whether a request has been submitted to cancel the job.
* **deliveryPackage**: [DeliveryPackageInformation](#deliverypackageinformation): Contains information about the package being shipped by the customer to the Microsoft data center.
* **diagnosticsPath**: string: The virtual blob directory to which the copy logs and backups of drive manifest files (if enabled) will be stored.
* **driveList**: [DriveStatus](#drivestatus)[]: List of up to ten drives that comprise the job. The drive list is a required element for an import job; it is not specified for export jobs.
* **encryptionKey**: [EncryptionKeyDetails](#encryptionkeydetails): Contains information about the encryption key.
* **export**: [Export](#export): A property containing information about the blobs to be exported for an export job. This property is included for export jobs only.
* **incompleteBlobListUri**: string: A blob path that points to a block blob containing a list of blob names that were not exported due to insufficient drive space. If all blobs were exported successfully, then this element is not included in the response.
* **jobType**: string: The type of job
* **logLevel**: string: Default value is Error. Indicates whether error logging or verbose logging will be enabled.
* **percentComplete**: int: Overall percentage completed for the job.
* **provisioningState**: string: Specifies the provisioning state of the job.
* **returnAddress**: [ReturnAddress](#returnaddress): Specifies the return address information for the job.
* **returnPackage**: [PackageInfomation](#packageinfomation): Contains information about the package being shipped from the Microsoft data center to the customer to return the drives. The format is the same as the deliveryPackage property above. This property is not included if the drives have not yet been returned.
* **returnShipping**: [ReturnShipping](#returnshipping): Specifies the return carrier and customer's account with the carrier.
* **shippingInformation**: [ShippingInformation](#shippinginformation): Contains information about the Microsoft datacenter to which the drives should be shipped.
* **state**: string: Current state of the job.
* **storageAccountId**: string: The resource identifier of the storage account where data will be imported to or exported from.

## PackageInfomation
### Properties
* **carrierName**: string (Required): The name of the carrier that is used to ship the import or export drives.
* **driveCount**: int (Required): The number of drives included in the package.
* **shipDate**: string (Required): The date when the package is shipped.
* **trackingNumber**: string (Required): The tracking number of the package.

## ReturnAddress
### Properties
* **city**: string (Required): The city name to use when returning the drives.
* **countryOrRegion**: string (Required): The country or region to use when returning the drives.
* **email**: string (Required): Email address of the recipient of the returned drives.
* **phone**: string (Required): Phone number of the recipient of the returned drives.
* **postalCode**: string (Required): The postal code to use when returning the drives.
* **recipientName**: string (Required): The name of the recipient who will receive the hard drives when they are returned.
* **stateOrProvince**: string: The state or province to use when returning the drives.
* **streetAddress1**: string (Required): The first line of the street address to use when returning the drives.
* **streetAddress2**: string: The second line of the street address to use when returning the drives.

## ReturnShipping
### Properties
* **carrierAccountNumber**: string (Required): The customer's account number with the carrier.
* **carrierName**: string (Required): The carrier's name.

## ShippingInformation
### Properties
* **additionalInformation**: string (ReadOnly): Additional shipping information for customer, specific to datacenter to which customer should send their disks.
* **city**: string: The city name to use when returning the drives.
* **countryOrRegion**: string: The country or region to use when returning the drives.
* **phone**: string: Phone number of the recipient of the returned drives.
* **postalCode**: string: The postal code to use when returning the drives.
* **recipientName**: string: The name of the recipient who will receive the hard drives when they are returned.
* **stateOrProvince**: string: The state or province to use when returning the drives.
* **streetAddress1**: string: The first line of the street address to use when returning the drives.
* **streetAddress2**: string: The second line of the street address to use when returning the drives.

## SystemData
### Properties
* **createdAt**: string: The timestamp of resource creation (UTC).
* **createdBy**: string: The identity that created the resource.
* **createdByType**: 'Application' | 'Key' | 'ManagedIdentity' | 'User' | string: The type of identity that created the resource.
* **lastModifiedAt**: string: The timestamp of resource last modification (UTC)
* **lastModifiedBy**: string: The identity that last modified the resource.
* **lastModifiedByType**: 'Application' | 'Key' | 'ManagedIdentity' | 'User' | string: The type of identity that last modified the resource.

