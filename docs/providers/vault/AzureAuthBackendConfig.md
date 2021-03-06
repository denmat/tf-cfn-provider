# Terraform::Vault::AzureAuthBackendConfig

Configures the Azure Auth Backend in Vault.

This resource sets the access key and secret key that Vault will use
when making API requests on behalf of an Azure Auth Backend. It can also
be used to override the URLs Vault uses when making those API requests.

For more information, see the
[Vault docs](https://www.vaultproject.io/api/auth/azure/index.html#configure).

~> **Important** All data provided in the resource configuration will be
written in cleartext to state and plan files generated by Terraform, and
will appear in the console output when Terraform runs. Protect these
artifacts accordingly. See
[the main provider documentation](../index.html)
for more details.

## Properties

`TenantId` - (Required) The tenant id for the Azure Active Directory
organization.

`Resource` - (Required) The configured URL for the application registered in
Azure Active Directory.

`Backend` - (Optional) The path the Azure auth backend being configured was
mounted at.  Defaults to `azure`.

`ClientId` - (Optional) The client id for credentials to query the Azure APIs.
Currently read permissions to query compute resources are required.

`ClientSecret` - (Optional) The client secret for credentials to query the
Azure APIs.

`Environment` - (Optional) The Azure cloud environment. Valid values:
AzurePublicCloud, AzureUSGovernmentCloud, AzureChinaCloud,
AzureGermanCloud.  Defaults to `AzurePublicCloud`.


## See Also

* [vault_azure_auth_backend_config](https://www.terraform.io/docs/providers/vault/r/azure_auth_backend_config.html) in the _Terraform Provider Documentation_