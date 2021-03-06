# Terraform::DNSimple::Record

Provides a DNSimple record resource.

## Properties

`Domain` - (Required) The domain to add the record to.

`Name` - (Required) The name of the record.

`Value` - (Required) The value of the record.

`Type` - (Required) The type of the record.

`Ttl` - (Optional) The TTL of the record.

`Priority` - (Optional) The priority of the record - only useful for some record types.


## Return Values

### Fn::GetAtt

`Id` - The record ID.

`Name` - The name of the record.

`Value` - The value of the record.

`Type` - The type of the record.

`Ttl` - The TTL of the record.

`Priority` - The priority of the record.

`DomainId` - The domain ID of the record.

`Hostname` - The FQDN of the record.

## See Also

* [dnsimple_record](https://www.terraform.io/docs/providers/dnsimple/r/record.html) in the _Terraform Provider Documentation_