# Microsoft.Network @ 2015-11-01

## Resource Microsoft.Network/trafficmanagerprofiles@2015-11-01
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2015-11-01' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **location**: string: Resource location
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [ProfileProperties](#profileproperties): Class representing the Traffic Manager profile properties.
* **tags**: [ResourceTags](#resourcetags): Resource tags
* **type**: 'Microsoft.Network/trafficmanagerprofiles' (ReadOnly, DeployTimeConstant): The resource type

## DnsConfig
### Properties
* **fqdn**: string: Gets or sets the fully-qualified domain name (FQDN) of the Traffic Manager profile.  This is formed from the concatenation of the RelativeName with the DNS domain used by Azure Traffic Manager.
* **relativeName**: string: Gets or sets the relative DNS name provided by this Traffic Manager profile.  This value is combined with the DNS domain name used by Azure Traffic Manager to form the fully-qualified domain name (FQDN) of the profile.
* **ttl**: int: Gets or sets the DNS Time-To-Live (TTL), in seconds.  This informs the local DNS resolvers and DNS clients how long to cache DNS responses provided by this Traffic Manager profile.

## Endpoint
### Properties
* **id**: string: Gets or sets the ID of the Traffic Manager endpoint.
* **name**: string: Gets or sets the name of the Traffic Manager endpoint.
* **properties**: [EndpointProperties](#endpointproperties): Class representing a Traffic Manager endpoint properties.
* **type**: string: Gets or sets the endpoint type of the Traffic Manager endpoint.

## EndpointProperties
### Properties
* **endpointLocation**: string: Specifies the location of the external or nested endpoints when using the ‘Performance’ traffic routing method.
* **endpointMonitorStatus**: string: Gets or sets the monitoring status of the endpoint.
* **endpointStatus**: string: Gets or sets the status of the endpoint..  If the endpoint is Enabled, it is probed for endpoint health and is included in the traffic routing method.  Possible values are 'Enabled' and 'Disabled'.
* **minChildEndpoints**: int: Gets or sets the minimum number of endpoints that must be available in the child profile in order for the parent profile to be considered available. Only applicable to endpoint of type 'NestedEndpoints'.
* **priority**: int: Gets or sets the priority of this endpoint when using the ‘Priority’ traffic routing method. Possible values are from 1 to 1000, lower values represent higher priority. This is an optional parameter.  If specified, it must be specified on all endpoints, and no two endpoints can share the same priority value.
* **target**: string: Gets or sets the fully-qualified DNS name of the endpoint.  Traffic Manager returns this value in DNS responses to direct traffic to this endpoint.
* **targetResourceId**: string: Gets or sets the Azure Resource URI of the of the endpoint.  Not applicable to endpoints of type 'ExternalEndpoints'.
* **weight**: int: Gets or sets the weight of this endpoint when using the 'Weighted' traffic routing method. Possible values are from 1 to 1000.

## MonitorConfig
### Properties
* **path**: string: Gets or sets the path relative to the endpoint domain name used to probe for endpoint health.
* **port**: int: Gets or sets the TCP port used to probe for endpoint health.
* **profileMonitorStatus**: string: Gets or sets the profile-level monitoring status of the Traffic Manager profile.
* **protocol**: string: Gets or sets the protocol (HTTP or HTTPS) used to probe for endpoint health.

## ProfileProperties
### Properties
* **dnsConfig**: [DnsConfig](#dnsconfig): Gets or sets the DNS settings of the Traffic Manager profile.
* **endpoints**: [Endpoint](#endpoint)[]: Gets or sets the list of endpoints in the Traffic Manager profile.
* **monitorConfig**: [MonitorConfig](#monitorconfig): Gets or sets the endpoint monitoring settings of the Traffic Manager profile.
* **profileStatus**: string: Gets or sets the status of the Traffic Manager profile.  Possible values are 'Enabled' and 'Disabled'.
* **trafficRoutingMethod**: string: Gets or sets the traffic routing method of the Traffic Manager profile.  Possible values are 'Performance', 'Weighted', or 'Priority'.

## ResourceTags
### Properties
### Additional Properties
* **Additional Properties Type**: string

