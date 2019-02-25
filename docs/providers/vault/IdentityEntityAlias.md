# Terraform::Vault::IdentityEntityAlias

Creates an Identity Entity Alias for Vault. 

~> **Important** All data provided in the resource configuration will be
written in cleartext to state and plan files generated by Terraform, and
will appear in the console output when Terraform runs. Protect these
artifacts accordingly. See
[the main provider documentation](../index.html)
for more details.

## Properties

`Name` - (Required) Name of the alias. Name should be the identifier of the client in the authentication source. For example, if the alias belongs to userpass backend, the name should be a valid username within userpass backend. If alias belongs to GitHub, it should be the GitHub username.

`MountAccessor` - (Required) Accessor of the mount to which the alias should belong to.

`CanonicalId` - (Required) Entity ID to which this alias belongs to.


## Return Values

### Fn::GetAtt

`Id` - ID of the entity alias.

## See Also

* [vault_identity_entity_alias](https://www.terraform.io/docs/providers/vault/r/identity_entity_alias.html) in the _Terraform Provider Documentation_