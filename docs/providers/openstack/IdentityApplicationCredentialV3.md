# Terraform::OpenStack::IdentityApplicationCredentialV3

Manages a V3 Application Credential resource within OpenStack Keystone.

~> **Note:** All arguments including the application credential name and secret
will be stored in the raw state as plain-text. [Read more about sensitive data
in state](/docs/state/sensitive-data.html).

~> **Note:** An Application Credential is created within the authenticated user
project scope and is not visible by an admin or other accounts.
The Application Credential visibility is similar to
[`Terraform::OpenStack::ComputeKeypairV2`](compute_keypair_v2.html).

## Properties

`Region` - (Optional) The region in which to obtain the V3 Keystone client.
If omitted, the `Region` argument of the provider is used. Changing this
creates a new application credential.

`Name` - (Required) A name of the application credential. Changing this
creates a new application credential.

`Description` - (Optional) A description of the application credential.
Changing this creates a new application credential.

`Unrestricted` - (Optional) A flag indicating whether the application
credential may be used for creation or destruction of other application
credentials or trusts. Changing this creates a new application credential.

`Secret` - (Optional) The secret for the application credential. If omitted,
it will be generated by the server. Changing this creates a new application
credential.

`Roles` - (Optional) A collection of one or more role names, which this
application credential has to be associated with its project. If omitted,
all the current user's roles within the scoped project will be inherited by
a new application credential. Changing this creates a new application
credential.

`ExpiresAt` - (Optional) The expiration time of the application credential
in the RFC3339 timestamp format (e.g. `2019-03-09T12:58:49Z`). If omitted,
an application credential will never expire. Changing this creates a new
application credential.


## Return Values

### Fn::GetAtt

`Region` - See Properties above.

`Name` - See Properties above.

`Description` - See Properties above.

`Unrestricted` - See Properties above.

`Secret` - See Properties above.

`Roles` - See Properties above.

`ExpiresAt` - See Properties above.

`ProjectId` - The ID of the project the application credential was created.

## See Also

* [openstack_identity_application_credential_v3](https://www.terraform.io/docs/providers/openstack/r/identity_application_credential_v3.html) in the _Terraform Provider Documentation_