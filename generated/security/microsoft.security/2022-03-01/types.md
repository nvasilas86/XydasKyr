# Microsoft.Security @ 2022-03-01

## Resource Microsoft.Security/pricings@2022-03-01
* **Valid Scope(s)**: Subscription
### Properties
* **apiVersion**: '2022-03-01' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [PricingProperties](#pricingproperties): Pricing properties for the relevant scope
* **type**: 'Microsoft.Security/pricings' (ReadOnly, DeployTimeConstant): The resource type

## PricingProperties
### Properties
* **freeTrialRemainingTime**: string (ReadOnly): The duration left for the subscriptions free trial period - in ISO 8601 format (e.g. P3Y6M4DT12H30M5S).
* **pricingTier**: 'Free' | 'Standard' | string (Required): The pricing tier value. Microsoft Defender for Cloud is provided in two pricing tiers: free and standard, with the standard tier available with a trial period. The standard tier offers advanced security capabilities, while the free tier offers basic security features.
* **subPlan**: string: The sub-plan selected for a Standard pricing configuration, when more than one sub-plan is available. Each sub-plan enables a set of security features. When not specified, full plan is applied.
