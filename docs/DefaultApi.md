# \DefaultApi

All URIs are relative to *https://127.0.0.1:8080*

Method | HTTP request | Description
------------- | ------------- | -------------
[**AssocRoleAm**](DefaultApi.md#AssocRoleAm) | **Post** /assoc-role-am | Create an association between role and auth method
[**Auth**](DefaultApi.md#Auth) | **Post** /auth | Authenticate to the service and returns a token to be used as a profile to execute the CLI without the need for re-authentication
[**Configure**](DefaultApi.md#Configure) | **Post** /configure | Configure client profile.
[**CreateAuthMethod**](DefaultApi.md#CreateAuthMethod) | **Post** /create-auth-method | Create a new Auth Method in the account
[**CreateAuthMethodAzureAd**](DefaultApi.md#CreateAuthMethodAzureAd) | **Post** /create-auth-method-azure-ad | Create a new Auth Method that will be able to authentication using Azure Active Directory credentials
[**CreateAuthMethodLdap**](DefaultApi.md#CreateAuthMethodLdap) | **Post** /create-auth-method-ldap | Create a new Auth Method that will be able to authentication using LDAP
[**CreateAuthMethodOauth2**](DefaultApi.md#CreateAuthMethodOauth2) | **Post** /create-auth-method-oauth2 | Create a new Auth Method that will be able to authentication using OpenId/OAuth2
[**CreateAuthMethodSaml**](DefaultApi.md#CreateAuthMethodSaml) | **Post** /create-auth-method-saml | Create a new Auth Method that will be able to authentication using SAML
[**CreateDynamicSecret**](DefaultApi.md#CreateDynamicSecret) | **Post** /create-dynamic-secret | Creates a new dynamic secret item
[**CreateKey**](DefaultApi.md#CreateKey) | **Post** /create-key | Creates a new key
[**CreateRole**](DefaultApi.md#CreateRole) | **Post** /create-role | Creates a new role
[**CreateSecret**](DefaultApi.md#CreateSecret) | **Post** /create-secret | Creates a new secret item
[**CreateSshCertIssuer**](DefaultApi.md#CreateSshCertIssuer) | **Post** /create-ssh-cert-issuer | Creates a new SSH certificate issuer
[**Decrypt**](DefaultApi.md#Decrypt) | **Post** /decrypt | Decrypts ciphertext into plaintext by using an AES key
[**DecryptFile**](DefaultApi.md#DecryptFile) | **Post** /decrypt-file | Decrypts a file by using an AES key
[**DecryptPkcs1**](DefaultApi.md#DecryptPkcs1) | **Post** /decrypt-pkcs1 | Decrypts a plaintext using RSA and the padding scheme from PKCS#1 v1.5
[**DeleteAssoc**](DefaultApi.md#DeleteAssoc) | **Post** /delete-assoc | Delete an association between role and auth method
[**DeleteAuthMethod**](DefaultApi.md#DeleteAuthMethod) | **Post** /delete-auth-method | Delete the Auth Method
[**DeleteItem**](DefaultApi.md#DeleteItem) | **Post** /delete-item | Delete an item
[**DeleteRole**](DefaultApi.md#DeleteRole) | **Post** /delete-role | Delete a role
[**DeleteRoleRule**](DefaultApi.md#DeleteRoleRule) | **Post** /delete-role-rule | Delete a rule from a role
[**DescribeItem**](DefaultApi.md#DescribeItem) | **Post** /describe-item | Returns the item details
[**Encrypt**](DefaultApi.md#Encrypt) | **Post** /encrypt | Encrypts plaintext into ciphertext by using an AES key
[**EncryptFile**](DefaultApi.md#EncryptFile) | **Post** /encrypt-file | Encrypts a file by using an AES key
[**EncryptPkcs1**](DefaultApi.md#EncryptPkcs1) | **Post** /encrypt-pkcs1 | Encrypts the given message with RSA and the padding scheme from PKCS#1 v1.5
[**GetAuthMethod**](DefaultApi.md#GetAuthMethod) | **Post** /get-auth-method | Returns an information about the Auth Method
[**GetDynamicSecretValue**](DefaultApi.md#GetDynamicSecretValue) | **Post** /get-dynamic-secret-value | Get dynamic secret value
[**GetRole**](DefaultApi.md#GetRole) | **Post** /get-role | Get role details
[**GetRsaPublic**](DefaultApi.md#GetRsaPublic) | **Post** /get-rsa-public | Obtain the public key from a specific RSA private key
[**GetSecretValue**](DefaultApi.md#GetSecretValue) | **Post** /get-secret-value | Get static secret value
[**GetSshCertificate**](DefaultApi.md#GetSshCertificate) | **Post** /get-ssh-certificate | Generates SSH certificate
[**Help**](DefaultApi.md#Help) | **Post** /help | help text
[**ListAuthMethods**](DefaultApi.md#ListAuthMethods) | **Post** /list-auth-methods | Returns a list of all the Auth Methods in the account
[**ListItems**](DefaultApi.md#ListItems) | **Post** /list-items | Returns a list of all accessible items
[**ListRoles**](DefaultApi.md#ListRoles) | **Post** /list-roles | Returns a list of all roles in the account
[**SetRoleRule**](DefaultApi.md#SetRoleRule) | **Post** /set-role-rule | Set a rule to a role
[**SignPkcs1**](DefaultApi.md#SignPkcs1) | **Post** /sign-pkcs1 | Calculates the signature of hashed using RSASSA-PKCS1-V1_5-SIGN from RSA PKCS#1 v1.5
[**Unconfigure**](DefaultApi.md#Unconfigure) | **Post** /unconfigure | Remove Configuration of client profile.
[**UpdateItem**](DefaultApi.md#UpdateItem) | **Post** /update-item | Update item name and metadata
[**UpdateRole**](DefaultApi.md#UpdateRole) | **Post** /update-role | Update role details
[**UpdateSecretVal**](DefaultApi.md#UpdateSecretVal) | **Post** /update-secret-val | Update static secret value
[**UploadPkcs12**](DefaultApi.md#UploadPkcs12) | **Post** /upload-pkcs12 | Upload a PKCS#12 key and certificates
[**UploadRsa**](DefaultApi.md#UploadRsa) | **Post** /upload-rsa | Upload RSA key
[**VerifyPkcs1**](DefaultApi.md#VerifyPkcs1) | **Post** /verify-pkcs1 | Verifies an RSA PKCS#1 v1.5 signature


# **AssocRoleAm**
> ReplyObj AssocRoleAm(ctx, roleName, amName, token, optional)
Create an association between role and auth method

Create an association between role and auth method Options:   role-name -    The role name to associate   am-name -    The auth method name to associate   sub-claims -    key/val of sub claims, ex. group=admins,developers   token -    Access token

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **roleName** | **string**| The role name to associate | 
  **amName** | **string**| The auth method name to associate | 
  **token** | **string**| Access token | 
 **optional** | ***AssocRoleAmOpts** | optional parameters | nil if no parameters

### Optional Parameters
Optional parameters are passed through a pointer to a AssocRoleAmOpts struct

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------



 **subClaims** | **optional.String**| key/val of sub claims, ex. group&#x3D;admins,developers | 

### Return type

[**ReplyObj**](ReplyObj.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **Auth**
> ReplyObj Auth(ctx, accessId, optional)
Authenticate to the service and returns a token to be used as a profile to execute the CLI without the need for re-authentication

Authenticate to the service and returns a token to be used as a profile to execute the CLI without the need for re-authentication Options:   access-id -    Access ID   access-type -    Access Type (api_key/okta_saml/ldap)   access-key -    Access key (relevant only for access-type=api_key)   ldap_proxy_url -    Address URL for LDAP proxy (relevant only for access-type=ldap)

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **accessId** | **string**| Access ID | 
 **optional** | ***AuthOpts** | optional parameters | nil if no parameters

### Optional Parameters
Optional parameters are passed through a pointer to a AuthOpts struct

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **accessType** | **optional.String**| Access Type (api_key/okta_saml/ldap) | 
 **accessKey** | **optional.String**| Access key (relevant only for access-type&#x3D;api_key) | 
 **ldapProxyUrl** | **optional.String**| Address URL for LDAP proxy (relevant only for access-type&#x3D;ldap) | 

### Return type

[**ReplyObj**](ReplyObj.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **Configure**
> ReplyObj Configure(ctx, accessId, optional)
Configure client profile.

Configure client profile. Options:   access-id -    Access ID   access-key -    Access Key   access-type -    Access Type (api_key/azure_ad/okta_saml/ldap)   ldap_proxy_url -    Address URL for ldap proxy (relevant only for access-type=ldap)   azure_ad_object_id -    Azure Active Directory ObjectId (relevant only for access-type=azure_ad)

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **accessId** | **string**| Access ID | 
 **optional** | ***ConfigureOpts** | optional parameters | nil if no parameters

### Optional Parameters
Optional parameters are passed through a pointer to a ConfigureOpts struct

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **accessKey** | **optional.String**| Access Key | 
 **accessType** | **optional.String**| Access Type (api_key/azure_ad/okta_saml/ldap) | 
 **ldapProxyUrl** | **optional.String**| Address URL for ldap proxy (relevant only for access-type&#x3D;ldap) | 
 **azureAdObjectId** | **optional.String**| Azure Active Directory ObjectId (relevant only for access-type&#x3D;azure_ad) | 

### Return type

[**ReplyObj**](ReplyObj.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **CreateAuthMethod**
> ReplyObj CreateAuthMethod(ctx, name, token, optional)
Create a new Auth Method in the account

Create a new Auth Method in the account Options:   name -    Auth Method name   access-expires -    Access expiration date in Unix timestamp (select 0 for access without expiry date)   bound-ips -    A CIDR whitelist with the IPs that the access is restricted to   token -    Access token

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **name** | **string**| Auth Method name | 
  **token** | **string**| Access token | 
 **optional** | ***CreateAuthMethodOpts** | optional parameters | nil if no parameters

### Optional Parameters
Optional parameters are passed through a pointer to a CreateAuthMethodOpts struct

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------


 **accessExpires** | **optional.String**| Access expiration date in Unix timestamp (select 0 for access without expiry date) | 
 **boundIps** | **optional.String**| A CIDR whitelist with the IPs that the access is restricted to | 

### Return type

[**ReplyObj**](ReplyObj.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **CreateAuthMethodAzureAd**
> ReplyObj CreateAuthMethodAzureAd(ctx, name, boundTenantId, token, optional)
Create a new Auth Method that will be able to authentication using Azure Active Directory credentials

Create a new Auth Method that will be able to authentication using Azure Active Directory credentials Options:   name -    Auth Method name   access-expires -    Access expiration date in Unix timestamp (select 0 for access without expiry date)   bound-ips -    A CIDR whitelist of the IPs that the access is restricted to   bound-tenant-id -    The Azure tenant id that the access is restricted to   issuer -    Issuer URL   jwks-uri -    The URL to the JSON Web Key Set (JWKS) that containing the public keys that should be used to verify any JSON Web Token (JWT) issued by the authorization server.   audience -    The audience in the JWT   bound-spid -    A list of service principal IDs that the access is restricted to   bound-group-id -    A list of group ids that the access is restricted to   bound-sub-id -    A list of subscription ids that the access is restricted to   bound-rg-id -    A list of resource groups that the access is restricted to   bound-providers -    A list of resource providers that the access is restricted to (e.g, Microsoft.Compute, Microsoft.ManagedIdentity, etc)   bound-resource-types -    A list of resource types that the access is restricted to (e.g, virtualMachines, userAssignedIdentities, etc)   bound-resource-names -    A list of resource names that the access is restricted to (e.g, a virtual machine name, scale set name, etc).   bound-resource-id -    A list of full resource ids that the access is restricted to   token -    Access token

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **name** | **string**| Auth Method name | 
  **boundTenantId** | **string**| The Azure tenant id that the access is restricted to | 
  **token** | **string**| Access token | 
 **optional** | ***CreateAuthMethodAzureAdOpts** | optional parameters | nil if no parameters

### Optional Parameters
Optional parameters are passed through a pointer to a CreateAuthMethodAzureAdOpts struct

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------



 **accessExpires** | **optional.String**| Access expiration date in Unix timestamp (select 0 for access without expiry date) | 
 **boundIps** | **optional.String**| A CIDR whitelist of the IPs that the access is restricted to | 
 **issuer** | **optional.String**| Issuer URL | 
 **jwksUri** | **optional.String**| The URL to the JSON Web Key Set (JWKS) that containing the public keys that should be used to verify any JSON Web Token (JWT) issued by the authorization server. | 
 **audience** | **optional.String**| The audience in the JWT | 
 **boundSpid** | **optional.String**| A list of service principal IDs that the access is restricted to | 
 **boundGroupId** | **optional.String**| A list of group ids that the access is restricted to | 
 **boundSubId** | **optional.String**| A list of subscription ids that the access is restricted to | 
 **boundRgId** | **optional.String**| A list of resource groups that the access is restricted to | 
 **boundProviders** | **optional.String**| A list of resource providers that the access is restricted to (e.g, Microsoft.Compute, Microsoft.ManagedIdentity, etc) | 
 **boundResourceTypes** | **optional.String**| A list of resource types that the access is restricted to (e.g, virtualMachines, userAssignedIdentities, etc) | 
 **boundResourceNames** | **optional.String**| A list of resource names that the access is restricted to (e.g, a virtual machine name, scale set name, etc). | 
 **boundResourceId** | **optional.String**| A list of full resource ids that the access is restricted to | 

### Return type

[**ReplyObj**](ReplyObj.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **CreateAuthMethodLdap**
> ReplyObj CreateAuthMethodLdap(ctx, name, publicKeyFilePath, token, optional)
Create a new Auth Method that will be able to authentication using LDAP

Create a new Auth Method that will be able to authentication using LDAP Options:   name -    Auth Method name   access-expires -    Access expiration date in Unix timestamp (select 0 for access without expiry date)   bound-ips -    A CIDR whitelist of the IPs that the access is restricted to   public-key-file-path -    A public key generated for LDAP authentication method on Akeyless [RSA2048]   token -    Access token

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **name** | **string**| Auth Method name | 
  **publicKeyFilePath** | **string**| A public key generated for LDAP authentication method on Akeyless [RSA2048] | 
  **token** | **string**| Access token | 
 **optional** | ***CreateAuthMethodLdapOpts** | optional parameters | nil if no parameters

### Optional Parameters
Optional parameters are passed through a pointer to a CreateAuthMethodLdapOpts struct

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------



 **accessExpires** | **optional.String**| Access expiration date in Unix timestamp (select 0 for access without expiry date) | 
 **boundIps** | **optional.String**| A CIDR whitelist of the IPs that the access is restricted to | 

### Return type

[**ReplyObj**](ReplyObj.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **CreateAuthMethodOauth2**
> ReplyObj CreateAuthMethodOauth2(ctx, name, boundClientsIds, issuer, jwksUri, audience, token, optional)
Create a new Auth Method that will be able to authentication using OpenId/OAuth2

Create a new Auth Method that will be able to authentication using OpenId/OAuth2 Options:   name -    Auth Method name   access-expires -    Access expiration date in Unix timestamp (select 0 for access without expiry date)   bound-ips -    A CIDR whitelist of the IPs that the access is restricted to   bound-clients-ids -    The clients ids that the access is restricted to   issuer -    Issuer URL   jwks-uri -    The URL to the JSON Web Key Set (JWKS) that containing the public keys that should be used to verify any JSON Web Token (JWT) issued by the authorization server.   audience -    The audience in the JWT   token -    Access token

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **name** | **string**| Auth Method name | 
  **boundClientsIds** | **string**| The clients ids that the access is restricted to | 
  **issuer** | **string**| Issuer URL | 
  **jwksUri** | **string**| The URL to the JSON Web Key Set (JWKS) that containing the public keys that should be used to verify any JSON Web Token (JWT) issued by the authorization server. | 
  **audience** | **string**| The audience in the JWT | 
  **token** | **string**| Access token | 
 **optional** | ***CreateAuthMethodOauth2Opts** | optional parameters | nil if no parameters

### Optional Parameters
Optional parameters are passed through a pointer to a CreateAuthMethodOauth2Opts struct

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------






 **accessExpires** | **optional.String**| Access expiration date in Unix timestamp (select 0 for access without expiry date) | 
 **boundIps** | **optional.String**| A CIDR whitelist of the IPs that the access is restricted to | 

### Return type

[**ReplyObj**](ReplyObj.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **CreateAuthMethodSaml**
> ReplyObj CreateAuthMethodSaml(ctx, name, idpMetadataUrl, token, optional)
Create a new Auth Method that will be able to authentication using SAML

Create a new Auth Method that will be able to authentication using SAML Options:   name -    Auth Method name   access-expires -    Access expiration date in Unix timestamp (select 0 for access without expiry date)   bound-ips -    A CIDR whitelist of the IPs that the access is restricted to   idp-metadata-url -    IDP metadata url   token -    Access token

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **name** | **string**| Auth Method name | 
  **idpMetadataUrl** | **string**| IDP metadata url | 
  **token** | **string**| Access token | 
 **optional** | ***CreateAuthMethodSamlOpts** | optional parameters | nil if no parameters

### Optional Parameters
Optional parameters are passed through a pointer to a CreateAuthMethodSamlOpts struct

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------



 **accessExpires** | **optional.String**| Access expiration date in Unix timestamp (select 0 for access without expiry date) | 
 **boundIps** | **optional.String**| A CIDR whitelist of the IPs that the access is restricted to | 

### Return type

[**ReplyObj**](ReplyObj.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **CreateDynamicSecret**
> ReplyObj CreateDynamicSecret(ctx, name, token, optional)
Creates a new dynamic secret item

Creates a new dynamic secret item Options:   name -    Dynamic secret name   metadata -    Metadata about the dynamic secret   key -    The name of a key that used to encrypt the dynamic secret values (if empty, the account default protectionKey key will be used)   token -    Access token

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **name** | **string**| Dynamic secret name | 
  **token** | **string**| Access token | 
 **optional** | ***CreateDynamicSecretOpts** | optional parameters | nil if no parameters

### Optional Parameters
Optional parameters are passed through a pointer to a CreateDynamicSecretOpts struct

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------


 **metadata** | **optional.String**| Metadata about the dynamic secret | 
 **key** | **optional.String**| The name of a key that used to encrypt the dynamic secret values (if empty, the account default protectionKey key will be used) | 

### Return type

[**ReplyObj**](ReplyObj.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **CreateKey**
> ReplyObj CreateKey(ctx, name, alg, token, optional)
Creates a new key

Creates a new key Options:   name -    Key name   alg -    Key type. options- [AES128GCM, AES256GCM, AES128SIV, AES256SIV, RSA1024, RSA2048]   metadata -    Metadata about the key   split-level -    The number of fragments that the item will be split into (not includes customer fragment)   customer-frg-id -    The customer fragment ID that will be used to create the key (if empty, the key will be created independently of a customer fragment)   token -    Access token

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **name** | **string**| Key name | 
  **alg** | **string**| Key type. options- [AES128GCM, AES256GCM, AES128SIV, AES256SIV, RSA1024, RSA2048] | 
  **token** | **string**| Access token | 
 **optional** | ***CreateKeyOpts** | optional parameters | nil if no parameters

### Optional Parameters
Optional parameters are passed through a pointer to a CreateKeyOpts struct

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------



 **metadata** | **optional.String**| Metadata about the key | 
 **splitLevel** | **optional.String**| The number of fragments that the item will be split into (not includes customer fragment) | 
 **customerFrgId** | **optional.String**| The customer fragment ID that will be used to create the key (if empty, the key will be created independently of a customer fragment) | 

### Return type

[**ReplyObj**](ReplyObj.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **CreateRole**
> ReplyObj CreateRole(ctx, name, token, optional)
Creates a new role

Creates a new role Options:   name -    Role name   comment -    Comment about the role   token -    Access token

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **name** | **string**| Role name | 
  **token** | **string**| Access token | 
 **optional** | ***CreateRoleOpts** | optional parameters | nil if no parameters

### Optional Parameters
Optional parameters are passed through a pointer to a CreateRoleOpts struct

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------


 **comment** | **optional.String**| Comment about the role | 

### Return type

[**ReplyObj**](ReplyObj.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **CreateSecret**
> ReplyObj CreateSecret(ctx, name, value, token, optional)
Creates a new secret item

Creates a new secret item Options:   name -    Secret name   value -    The secret value   metadata -    Metadata about the secret   key -    The name of a key that used to encrypt the secret value (if empty, the account default protectionKey key will be used)   multiline -    The provided value is a multiline value (separated by '\\n')   token -    Access token

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **name** | **string**| Secret name | 
  **value** | **string**| The secret value | 
  **token** | **string**| Access token | 
 **optional** | ***CreateSecretOpts** | optional parameters | nil if no parameters

### Optional Parameters
Optional parameters are passed through a pointer to a CreateSecretOpts struct

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------



 **metadata** | **optional.String**| Metadata about the secret | 
 **key** | **optional.String**| The name of a key that used to encrypt the secret value (if empty, the account default protectionKey key will be used) | 
 **multiline** | **optional.Bool**| The provided value is a multiline value (separated by &#39;\\n&#39;) | 

### Return type

[**ReplyObj**](ReplyObj.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **CreateSshCertIssuer**
> ReplyObj CreateSshCertIssuer(ctx, name, signerKeyName, allowedUsers, expirationSec, token, optional)
Creates a new SSH certificate issuer

Creates a new SSH certificate issuer Options:   name -    SSH certificate issuer name   signer-key-name -    A key to sign the certificate with   allowed-users -    Users allowed to fetch the certificate, ex. root,ubuntu   principals -    Signed certificates with principal, ex. example_role1,example_role2   extensions -    Signed certificates with extensions, ex. permit-port-forwarding=\"\"   expiration-sec -    Signed certificates with expiration, use second units   metadata -    A metadata about the issuer   token -    Access token

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **name** | **string**| SSH certificate issuer name | 
  **signerKeyName** | **string**| A key to sign the certificate with | 
  **allowedUsers** | **string**| Users allowed to fetch the certificate, ex. root,ubuntu | 
  **expirationSec** | **string**| Signed certificates with expiration, use second units | 
  **token** | **string**| Access token | 
 **optional** | ***CreateSshCertIssuerOpts** | optional parameters | nil if no parameters

### Optional Parameters
Optional parameters are passed through a pointer to a CreateSshCertIssuerOpts struct

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------





 **principals** | **optional.String**| Signed certificates with principal, ex. example_role1,example_role2 | 
 **extensions** | **optional.String**| Signed certificates with extensions, ex. permit-port-forwarding&#x3D;\&quot;\&quot; | 
 **metadata** | **optional.String**| A metadata about the issuer | 

### Return type

[**ReplyObj**](ReplyObj.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **Decrypt**
> ReplyObj Decrypt(ctx, keyName, ciphertext, token, optional)
Decrypts ciphertext into plaintext by using an AES key

Decrypts ciphertext into plaintext by using an AES key Options:   key-name -    The name of the key to use in the decryption process   ciphertext -    Ciphertext to be decrypted in base64 encoded format   encryption-context -    The encryption context. If this was specified in the encrypt command, it must be specified here or the decryption operation will fail   token -    Access token

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **keyName** | **string**| The name of the key to use in the decryption process | 
  **ciphertext** | **string**| Ciphertext to be decrypted in base64 encoded format | 
  **token** | **string**| Access token | 
 **optional** | ***DecryptOpts** | optional parameters | nil if no parameters

### Optional Parameters
Optional parameters are passed through a pointer to a DecryptOpts struct

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------



 **encryptionContext** | **optional.String**| The encryption context. If this was specified in the encrypt command, it must be specified here or the decryption operation will fail | 

### Return type

[**ReplyObj**](ReplyObj.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **DecryptFile**
> ReplyObj DecryptFile(ctx, keyName, in, token, optional)
Decrypts a file by using an AES key

Decrypts a file by using an AES key Options:   key-name -    The name of the key to use in the decryption process   in -    Path to the file to be decrypted. If not provided, the content will be taken from stdin   out -    Path to the output file. If not provided, the output will be sent to stdout   encryption-context -    The encryption context. If this was specified in the encrypt command, it must be specified here or the decryption operation will fail   token -    Access token

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **keyName** | **string**| The name of the key to use in the decryption process | 
  **in** | **string**| Path to the file to be decrypted. If not provided, the content will be taken from stdin | 
  **token** | **string**| Access token | 
 **optional** | ***DecryptFileOpts** | optional parameters | nil if no parameters

### Optional Parameters
Optional parameters are passed through a pointer to a DecryptFileOpts struct

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------



 **out** | **optional.String**| Path to the output file. If not provided, the output will be sent to stdout | 
 **encryptionContext** | **optional.String**| The encryption context. If this was specified in the encrypt command, it must be specified here or the decryption operation will fail | 

### Return type

[**ReplyObj**](ReplyObj.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **DecryptPkcs1**
> ReplyObj DecryptPkcs1(ctx, keyName, ciphertext, token)
Decrypts a plaintext using RSA and the padding scheme from PKCS#1 v1.5

Decrypts a plaintext using RSA and the padding scheme from PKCS#1 v1.5 Options:   key-name -    The name of the RSA key to use in the decryption process   ciphertext -    Ciphertext to be decrypted in base64 encoded format   token -    Access token

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **keyName** | **string**| The name of the RSA key to use in the decryption process | 
  **ciphertext** | **string**| Ciphertext to be decrypted in base64 encoded format | 
  **token** | **string**| Access token | 

### Return type

[**ReplyObj**](ReplyObj.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **DeleteAssoc**
> ReplyObj DeleteAssoc(ctx, assocId, token)
Delete an association between role and auth method

Delete an association between role and auth method Options:   assoc-id -    The association id to be deleted   token -    Access token

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **assocId** | **string**| The association id to be deleted | 
  **token** | **string**| Access token | 

### Return type

[**ReplyObj**](ReplyObj.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **DeleteAuthMethod**
> ReplyObj DeleteAuthMethod(ctx, name, token)
Delete the Auth Method

Delete the Auth Method Options:   name -    Auth Method name   token -    Access token

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **name** | **string**| Auth Method name | 
  **token** | **string**| Access token | 

### Return type

[**ReplyObj**](ReplyObj.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **DeleteItem**
> ReplyObj DeleteItem(ctx, name, token)
Delete an item

Delete an item Options:   name -    Item name   token -    Access token

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **name** | **string**| Item name | 
  **token** | **string**| Access token | 

### Return type

[**ReplyObj**](ReplyObj.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **DeleteRole**
> ReplyObj DeleteRole(ctx, name, token)
Delete a role

Delete a role Options:   name -    Role name   token -    Access token

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **name** | **string**| Role name | 
  **token** | **string**| Access token | 

### Return type

[**ReplyObj**](ReplyObj.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **DeleteRoleRule**
> ReplyObj DeleteRoleRule(ctx, roleName, path, token)
Delete a rule from a role

Delete a rule from a role Options:   role-name -    The role name to be updated   path -    The path the rule refers to   token -    Access token

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **roleName** | **string**| The role name to be updated | 
  **path** | **string**| The path the rule refers to | 
  **token** | **string**| Access token | 

### Return type

[**ReplyObj**](ReplyObj.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **DescribeItem**
> ReplyObj DescribeItem(ctx, name, token)
Returns the item details

Returns the item details Options:   name -    Item name   token -    Access token

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **name** | **string**| Item name | 
  **token** | **string**| Access token | 

### Return type

[**ReplyObj**](ReplyObj.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **Encrypt**
> ReplyObj Encrypt(ctx, keyName, plaintext, token, optional)
Encrypts plaintext into ciphertext by using an AES key

Encrypts plaintext into ciphertext by using an AES key Options:   key-name -    The name of the key to use in the encryption process   plaintext -    Data to be encrypted   encryption-context -    name-value pair that specifies the encryption context to be used for authenticated encryption. If used here, the same value must be supplied to the decrypt command or decryption will fail   token -    Access token

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **keyName** | **string**| The name of the key to use in the encryption process | 
  **plaintext** | **string**| Data to be encrypted | 
  **token** | **string**| Access token | 
 **optional** | ***EncryptOpts** | optional parameters | nil if no parameters

### Optional Parameters
Optional parameters are passed through a pointer to a EncryptOpts struct

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------



 **encryptionContext** | **optional.String**| name-value pair that specifies the encryption context to be used for authenticated encryption. If used here, the same value must be supplied to the decrypt command or decryption will fail | 

### Return type

[**ReplyObj**](ReplyObj.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **EncryptFile**
> ReplyObj EncryptFile(ctx, keyName, in, token, optional)
Encrypts a file by using an AES key

Encrypts a file by using an AES key Options:   key-name -    The name of the key to use in the encryption process   in -    Path to the file to be encrypted. If not provided, the content will be taken from stdin   out -    Path to the output file. If not provided, the output will be sent to stdout   encryption-context -    name-value pair that specifies the encryption context to be used for authenticated encryption. If used here, the same value must be supplied to the decrypt command or decryption will fail   token -    Access token

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **keyName** | **string**| The name of the key to use in the encryption process | 
  **in** | **string**| Path to the file to be encrypted. If not provided, the content will be taken from stdin | 
  **token** | **string**| Access token | 
 **optional** | ***EncryptFileOpts** | optional parameters | nil if no parameters

### Optional Parameters
Optional parameters are passed through a pointer to a EncryptFileOpts struct

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------



 **out** | **optional.String**| Path to the output file. If not provided, the output will be sent to stdout | 
 **encryptionContext** | **optional.String**| name-value pair that specifies the encryption context to be used for authenticated encryption. If used here, the same value must be supplied to the decrypt command or decryption will fail | 

### Return type

[**ReplyObj**](ReplyObj.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **EncryptPkcs1**
> ReplyObj EncryptPkcs1(ctx, keyName, plaintext, token)
Encrypts the given message with RSA and the padding scheme from PKCS#1 v1.5

Encrypts the given message with RSA and the padding scheme from PKCS#1 v1.5 Options:   key-name -    The name of the RSA key to use in the encryption process   plaintext -    Data to be encrypted   token -    Access token

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **keyName** | **string**| The name of the RSA key to use in the encryption process | 
  **plaintext** | **string**| Data to be encrypted | 
  **token** | **string**| Access token | 

### Return type

[**ReplyObj**](ReplyObj.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **GetAuthMethod**
> ReplyObj GetAuthMethod(ctx, name, token)
Returns an information about the Auth Method

Returns an information about the Auth Method Options:   name -    Auth Method name   token -    Access token

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **name** | **string**| Auth Method name | 
  **token** | **string**| Access token | 

### Return type

[**ReplyObj**](ReplyObj.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **GetDynamicSecretValue**
> ReplyObj GetDynamicSecretValue(ctx, name, token)
Get dynamic secret value

Get dynamic secret value Options:   name -    Dynamic secret name   token -    Access token

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **name** | **string**| Dynamic secret name | 
  **token** | **string**| Access token | 

### Return type

[**ReplyObj**](ReplyObj.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **GetRole**
> ReplyObj GetRole(ctx, name, token)
Get role details

Get role details Options:   name -    Role name   token -    Access token

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **name** | **string**| Role name | 
  **token** | **string**| Access token | 

### Return type

[**ReplyObj**](ReplyObj.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **GetRsaPublic**
> ReplyObj GetRsaPublic(ctx, name, token)
Obtain the public key from a specific RSA private key

Obtain the public key from a specific RSA private key Options:   name -    Name of key to be created   token -    Access token

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **name** | **string**| Name of key to be created | 
  **token** | **string**| Access token | 

### Return type

[**ReplyObj**](ReplyObj.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **GetSecretValue**
> ReplyObj GetSecretValue(ctx, name, token)
Get static secret value

Get static secret value Options:   name -    Secret name   token -    Access token

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **name** | **string**| Secret name | 
  **token** | **string**| Access token | 

### Return type

[**ReplyObj**](ReplyObj.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **GetSshCertificate**
> ReplyObj GetSshCertificate(ctx, certUsername, certIssuerName, publicKeyFilePath, token)
Generates SSH certificate

Generates SSH certificate Options:   cert-username -    The username to sign in the SSH certificate   cert-issuer-name -    The name of the SSH certificate issuer   public-key-file-path -    SSH public key   token -    Access token

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **certUsername** | **string**| The username to sign in the SSH certificate | 
  **certIssuerName** | **string**| The name of the SSH certificate issuer | 
  **publicKeyFilePath** | **string**| SSH public key | 
  **token** | **string**| Access token | 

### Return type

[**ReplyObj**](ReplyObj.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **Help**
> ReplyObj Help(ctx, )
help text

help text

### Required Parameters
This endpoint does not need any parameter.

### Return type

[**ReplyObj**](ReplyObj.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **ListAuthMethods**
> ReplyObj ListAuthMethods(ctx, token)
Returns a list of all the Auth Methods in the account

Returns a list of all the Auth Methods in the account Options:   token -    Access token

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **token** | **string**| Access token | 

### Return type

[**ReplyObj**](ReplyObj.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **ListItems**
> ReplyObj ListItems(ctx, token, optional)
Returns a list of all accessible items

Returns a list of all accessible items Options:   type -    The item types list of the requested items. In case it is empty, all types of items will be returned. options- [key, static-secret, dynamic-secret]   ItemsTypes -    ItemsTypes   path -    Path to folder   token -    Access token

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **token** | **string**| Access token | 
 **optional** | ***ListItemsOpts** | optional parameters | nil if no parameters

### Optional Parameters
Optional parameters are passed through a pointer to a ListItemsOpts struct

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **type_** | **optional.String**| The item types list of the requested items. In case it is empty, all types of items will be returned. options- [key, static-secret, dynamic-secret] | 
 **itemsTypes** | **optional.String**| ItemsTypes | 
 **path** | **optional.String**| Path to folder | 

### Return type

[**ReplyObj**](ReplyObj.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **ListRoles**
> ReplyObj ListRoles(ctx, token)
Returns a list of all roles in the account

Returns a list of all roles in the account Options:   token -    Access token

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **token** | **string**| Access token | 

### Return type

[**ReplyObj**](ReplyObj.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **SetRoleRule**
> ReplyObj SetRoleRule(ctx, roleName, path, capability, token)
Set a rule to a role

Set a rule to a role Options:   role-name -    The role name to be updated   path -    The path the rule refers to   capability -    List of the approved/denied capabilities in the path options- [read, create, update, delete, list, deny]   token -    Access token

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **roleName** | **string**| The role name to be updated | 
  **path** | **string**| The path the rule refers to | 
  **capability** | **string**| List of the approved/denied capabilities in the path options- [read, create, update, delete, list, deny] | 
  **token** | **string**| Access token | 

### Return type

[**ReplyObj**](ReplyObj.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **SignPkcs1**
> ReplyObj SignPkcs1(ctx, keyName, message, token)
Calculates the signature of hashed using RSASSA-PKCS1-V1_5-SIGN from RSA PKCS#1 v1.5

Calculates the signature of hashed using RSASSA-PKCS1-V1_5-SIGN from RSA PKCS#1 v1.5 Options:   key-name -    The name of the RSA key to use in the signing process   message -    The message to be signed   token -    Access token

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **keyName** | **string**| The name of the RSA key to use in the signing process | 
  **message** | **string**| The message to be signed | 
  **token** | **string**| Access token | 

### Return type

[**ReplyObj**](ReplyObj.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **Unconfigure**
> ReplyObj Unconfigure(ctx, token)
Remove Configuration of client profile.

Remove Configuration of client profile. Options:   token -    Access token

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **token** | **string**| Access token | 

### Return type

[**ReplyObj**](ReplyObj.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **UpdateItem**
> ReplyObj UpdateItem(ctx, name, token, optional)
Update item name and metadata

Update item name and metadata Options:   name -    Current item name   new-name -    New item name   new-metadata -    New item metadata   token -    Access token

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **name** | **string**| Current item name | 
  **token** | **string**| Access token | 
 **optional** | ***UpdateItemOpts** | optional parameters | nil if no parameters

### Optional Parameters
Optional parameters are passed through a pointer to a UpdateItemOpts struct

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------


 **newName** | **optional.String**| New item name | 
 **newMetadata** | **optional.String**| New item metadata | 

### Return type

[**ReplyObj**](ReplyObj.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **UpdateRole**
> ReplyObj UpdateRole(ctx, name, token, optional)
Update role details

Update role details Options:   name -    Role name   new-name -    New Role name   new-comment -    New comment about the role   token -    Access token

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **name** | **string**| Role name | 
  **token** | **string**| Access token | 
 **optional** | ***UpdateRoleOpts** | optional parameters | nil if no parameters

### Optional Parameters
Optional parameters are passed through a pointer to a UpdateRoleOpts struct

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------


 **newName** | **optional.String**| New Role name | 
 **newComment** | **optional.String**| New comment about the role | 

### Return type

[**ReplyObj**](ReplyObj.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **UpdateSecretVal**
> ReplyObj UpdateSecretVal(ctx, name, value, token, optional)
Update static secret value

Update static secret value Options:   name -    Secret name   value -    The new secret value   key -    The name of a key that used to encrypt the secret value (if empty, the account default protectionKey key will be used)   multiline -    The provided value is a multiline value (separated by '\\n')   token -    Access token

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **name** | **string**| Secret name | 
  **value** | **string**| The new secret value | 
  **token** | **string**| Access token | 
 **optional** | ***UpdateSecretValOpts** | optional parameters | nil if no parameters

### Optional Parameters
Optional parameters are passed through a pointer to a UpdateSecretValOpts struct

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------



 **key** | **optional.String**| The name of a key that used to encrypt the secret value (if empty, the account default protectionKey key will be used) | 
 **multiline** | **optional.Bool**| The provided value is a multiline value (separated by &#39;\\n&#39;) | 

### Return type

[**ReplyObj**](ReplyObj.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **UploadPkcs12**
> ReplyObj UploadPkcs12(ctx, name, in, passphrase, token, optional)
Upload a PKCS#12 key and certificates

Upload a PKCS#12 key and certificates Options:   name -    Name of key to be created   in -    PKCS#12 input file (private key and certificate only)   passphrase -    Passphrase to unlock the pkcs#12 bundle   metadata -    A metadata about the key   split-level -    The number of fragments that the item will be split into   customer-frg-id -    The customer fragment ID that will be used to split the key (if empty, the key will be created independently of a customer fragment)   cert -    Path to a file that contain the certificate in a PEM format. If this parameter is not empty, the certificate will be taken from here and not from the PKCS#12 input file   token -    Access token

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **name** | **string**| Name of key to be created | 
  **in** | **string**| PKCS#12 input file (private key and certificate only) | 
  **passphrase** | **string**| Passphrase to unlock the pkcs#12 bundle | 
  **token** | **string**| Access token | 
 **optional** | ***UploadPkcs12Opts** | optional parameters | nil if no parameters

### Optional Parameters
Optional parameters are passed through a pointer to a UploadPkcs12Opts struct

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------




 **metadata** | **optional.String**| A metadata about the key | 
 **splitLevel** | **optional.String**| The number of fragments that the item will be split into | 
 **customerFrgId** | **optional.String**| The customer fragment ID that will be used to split the key (if empty, the key will be created independently of a customer fragment) | 
 **cert** | **optional.String**| Path to a file that contain the certificate in a PEM format. If this parameter is not empty, the certificate will be taken from here and not from the PKCS#12 input file | 

### Return type

[**ReplyObj**](ReplyObj.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **UploadRsa**
> ReplyObj UploadRsa(ctx, name, alg, rsaKeyFilePath, token, optional)
Upload RSA key

Upload RSA key Options:   name -    Name of key to be created   alg -    Key type. options- [RSA1024, RSA2048]   rsa-key-file-path -    RSA private key file path   metadata -    A metadata about the key   split-level -    The number of fragments that the item will be split into   customer-frg-id -    The customer fragment ID that will be used to split the key (if empty, the key will be created independently of a customer fragment)   token -    Access token

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **name** | **string**| Name of key to be created | 
  **alg** | **string**| Key type. options- [RSA1024, RSA2048] | 
  **rsaKeyFilePath** | **string**| RSA private key file path | 
  **token** | **string**| Access token | 
 **optional** | ***UploadRsaOpts** | optional parameters | nil if no parameters

### Optional Parameters
Optional parameters are passed through a pointer to a UploadRsaOpts struct

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------




 **metadata** | **optional.String**| A metadata about the key | 
 **splitLevel** | **optional.String**| The number of fragments that the item will be split into | 
 **customerFrgId** | **optional.String**| The customer fragment ID that will be used to split the key (if empty, the key will be created independently of a customer fragment) | 

### Return type

[**ReplyObj**](ReplyObj.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **VerifyPkcs1**
> ReplyObj VerifyPkcs1(ctx, keyName, message, signature, token)
Verifies an RSA PKCS#1 v1.5 signature

Verifies an RSA PKCS#1 v1.5 signature Options:   key-name -    The name of the RSA key to use in the verification process   message -    The message to be verified   signature -    The message's signature   token -    Access token

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **keyName** | **string**| The name of the RSA key to use in the verification process | 
  **message** | **string**| The message to be verified | 
  **signature** | **string**| The message&#39;s signature | 
  **token** | **string**| Access token | 

### Return type

[**ReplyObj**](ReplyObj.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

