# Microsoft.AzureActiveDirectory @ 2021-04-01

## Resource Microsoft.AzureActiveDirectory/b2cDirectories@2021-04-01
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2021-04-01' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **location**: string (Required): The location in which the resource is hosted and data resides. Can be one of 'United States', 'Europe', 'Asia Pacific', or 'Australia'. Refer to [this documentation](https://aka.ms/B2CDataResidency) for more information.
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [CreateTenantRequestBodyProperties](#createtenantrequestbodyproperties) (Required)
* **sku**: [B2CResourceSKU](#b2cresourcesku) (Required): SKU properties of the Azure AD B2C tenant. Learn more about Azure AD B2C billing at [aka.ms/b2cBilling](https://aka.ms/b2cBilling).
* **systemData**: [SystemData](#systemdata) (ReadOnly): Metadata pertaining to creation and last modification of the resource.
* **tags**: [CreateTenantRequestBodyTags](#createtenantrequestbodytags): Resource Tags
* **type**: 'Microsoft.AzureActiveDirectory/b2cDirectories' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.AzureActiveDirectory/guestUsages@2021-04-01
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2021-04-01' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **location**: string: Location of the Guest Usages resource.
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [GuestUsagesResourceProperties](#guestusagesresourceproperties): Guest Usages Resource Properties
* **systemData**: [SystemData](#systemdata) (ReadOnly): Metadata pertaining to creation and last modification of the resource.
* **tags**: [GuestUsagesResourceTags](#guestusagesresourcetags): Key-value pairs of additional resource provisioning properties.
* **type**: 'Microsoft.AzureActiveDirectory/guestUsages' (ReadOnly, DeployTimeConstant): The resource type

## CreateTenantRequestBodyProperties
### Properties
* **billingConfig**: [B2CTenantResourcePropertiesBillingConfig](#b2ctenantresourcepropertiesbillingconfig) (ReadOnly): The billing configuration for the tenant.
* **createTenantProperties**: [CreateTenantProperties](#createtenantproperties) (WriteOnly): These properties are used to create the Azure AD B2C tenant. These properties are not part of the Azure resource.
* **tenantId**: string (ReadOnly): An identifier of the Azure AD B2C tenant.

## B2CTenantResourcePropertiesBillingConfig
### Properties
* **billingType**: 'Auths' | 'MAU' (ReadOnly): The type of billing. Will be MAU for all new customers. If 'Auths', it can be updated to 'MAU'. Cannot be changed if value is 'MAU'. Learn more about Azure AD B2C billing at [aka.ms/b2cBilling](https://aka.ms/b2cbilling).
* **effectiveStartDateUtc**: string (ReadOnly): The data from which the billing type took effect

## CreateTenantProperties
### Properties
* **countryCode**: string (WriteOnly): Country code of Azure tenant (e.g. 'US'). Refer to [aka.ms/B2CDataResidency](https://aka.ms/B2CDataResidency) to see valid country codes and corresponding data residency locations. If you do not see a country code in an valid data residency location, choose one from the list.
* **displayName**: string (WriteOnly): The display name of the Azure AD B2C tenant.

## B2CResourceSKU
### Properties
* **name**: 'PremiumP1' | 'PremiumP2' | 'Standard': The name of the SKU for the tenant.
* **tier**: 'A0': The tier of the tenant.

## SystemData
### Properties
* **createdAt**: string (ReadOnly): The timestamp of resource creation (UTC).
* **createdBy**: string (ReadOnly): The identity that created the resource.
* **createdByType**: 'Application' | 'Key' | 'ManagedIdentity' | 'User' (ReadOnly): The type of identity that created the resource.
* **lastModifiedAt**: string (ReadOnly): The timestamp of resource last modification (UTC)
* **lastModifiedBy**: string (ReadOnly): The identity that last modified the resource.
* **lastModifiedByType**: 'Application' | 'Key' | 'ManagedIdentity' | 'User' (ReadOnly): The type of identity that created the resource.

## CreateTenantRequestBodyTags
### Properties
### Additional Properties
* **Additional Properties Type**: string

## GuestUsagesResourceProperties
### Properties
* **tenantId**: string: An identifier for the tenant for which the resource is being created

## GuestUsagesResourceTags
### Properties
### Additional Properties
* **Additional Properties Type**: string
