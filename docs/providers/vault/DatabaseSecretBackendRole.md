# Terraform::Vault::DatabaseSecretBackendRole

Creates a Database Secret Backend role in Vault. Database secret backend
roles can be used to generate dynamic credentials for the database.

~> **Important** All data provided in the resource configuration will be
written in cleartext to state and plan files generated by Terraform, and
will appear in the console output when Terraform runs. Protect these
artifacts accordingly. See
[the main provider documentation](../index.html)
for more details.

## Properties

`Name` - (Required) A unique name to give the role.

`Backend` - (Required) The unique name of the Vault mount to configure.

`DbName` - (Required) The unique name of the database connection to use for
the role.

`CreationStatements` - (Required) The database statements to execute when
creating a user.

`RevocationStatements` - (Optional) The database statements to execute when
revoking a user.

`RollbackStatements` - (Optional) The database statements to execute when
rolling back creation due to an error.

`RenewStatements` - (Optional) The database statements to execute when
renewing a user.

`DefaultTtl` - (Optional) The default number of seconds for leases for this
role.

`MaxTtl` - (Optional) The maximum number of seconds for leases for this
role.


## See Also

* [vault_database_secret_backend_role](https://www.terraform.io/docs/providers/vault/r/database_secret_backend_role.html) in the _Terraform Provider Documentation_