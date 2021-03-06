# Terraform::AWS::MacieMemberAccountAssociation

Associates an AWS account with Amazon Macie as a member account.

~> **NOTE:** Before using Amazon Macie for the first time it must be enabled manually. Instructions are [here](https://docs.aws.amazon.com/macie/latest/userguide/macie-setting-up.html#macie-setting-up-enable).

## Properties

`MemberAccountId` - (Required) The ID of the AWS account that you want to associate with Amazon Macie as a member account.


## Return Values

### Fn::GetAtt

`Id` - The ID of the association.

## See Also

* [aws_macie_member_account_association](https://www.terraform.io/docs/providers/aws/r/macie_member_account_association.html) in the _Terraform Provider Documentation_