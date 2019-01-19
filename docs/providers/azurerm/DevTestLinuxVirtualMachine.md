# Terraform::AzureRM::DevTestLinuxVirtualMachine

Manages a Linux Virtual Machine within a Dev Test Lab.

## Return Values

### Fn::GetAtt

Fn::GetAtt returns a value for a specified attribute of this type. The following are the available attributes and sample return values.

`Id` - The ID of the Virtual Machine.

`Fqdn` - The FQDN of the Virtual Machine.

`InboundNatRule` - One or more `inbound_nat_rule` blocks as defined below.

`UniqueIdentifier` - The unique immutable identifier of the Virtual Machine.

`FrontendPort` - The frontend port associated with this Inbound NAT Rule.

## See Also

* [azurerm_dev_test_linux_virtual_machine](https://www.terraform.io/docs/providers/azurerm/r/dev_test_linux_virtual_machine.html) in the _Terraform Provider Documentation_