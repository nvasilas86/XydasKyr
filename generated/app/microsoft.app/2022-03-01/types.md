# Microsoft.App @ 2022-03-01

## Resource Microsoft.App/containerApps@2022-03-01
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2022-03-01' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **identity**: [ManagedServiceIdentity](#managedserviceidentity): Managed service identity (system assigned and/or user assigned identities)
* **location**: string (Required): The geo-location where the resource lives
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [ContainerAppProperties](#containerappproperties): ContainerApp resource specific properties
* **systemData**: [SystemData](#systemdata) (ReadOnly): Metadata pertaining to creation and last modification of the resource.
* **tags**: [TrackedResourceTags](#trackedresourcetags): Resource tags.
* **type**: 'Microsoft.App/containerApps' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.App/containerApps/authConfigs@2022-03-01
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2022-03-01' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [AuthConfigProperties](#authconfigproperties): AuthConfig resource specific properties
* **systemData**: [SystemData](#systemdata) (ReadOnly): Metadata pertaining to creation and last modification of the resource.
* **type**: 'Microsoft.App/containerApps/authConfigs' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.App/containerApps/sourcecontrols@2022-03-01
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2022-03-01' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [SourceControlProperties](#sourcecontrolproperties): SourceControl resource specific properties
* **systemData**: [SystemData](#systemdata) (ReadOnly): Metadata pertaining to creation and last modification of the resource.
* **type**: 'Microsoft.App/containerApps/sourcecontrols' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.App/managedEnvironments@2022-03-01
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2022-03-01' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **location**: string (Required): The geo-location where the resource lives
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [ManagedEnvironmentProperties](#managedenvironmentproperties): Managed environment resource specific properties
* **systemData**: [SystemData](#systemdata) (ReadOnly): Metadata pertaining to creation and last modification of the resource.
* **tags**: [TrackedResourceTags](#trackedresourcetags): Resource tags.
* **type**: 'Microsoft.App/managedEnvironments' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.App/managedEnvironments/certificates@2022-03-01
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2022-03-01' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **location**: string (Required): The geo-location where the resource lives
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [CertificateProperties](#certificateproperties): Certificate resource specific properties
* **systemData**: [SystemData](#systemdata) (ReadOnly): Metadata pertaining to creation and last modification of the resource.
* **tags**: [TrackedResourceTags](#trackedresourcetags): Resource tags.
* **type**: 'Microsoft.App/managedEnvironments/certificates' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.App/managedEnvironments/daprComponents@2022-03-01
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2022-03-01' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [DaprComponentProperties](#daprcomponentproperties): Dapr Component resource specific properties
* **systemData**: [SystemData](#systemdata) (ReadOnly): Metadata pertaining to creation and last modification of the resource.
* **type**: 'Microsoft.App/managedEnvironments/daprComponents' (ReadOnly, DeployTimeConstant): The resource type

## Resource Microsoft.App/managedEnvironments/storages@2022-03-01
* **Valid Scope(s)**: ResourceGroup
### Properties
* **apiVersion**: '2022-03-01' (ReadOnly, DeployTimeConstant): The resource api version
* **id**: string (ReadOnly, DeployTimeConstant): The resource id
* **name**: string (Required, DeployTimeConstant): The resource name
* **properties**: [ManagedEnvironmentStorageProperties](#managedenvironmentstorageproperties): Storage properties
* **systemData**: [SystemData](#systemdata) (ReadOnly): Metadata pertaining to creation and last modification of the resource.
* **type**: 'Microsoft.App/managedEnvironments/storages' (ReadOnly, DeployTimeConstant): The resource type

## Function listCustomHostNameAnalysis (Microsoft.App/containerApps@2022-03-01)
* **Resource**: Microsoft.App/containerApps
* **ApiVersion**: 2022-03-01
* **Output**: [CustomHostnameAnalysisResult](#customhostnameanalysisresult)

## Function listSecrets (Microsoft.App/containerApps@2022-03-01)
* **Resource**: Microsoft.App/containerApps
* **ApiVersion**: 2022-03-01
* **Output**: [SecretsCollection](#secretscollection)

## Function listSecrets (Microsoft.App/managedEnvironments/daprComponents@2022-03-01)
* **Resource**: Microsoft.App/managedEnvironments/daprComponents
* **ApiVersion**: 2022-03-01
* **Output**: [DaprSecretsCollection](#daprsecretscollection)

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

## ContainerAppProperties
### Properties
* **configuration**: [Configuration](#configuration): Non versioned Container App configuration properties that define the mutable settings of a Container app
* **customDomainVerificationId**: string (ReadOnly): Id used to verify domain name ownership
* **latestRevisionFqdn**: string (ReadOnly): Fully Qualified Domain Name of the latest revision of the Container App.
* **latestRevisionName**: string (ReadOnly): Name of the latest revision of the Container App.
* **managedEnvironmentId**: string: Resource ID of the Container App's environment.
* **outboundIPAddresses**: string[] (ReadOnly): Outbound IP Addresses for container app.
* **provisioningState**: 'Canceled' | 'Failed' | 'InProgress' | 'Succeeded' | string (ReadOnly): Provisioning state of the Container App.
* **template**: [Template](#template): Container App versioned application definition.
Defines the desired state of an immutable revision.
Any changes to this section Will result in a new revision being created

## Configuration
### Properties
* **activeRevisionsMode**: 'multiple' | 'single' | string: ActiveRevisionsMode controls how active revisions are handled for the Container app:
<list><item>Multiple: multiple revisions can be active.</item><item>Single: Only one revision can be active at a time. Revision weights can not be used in this mode. If no value if provided, this is the default.</item></list>
* **dapr**: [Dapr](#dapr): Container App Dapr configuration.
* **ingress**: [Ingress](#ingress): Container App Ingress configuration.
* **registries**: [RegistryCredentials](#registrycredentials)[]: Collection of private container registry credentials for containers used by the Container app
* **secrets**: [Secret](#secret)[]: Collection of secrets used by a Container app

## Dapr
### Properties
* **appId**: string: Dapr application identifier
* **appPort**: int: Tells Dapr which port your application is listening on
* **appProtocol**: 'grpc' | 'http' | string: Tells Dapr which protocol your application is using. Valid options are http and grpc. Default is http
* **enabled**: bool: Boolean indicating if the Dapr side car is enabled

## Ingress
### Properties
* **allowInsecure**: bool: Bool indicating if HTTP connections to is allowed. If set to false HTTP connections are automatically redirected to HTTPS connections
* **customDomains**: [CustomDomain](#customdomain)[]: custom domain bindings for Container Apps' hostnames.
* **external**: bool: Bool indicating if app exposes an external http endpoint
* **fqdn**: string (ReadOnly): Hostname.
* **targetPort**: int: Target Port in containers for traffic from ingress
* **traffic**: [TrafficWeight](#trafficweight)[]: Traffic weights for app's revisions
* **transport**: 'auto' | 'http' | 'http2' | string: Ingress transport protocol

## CustomDomain
### Properties
* **bindingType**: 'Disabled' | 'SniEnabled' | string: Custom Domain binding type.
* **certificateId**: string (Required): Resource Id of the Certificate to be bound to this hostname. Must exist in the Managed Environment.
* **name**: string (Required): Hostname.

## TrafficWeight
### Properties
* **label**: string: Associates a traffic label with a revision
* **latestRevision**: bool: Indicates that the traffic weight belongs to a latest stable revision
* **revisionName**: string: Name of a revision
* **weight**: int: Traffic weight assigned to a revision

## RegistryCredentials
### Properties
* **identity**: string: A Managed Identity to use to authenticate with Azure Container Registry. For user-assigned identities, use the full user-assigned identity Resource ID. For system-assigned identities, use 'system'
* **passwordSecretRef**: string: The name of the Secret that contains the registry login password
* **server**: string: Container Registry Server
* **username**: string: Container Registry Username

## Secret
### Properties
* **name**: string: Secret Name.
* **value**: string (WriteOnly): Secret Value.

## Template
### Properties
* **containers**: [Container](#container)[]: List of container definitions for the Container App.
* **revisionSuffix**: string: User friendly suffix that is appended to the revision name
* **scale**: [Scale](#scale): Container App scaling configurations.
* **volumes**: [Volume](#volume)[]: List of volume definitions for the Container App.

## Container
### Properties
* **args**: string[]: Container start command arguments.
* **command**: string[]: Container start command.
* **env**: [EnvironmentVar](#environmentvar)[]: Container environment variables.
* **image**: string: Container image tag.
* **name**: string: Custom container name.
* **probes**: [ContainerAppProbe](#containerappprobe)[]: List of probes for the container.
* **resources**: [ContainerResources](#containerresources): Container App container resource requirements.
* **volumeMounts**: [VolumeMount](#volumemount)[]: Container volume mounts.

## EnvironmentVar
### Properties
* **name**: string: Environment variable name.
* **secretRef**: string: Name of the Container App secret from which to pull the environment variable value.
* **value**: string: Non-secret environment variable value.

## ContainerAppProbe
### Properties
* **failureThreshold**: int: Minimum consecutive failures for the probe to be considered failed after having succeeded. Defaults to 3. Minimum value is 1. Maximum value is 10.
* **httpGet**: [ContainerAppProbeHttpGet](#containerappprobehttpget): HTTPGet specifies the http request to perform.
* **initialDelaySeconds**: int: Number of seconds after the container has started before liveness probes are initiated. Minimum value is 1. Maximum value is 60.
* **periodSeconds**: int: How often (in seconds) to perform the probe. Default to 10 seconds. Minimum value is 1. Maximum value is 240.
* **successThreshold**: int: Minimum consecutive successes for the probe to be considered successful after having failed. Defaults to 1. Must be 1 for liveness and startup. Minimum value is 1. Maximum value is 10.
* **tcpSocket**: [ContainerAppProbeTcpSocket](#containerappprobetcpsocket): TCPSocket specifies an action involving a TCP port. TCP hooks not yet supported.
* **terminationGracePeriodSeconds**: int: Optional duration in seconds the pod needs to terminate gracefully upon probe failure. The grace period is the duration in seconds after the processes running in the pod are sent a termination signal and the time when the processes are forcibly halted with a kill signal. Set this value longer than the expected cleanup time for your process. If this value is nil, the pod's terminationGracePeriodSeconds will be used. Otherwise, this value overrides the value provided by the pod spec. Value must be non-negative integer. The value zero indicates stop immediately via the kill signal (no opportunity to shut down). This is an alpha field and requires enabling ProbeTerminationGracePeriod feature gate. Maximum value is 3600 seconds (1 hour)
* **timeoutSeconds**: int: Number of seconds after which the probe times out. Defaults to 1 second. Minimum value is 1. Maximum value is 240.
* **type**: 'liveness' | 'readiness' | 'startup' | string: The type of probe.

## ContainerAppProbeHttpGet
### Properties
* **host**: string: Host name to connect to, defaults to the pod IP. You probably want to set "Host" in httpHeaders instead.
* **httpHeaders**: [ContainerAppProbeHttpGetHttpHeadersItem](#containerappprobehttpgethttpheadersitem)[]: Custom headers to set in the request. HTTP allows repeated headers.
* **path**: string: Path to access on the HTTP server.
* **port**: int (Required): Name or number of the port to access on the container. Number must be in the range 1 to 65535. Name must be an IANA_SVC_NAME.
* **scheme**: string: Scheme to use for connecting to the host. Defaults to HTTP.

## ContainerAppProbeHttpGetHttpHeadersItem
### Properties
* **name**: string (Required): The header field name
* **value**: string (Required): The header field value

## ContainerAppProbeTcpSocket
### Properties
* **host**: string: Optional: Host name to connect to, defaults to the pod IP.
* **port**: int (Required): Number or name of the port to access on the container. Number must be in the range 1 to 65535. Name must be an IANA_SVC_NAME.

## ContainerResources
### Properties
* **cpu**: int: Required CPU in cores, e.g. 0.5
* **ephemeralStorage**: string (ReadOnly): Ephemeral Storage, e.g. "1Gi"
* **memory**: string: Required memory, e.g. "250Mb"

## VolumeMount
### Properties
* **mountPath**: string: Path within the container at which the volume should be mounted.Must not contain ':'.
* **volumeName**: string: This must match the Name of a Volume.

## Scale
### Properties
* **maxReplicas**: int: Optional. Maximum number of container replicas. Defaults to 10 if not set.
* **minReplicas**: int: Optional. Minimum number of container replicas.
* **rules**: [ScaleRule](#scalerule)[]: Scaling rules.

## ScaleRule
### Properties
* **azureQueue**: [QueueScaleRule](#queuescalerule): Container App container Azure Queue based scaling rule.
* **custom**: [CustomScaleRule](#customscalerule): Container App container Custom scaling rule.
* **http**: [HttpScaleRule](#httpscalerule): Container App container Custom scaling rule.
* **name**: string: Scale Rule Name

## QueueScaleRule
### Properties
* **auth**: [ScaleRuleAuth](#scaleruleauth)[]: Authentication secrets for the queue scale rule.
* **queueLength**: int: Queue length.
* **queueName**: string: Queue name.

## ScaleRuleAuth
### Properties
* **secretRef**: string: Name of the Container App secret from which to pull the auth params.
* **triggerParameter**: string: Trigger Parameter that uses the secret

## CustomScaleRule
### Properties
* **auth**: [ScaleRuleAuth](#scaleruleauth)[]: Authentication secrets for the custom scale rule.
* **metadata**: [CustomScaleRuleMetadata](#customscalerulemetadata): Metadata properties to describe custom scale rule.
* **type**: string: Type of the custom scale rule
eg: azure-servicebus, redis etc.

## CustomScaleRuleMetadata
### Properties
### Additional Properties
* **Additional Properties Type**: string

## HttpScaleRule
### Properties
* **auth**: [ScaleRuleAuth](#scaleruleauth)[]: Authentication secrets for the custom scale rule.
* **metadata**: [HttpScaleRuleMetadata](#httpscalerulemetadata): Metadata properties to describe http scale rule.

## HttpScaleRuleMetadata
### Properties
### Additional Properties
* **Additional Properties Type**: string

## Volume
### Properties
* **name**: string: Volume name.
* **storageName**: string: Name of storage resource. No need to provide for EmptyDir.
* **storageType**: 'AzureFile' | 'EmptyDir' | string: Storage type for the volume. If not provided, use EmptyDir.

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

## AuthConfigProperties
### Properties
* **globalValidation**: [GlobalValidation](#globalvalidation): The configuration settings that determines the validation flow of users using ContainerApp Service Authentication/Authorization.
* **httpSettings**: [HttpSettings](#httpsettings): The configuration settings of the HTTP requests for authentication and authorization requests made against ContainerApp Service Authentication/Authorization.
* **identityProviders**: [IdentityProviders](#identityproviders): The configuration settings of each of the identity providers used to configure ContainerApp Service Authentication/Authorization.
* **login**: [Login](#login): The configuration settings of the login flow of users using ContainerApp Service Authentication/Authorization.
* **platform**: [AuthPlatform](#authplatform): The configuration settings of the platform of ContainerApp Service Authentication/Authorization.

## GlobalValidation
### Properties
* **excludedPaths**: string[]: The paths for which unauthenticated flow would not be redirected to the login page.
* **redirectToProvider**: string: The default authentication provider to use when multiple providers are configured.
This setting is only needed if multiple providers are configured and the unauthenticated client
action is set to "RedirectToLoginPage".
* **unauthenticatedClientAction**: 'AllowAnonymous' | 'RedirectToLoginPage' | 'Return401' | 'Return403': The action to take when an unauthenticated client attempts to access the app.

## HttpSettings
### Properties
* **forwardProxy**: [ForwardProxy](#forwardproxy): The configuration settings of a forward proxy used to make the requests.
* **requireHttps**: bool: <code>false</code> if the authentication/authorization responses not having the HTTPS scheme are permissible; otherwise, <code>true</code>.
* **routes**: [HttpSettingsRoutes](#httpsettingsroutes): The configuration settings of the paths HTTP requests.

## ForwardProxy
### Properties
* **convention**: 'Custom' | 'NoProxy' | 'Standard': The convention used to determine the url of the request made.
* **customHostHeaderName**: string: The name of the header containing the host of the request.
* **customProtoHeaderName**: string: The name of the header containing the scheme of the request.

## HttpSettingsRoutes
### Properties
* **apiPrefix**: string: The prefix that should precede all the authentication/authorization paths.

## IdentityProviders
### Properties
* **apple**: [Apple](#apple): The configuration settings of the Apple provider.
* **azureActiveDirectory**: [AzureActiveDirectory](#azureactivedirectory): The configuration settings of the Azure Active directory provider.
* **azureStaticWebApps**: [AzureStaticWebApps](#azurestaticwebapps): The configuration settings of the Azure Static Web Apps provider.
* **customOpenIdConnectProviders**: [IdentityProvidersCustomOpenIdConnectProviders](#identityproviderscustomopenidconnectproviders): The map of the name of the alias of each custom Open ID Connect provider to the
configuration settings of the custom Open ID Connect provider.
* **facebook**: [Facebook](#facebook): The configuration settings of the Facebook provider.
* **gitHub**: [GitHub](#github): The configuration settings of the GitHub provider.
* **google**: [Google](#google): The configuration settings of the Google provider.
* **twitter**: [Twitter](#twitter): The configuration settings of the Twitter provider.

## Apple
### Properties
* **enabled**: bool: <code>false</code> if the Apple provider should not be enabled despite the set registration; otherwise, <code>true</code>.
* **login**: [LoginScopes](#loginscopes): The configuration settings of the login flow, including the scopes that should be requested.
* **registration**: [AppleRegistration](#appleregistration): The configuration settings of the registration for the Apple provider

## LoginScopes
### Properties
* **scopes**: string[]: A list of the scopes that should be requested while authenticating.

## AppleRegistration
### Properties
* **clientId**: string: The Client ID of the app used for login.
* **clientSecretSettingName**: string: The app setting name that contains the client secret.

## AzureActiveDirectory
### Properties
* **enabled**: bool: <code>false</code> if the Azure Active Directory provider should not be enabled despite the set registration; otherwise, <code>true</code>.
* **isAutoProvisioned**: bool: Gets a value indicating whether the Azure AD configuration was auto-provisioned using 1st party tooling.
This is an internal flag primarily intended to support the Azure Management Portal. Users should not
read or write to this property.
* **login**: [AzureActiveDirectoryLogin](#azureactivedirectorylogin): The configuration settings of the Azure Active Directory login flow.
* **registration**: [AzureActiveDirectoryRegistration](#azureactivedirectoryregistration): The configuration settings of the Azure Active Directory app registration.
* **validation**: [AzureActiveDirectoryValidation](#azureactivedirectoryvalidation): The configuration settings of the Azure Active Directory token validation flow.

## AzureActiveDirectoryLogin
### Properties
* **disableWWWAuthenticate**: bool: <code>true</code> if the www-authenticate provider should be omitted from the request; otherwise, <code>false</code>.
* **loginParameters**: string[]: Login parameters to send to the OpenID Connect authorization endpoint when
a user logs in. Each parameter must be in the form "key=value".

## AzureActiveDirectoryRegistration
### Properties
* **clientId**: string: The Client ID of this relying party application, known as the client_id.
This setting is required for enabling OpenID Connection authentication with Azure Active Directory or 
other 3rd party OpenID Connect providers.
More information on OpenID Connect: http://openid.net/specs/openid-connect-core-1_0.html
* **clientSecretCertificateIssuer**: string: An alternative to the client secret thumbprint, that is the issuer of a certificate used for signing purposes. This property acts as
a replacement for the Client Secret Certificate Thumbprint. It is also optional.
* **clientSecretCertificateSubjectAlternativeName**: string: An alternative to the client secret thumbprint, that is the subject alternative name of a certificate used for signing purposes. This property acts as
a replacement for the Client Secret Certificate Thumbprint. It is also optional.
* **clientSecretCertificateThumbprint**: string: An alternative to the client secret, that is the thumbprint of a certificate used for signing purposes. This property acts as
a replacement for the Client Secret. It is also optional.
* **clientSecretSettingName**: string: The app setting name that contains the client secret of the relying party application.
* **openIdIssuer**: string: The OpenID Connect Issuer URI that represents the entity which issues access tokens for this application.
When using Azure Active Directory, this value is the URI of the directory tenant, e.g. https://login.microsoftonline.com/v2.0/{tenant-guid}/.
This URI is a case-sensitive identifier for the token issuer.
More information on OpenID Connect Discovery: http://openid.net/specs/openid-connect-discovery-1_0.html

## AzureActiveDirectoryValidation
### Properties
* **allowedAudiences**: string[]: The list of audiences that can make successful authentication/authorization requests.
* **defaultAuthorizationPolicy**: [DefaultAuthorizationPolicy](#defaultauthorizationpolicy): The configuration settings of the Azure Active Directory default authorization policy.
* **jwtClaimChecks**: [JwtClaimChecks](#jwtclaimchecks): The configuration settings of the checks that should be made while validating the JWT Claims.

## DefaultAuthorizationPolicy
### Properties
* **allowedApplications**: string[]: The configuration settings of the Azure Active Directory allowed applications.
* **allowedPrincipals**: [AllowedPrincipals](#allowedprincipals): The configuration settings of the Azure Active Directory allowed principals.

## AllowedPrincipals
### Properties
* **groups**: string[]: The list of the allowed groups.
* **identities**: string[]: The list of the allowed identities.

## JwtClaimChecks
### Properties
* **allowedClientApplications**: string[]: The list of the allowed client applications.
* **allowedGroups**: string[]: The list of the allowed groups.

## AzureStaticWebApps
### Properties
* **enabled**: bool: <code>false</code> if the Azure Static Web Apps provider should not be enabled despite the set registration; otherwise, <code>true</code>.
* **registration**: [AzureStaticWebAppsRegistration](#azurestaticwebappsregistration): The configuration settings of the registration for the Azure Static Web Apps provider

## AzureStaticWebAppsRegistration
### Properties
* **clientId**: string: The Client ID of the app used for login.

## IdentityProvidersCustomOpenIdConnectProviders
### Properties
### Additional Properties
* **Additional Properties Type**: [CustomOpenIdConnectProvider](#customopenidconnectprovider)

## CustomOpenIdConnectProvider
### Properties
* **enabled**: bool: <code>false</code> if the custom Open ID provider provider should not be enabled; otherwise, <code>true</code>.
* **login**: [OpenIdConnectLogin](#openidconnectlogin): The configuration settings of the login flow of the custom Open ID Connect provider.
* **registration**: [OpenIdConnectRegistration](#openidconnectregistration): The configuration settings of the app registration for the custom Open ID Connect provider.

## OpenIdConnectLogin
### Properties
* **nameClaimType**: string: The name of the claim that contains the users name.
* **scopes**: string[]: A list of the scopes that should be requested while authenticating.

## OpenIdConnectRegistration
### Properties
* **clientCredential**: [OpenIdConnectClientCredential](#openidconnectclientcredential): The authentication client credentials of the custom Open ID Connect provider.
* **clientId**: string: The client id of the custom Open ID Connect provider.
* **openIdConnectConfiguration**: [OpenIdConnectConfig](#openidconnectconfig): The configuration settings of the endpoints used for the custom Open ID Connect provider.

## OpenIdConnectClientCredential
### Properties
* **clientSecretSettingName**: string: The app setting that contains the client secret for the custom Open ID Connect provider.
* **method**: 'ClientSecretPost': The method that should be used to authenticate the user.

## OpenIdConnectConfig
### Properties
* **authorizationEndpoint**: string: The endpoint to be used to make an authorization request.
* **certificationUri**: string: The endpoint that provides the keys necessary to validate the token.
* **issuer**: string: The endpoint that issues the token.
* **tokenEndpoint**: string: The endpoint to be used to request a token.
* **wellKnownOpenIdConfiguration**: string: The endpoint that contains all the configuration endpoints for the provider.

## Facebook
### Properties
* **enabled**: bool: <code>false</code> if the Facebook provider should not be enabled despite the set registration; otherwise, <code>true</code>.
* **graphApiVersion**: string: The version of the Facebook api to be used while logging in.
* **login**: [LoginScopes](#loginscopes): The configuration settings of the login flow, including the scopes that should be requested.
* **registration**: [AppRegistration](#appregistration): The configuration settings of the app registration for providers that have app ids and app secrets

## AppRegistration
### Properties
* **appId**: string: The App ID of the app used for login.
* **appSecretSettingName**: string: The app setting name that contains the app secret.

## GitHub
### Properties
* **enabled**: bool: <code>false</code> if the GitHub provider should not be enabled despite the set registration; otherwise, <code>true</code>.
* **login**: [LoginScopes](#loginscopes): The configuration settings of the login flow, including the scopes that should be requested.
* **registration**: [ClientRegistration](#clientregistration): The configuration settings of the app registration for providers that have client ids and client secrets

## ClientRegistration
### Properties
* **clientId**: string: The Client ID of the app used for login.
* **clientSecretSettingName**: string: The app setting name that contains the client secret.

## Google
### Properties
* **enabled**: bool: <code>false</code> if the Google provider should not be enabled despite the set registration; otherwise, <code>true</code>.
* **login**: [LoginScopes](#loginscopes): The configuration settings of the login flow, including the scopes that should be requested.
* **registration**: [ClientRegistration](#clientregistration): The configuration settings of the app registration for providers that have client ids and client secrets
* **validation**: [AllowedAudiencesValidation](#allowedaudiencesvalidation): The configuration settings of the Allowed Audiences validation flow.

## AllowedAudiencesValidation
### Properties
* **allowedAudiences**: string[]: The configuration settings of the allowed list of audiences from which to validate the JWT token.

## Twitter
### Properties
* **enabled**: bool: <code>false</code> if the Twitter provider should not be enabled despite the set registration; otherwise, <code>true</code>.
* **registration**: [TwitterRegistration](#twitterregistration): The configuration settings of the app registration for the Twitter provider.

## TwitterRegistration
### Properties
* **consumerKey**: string: The OAuth 1.0a consumer key of the Twitter application used for sign-in.
This setting is required for enabling Twitter Sign-In.
Twitter Sign-In documentation: https://dev.twitter.com/web/sign-in
* **consumerSecretSettingName**: string: The app setting name that contains the OAuth 1.0a consumer secret of the Twitter
application used for sign-in.

## Login
### Properties
* **allowedExternalRedirectUrls**: string[]: External URLs that can be redirected to as part of logging in or logging out of the app. Note that the query string part of the URL is ignored.
This is an advanced setting typically only needed by Windows Store application backends.
Note that URLs within the current domain are always implicitly allowed.
* **cookieExpiration**: [CookieExpiration](#cookieexpiration): The configuration settings of the session cookie's expiration.
* **nonce**: [Nonce](#nonce): The configuration settings of the nonce used in the login flow.
* **preserveUrlFragmentsForLogins**: bool: <code>true</code> if the fragments from the request are preserved after the login request is made; otherwise, <code>false</code>.
* **routes**: [LoginRoutes](#loginroutes): The routes that specify the endpoints used for login and logout requests.

## CookieExpiration
### Properties
* **convention**: 'FixedTime' | 'IdentityProviderDerived': The convention used when determining the session cookie's expiration.
* **timeToExpiration**: string: The time after the request is made when the session cookie should expire.

## Nonce
### Properties
* **nonceExpirationInterval**: string: The time after the request is made when the nonce should expire.
* **validateNonce**: bool: <code>false</code> if the nonce should not be validated while completing the login flow; otherwise, <code>true</code>.

## LoginRoutes
### Properties
* **logoutEndpoint**: string: The endpoint at which a logout request should be made.

## AuthPlatform
### Properties
* **enabled**: bool: <code>true</code> if the Authentication / Authorization feature is enabled for the current app; otherwise, <code>false</code>.
* **runtimeVersion**: string: The RuntimeVersion of the Authentication / Authorization feature in use for the current app.
The setting in this value can control the behavior of certain features in the Authentication / Authorization module.

## SourceControlProperties
### Properties
* **branch**: string: The branch which will trigger the auto deployment
* **githubActionConfiguration**: [GithubActionConfiguration](#githubactionconfiguration): Configuration properties that define the mutable settings of a Container App SourceControl
* **operationState**: 'Canceled' | 'Failed' | 'InProgress' | 'Succeeded' | string (ReadOnly): Current provisioning State of the operation
* **repoUrl**: string: The repo url which will be integrated to ContainerApp.

## GithubActionConfiguration
### Properties
* **azureCredentials**: [AzureCredentials](#azurecredentials): Container App credentials.
* **contextPath**: string: Context path
* **image**: string: Image name
* **os**: string: Operation system
* **publishType**: string: Code or Image
* **registryInfo**: [RegistryInfo](#registryinfo): Container App registry information.
* **runtimeStack**: string: Runtime stack
* **runtimeVersion**: string: Runtime version

## AzureCredentials
### Properties
* **clientId**: string (WriteOnly): Client Id.
* **clientSecret**: string (WriteOnly): Client Secret.
* **subscriptionId**: string: Subscription Id.
* **tenantId**: string (WriteOnly): Tenant Id.

## RegistryInfo
### Properties
* **registryPassword**: string (WriteOnly): registry secret.
* **registryUrl**: string: registry server Url.
* **registryUserName**: string: registry username.

## ManagedEnvironmentProperties
### Properties
* **appLogsConfiguration**: [AppLogsConfiguration](#applogsconfiguration): Configuration of application logs
* **daprAIConnectionString**: string: Application Insights connection string used by Dapr to export Service to Service communication telemetry
* **daprAIInstrumentationKey**: string: Azure Monitor instrumentation key used by Dapr to export Service to Service communication telemetry
* **defaultDomain**: string (ReadOnly): Default Domain Name for the cluster
* **deploymentErrors**: string (ReadOnly): Any errors that occurred during deployment or deployment validation
* **provisioningState**: 'Canceled' | 'Failed' | 'InfrastructureSetupComplete' | 'InfrastructureSetupInProgress' | 'InitializationInProgress' | 'ScheduledForDelete' | 'Succeeded' | 'UpgradeFailed' | 'UpgradeRequested' | 'Waiting' | string (ReadOnly): Provisioning state of the Environment.
* **staticIp**: string (ReadOnly): Static IP of the Environment
* **vnetConfiguration**: [VnetConfiguration](#vnetconfiguration): Configuration properties for apps environment to join a Virtual Network
* **zoneRedundant**: bool: Whether or not this Managed Environment is zone-redundant.

## AppLogsConfiguration
### Properties
* **destination**: string: Logs destination
* **logAnalyticsConfiguration**: [LogAnalyticsConfiguration](#loganalyticsconfiguration): Log analytics configuration

## LogAnalyticsConfiguration
### Properties
* **customerId**: string: Log analytics customer id
* **sharedKey**: string (WriteOnly): Log analytics customer key

## VnetConfiguration
### Properties
* **dockerBridgeCidr**: string: CIDR notation IP range assigned to the Docker bridge, network. Must not overlap with any other provided IP ranges.
* **infrastructureSubnetId**: string: Resource ID of a subnet for infrastructure components. This subnet must be in the same VNET as the subnet defined in runtimeSubnetId. Must not overlap with any other provided IP ranges.
* **internal**: bool: Boolean indicating the environment only has an internal load balancer. These environments do not have a public static IP resource, must provide ControlPlaneSubnetResourceId and AppSubnetResourceId if enabling this property
* **platformReservedCidr**: string: IP range in CIDR notation that can be reserved for environment infrastructure IP addresses. Must not overlap with any other provided IP ranges.
* **platformReservedDnsIP**: string: An IP address from the IP range defined by platformReservedCidr that will be reserved for the internal DNS server.
* **runtimeSubnetId**: string: Resource ID of a subnet that Container App containers are injected into. This subnet must be in the same VNET as the subnet defined in infrastructureSubnetId. Must not overlap with any other provided IP ranges.

## TrackedResourceTags
### Properties
### Additional Properties
* **Additional Properties Type**: string

## CertificateProperties
### Properties
* **expirationDate**: string (ReadOnly): Certificate expiration date.
* **issueDate**: string (ReadOnly): Certificate issue Date.
* **issuer**: string (ReadOnly): Certificate issuer.
* **password**: string (WriteOnly): Certificate password.
* **provisioningState**: 'Canceled' | 'DeleteFailed' | 'Failed' | 'Pending' | 'Succeeded' | string (ReadOnly): Provisioning state of the certificate.
* **publicKeyHash**: string (ReadOnly): Public key hash.
* **subjectName**: string (ReadOnly): Subject name of the certificate.
* **thumbprint**: string (ReadOnly): Certificate thumbprint.
* **valid**: bool (ReadOnly): Is the certificate valid?.
* **value**: any (WriteOnly): PFX or PEM blob

## TrackedResourceTags
### Properties
### Additional Properties
* **Additional Properties Type**: string

## DaprComponentProperties
### Properties
* **componentType**: string: Component type
* **ignoreErrors**: bool: Boolean describing if the component errors are ignores
* **initTimeout**: string: Initialization timeout
* **metadata**: [DaprMetadata](#daprmetadata)[]: Component metadata
* **scopes**: string[]: Names of container apps that can use this Dapr component
* **secrets**: [Secret](#secret)[]: Collection of secrets used by a Dapr component
* **version**: string: Component version

## DaprMetadata
### Properties
* **name**: string: Metadata property name.
* **secretRef**: string: Name of the Dapr Component secret from which to pull the metadata property value.
* **value**: string: Metadata property value.

## ManagedEnvironmentStorageProperties
### Properties
* **azureFile**: [AzureFileProperties](#azurefileproperties): Azure File Properties.

## AzureFileProperties
### Properties
* **accessMode**: 'ReadOnly' | 'ReadWrite' | string: Access mode for storage
* **accountKey**: string: Storage account key for azure file.
* **accountName**: string: Storage account name for azure file.
* **shareName**: string: Azure file share name.

## CustomHostnameAnalysisResult
### Properties
* **id**: string (ReadOnly): Fully qualified resource ID for the resource. Ex - /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/{resourceProviderNamespace}/{resourceType}/{resourceName}
* **name**: string (ReadOnly): The name of the resource
* **properties**: [CustomHostnameAnalysisResultProperties](#customhostnameanalysisresultproperties) (ReadOnly): CustomHostnameAnalysisResult resource specific properties
* **systemData**: [SystemData](#systemdata) (ReadOnly): Metadata pertaining to creation and last modification of the resource.
* **type**: string (ReadOnly): The type of the resource. E.g. "Microsoft.Compute/virtualMachines" or "Microsoft.Storage/storageAccounts"

## CustomHostnameAnalysisResultProperties
### Properties
* **alternateCNameRecords**: string[] (ReadOnly): Alternate CName records visible for this hostname.
* **alternateTxtRecords**: string[] (ReadOnly): Alternate TXT records visible for this hostname.
* **aRecords**: string[] (ReadOnly): A records visible for this hostname.
* **cNameRecords**: string[] (ReadOnly): CName records visible for this hostname.
* **conflictingContainerAppResourceId**: string (ReadOnly): Name of the conflicting Container App on the Managed Environment if it's within the same subscription.
* **customDomainVerificationFailureInfo**: [DefaultErrorResponse](#defaulterrorresponse) (ReadOnly): App Service error response.
* **customDomainVerificationTest**: 'Failed' | 'Passed' | 'Skipped' (ReadOnly): DNS verification test result.
* **hasConflictOnManagedEnvironment**: bool (ReadOnly): <code>true</code> if there is a conflict on the Container App's managed environment; otherwise, <code>false</code>.
* **hostName**: string (ReadOnly): Host name that was analyzed
* **isHostnameAlreadyVerified**: bool (ReadOnly): <code>true</code> if hostname is already verified; otherwise, <code>false</code>.
* **txtRecords**: string[] (ReadOnly): TXT records visible for this hostname.

## DefaultErrorResponse
### Properties
* **error**: [DefaultErrorResponseError](#defaulterrorresponseerror) (ReadOnly): Error model.

## DefaultErrorResponseError
### Properties
* **code**: string (ReadOnly): Standardized string to programmatically identify the error.
* **details**: [DefaultErrorResponseErrorDetailsItem](#defaulterrorresponseerrordetailsitem)[] (ReadOnly): Details or the error
* **innererror**: string (ReadOnly): More information to debug error.
* **message**: string (ReadOnly): Detailed error description and debugging information.
* **target**: string (ReadOnly): Detailed error description and debugging information.

## DefaultErrorResponseErrorDetailsItem
### Properties
* **code**: string (ReadOnly): Standardized string to programmatically identify the error.
* **message**: string (ReadOnly): Detailed error description and debugging information.
* **target**: string (ReadOnly): Detailed error description and debugging information.

## SecretsCollection
### Properties
* **value**: [ContainerAppSecret](#containerappsecret)[] (ReadOnly): Collection of resources.

## ContainerAppSecret
### Properties
* **name**: string (ReadOnly): Secret Name.
* **value**: string (ReadOnly): Secret Value.

## DaprSecretsCollection
### Properties
* **value**: [Secret](#secret)[] (ReadOnly): Collection of secrets used by a Dapr component
