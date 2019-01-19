# Terraform::Alicloud::NetworkInterface

Provides an ECS Elastic Network Interface resource.

For information about Elastic Network Interface and how to use it, see [Elastic Network Interface](https://www.alibabacloud.com/help/doc-detail/58496.html).

~> **NOTE** Only one of private_ips or private_ips_count can be specified when assign private IPs.

## Return Values

### Fn::GetAtt

Fn::GetAtt returns a value for a specified attribute of this type. The following are the available attributes and sample return values.

`Id` - The ENI ID.

## See Also

* [alicloud_network_interface](https://www.terraform.io/docs/providers/alicloud/r/network_interface.html) in the _Terraform Provider Documentation_