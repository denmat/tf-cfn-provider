# Terraform::CloudScale::FloatingIp

Provides a cloudscale.ch Floating IP to represent a publicly-accessible static IP address or IP network that can be assigned to one of your cloudscale.ch servers. Floating IPs can be moved between servers. Possible use cases include: High-availability, non-disruptive maintenance, multiple IPs per server, or re-using the same IP after replacing a server.

## Properties

`Server` - (Required) Assign the Floating IP to this server (UUID).

`IpVersion` - (Required) `4` or `6`, for an IPv4 or IPv6 address or network respectively.

`PrefixLength` - (Optional) If you want to assign an entire network instead of a single IP address to your server, you must specify the prefix length. Currently, there is only support for `ip_version=6` and `prefix_length=56`.

`ReversePtr` - (Optional) You can specify the PTR record (reverse DNS pointer) in case of a single Floating IP address.

`Server` - (Required) (Re-)Assign the Floating IP to this server (UUID).


## Return Values

### Fn::GetAtt

`Href` - The cloudscale.ch API URL of the current resource.

`Network` - The CIDR notation of the Floating IP address or network, e.g. `192.0.2.123/32`.

`NextHop` - The IP address of the server that your Floating IP is currently assigned to.

## See Also

* [cloudscale_floating_ip](https://www.terraform.io/docs/providers/cloudscale/r/floating_ip.html) in the _Terraform Provider Documentation_