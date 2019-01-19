# Terraform::Brightbox::LoadBalancer

Provides a Brightbox Load Balancer resource. This can be used to create,
modify, and delete Load Balancers.

## Return Values

### Fn::GetAtt

Fn::GetAtt returns a value for a specified attribute of this type. The following are the available attributes and sample return values.

`Id` - The ID of the Load Balancer.

`Status` - Current state of the load balancer. Usually `creating` or `active`.

`Locked` - True if the database server has been set to locked and cannot be deleted.

## See Also

* [brightbox_load_balancer](https://www.terraform.io/docs/providers/brightbox/r/load_balancer.html) in the _Terraform Provider Documentation_