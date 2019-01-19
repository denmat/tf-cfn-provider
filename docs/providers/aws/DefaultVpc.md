# Terraform::AWS::DefaultVpc

Provides a resource to manage the [default AWS VPC](http://docs.aws.amazon.com/AmazonVPC/latest/UserGuide/default-vpc.html)
in the current region.

For AWS accounts created after 2013-12-04, each region comes with a Default VPC.
**This is an advanced resource**, and has special caveats to be aware of when
using it. Please read this document in its entirety before using this resource.

The `aws_default_vpc` behaves differently from normal resources, in that
Terraform does not _create_ this resource, but instead "adopts" it
into management.

## Return Values

### Fn::GetAtt

Fn::GetAtt returns a value for a specified attribute of this type. The following are the available attributes and sample return values.

`Arn` - Amazon Resource Name (ARN) of VPC.

`Id` - The ID of the VPC.

`CidrBlock` - The CIDR block of the VPC.

`InstanceTenancy` - Tenancy of instances spin up within VPC.

`EnableDnsSupport` - Whether or not the VPC has DNS support.

`EnableDnsHostnames` - Whether or not the VPC has DNS hostname support.

`EnableClassiclink` - Whether or not the VPC has Classiclink enabled.

`AssignGeneratedIpv6CidrBlock` - Whether or not an Amazon-provided IPv6 CIDR.

`MainRouteTableId` - The ID of the main route table associated with.

`DefaultNetworkAclId` - The ID of the network ACL created by default on VPC creation.

`DefaultSecurityGroupId` - The ID of the security group created by default on VPC creation.

`DefaultRouteTableId` - The ID of the route table created by default on VPC creation.

`Ipv6AssociationId` - The association ID for the IPv6 CIDR block of the VPC.

`Ipv6CidrBlock` - The IPv6 CIDR block of the VPC.

`OwnerId` - The ID of the AWS account that owns the VPC.

## See Also

* [aws_default_vpc](https://www.terraform.io/docs/providers/aws/r/default_vpc.html) in the _Terraform Provider Documentation_