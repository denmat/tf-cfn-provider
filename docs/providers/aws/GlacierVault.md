# Terraform::AWS::GlacierVault

Provides a Glacier Vault Resource. You can refer to the [Glacier Developer Guide](https://docs.aws.amazon.com/amazonglacier/latest/dev/working-with-vaults.html) for a full explanation of the Glacier Vault functionality

~> **NOTE:** When removing a Glacier Vault, the Vault must be empty.

## Return Values

### Fn::GetAtt

Fn::GetAtt returns a value for a specified attribute of this type. The following are the available attributes and sample return values.

`Location` - The URI of the vault that was created.

`Arn` - The ARN of the vault.

## See Also

* [aws_glacier_vault](https://www.terraform.io/docs/providers/aws/r/glacier_vault.html) in the _Terraform Provider Documentation_