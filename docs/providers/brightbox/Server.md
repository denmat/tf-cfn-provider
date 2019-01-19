# Terraform::Brightbox::Server

Provides a Brightbox Server resource. This can be used to create,
modify, and delete Servers. Servers also support
[provisioning](/docs/provisioners/index.html).

## Return Values

### Fn::GetAtt

Fn::GetAtt returns a value for a specified attribute of this type. The following are the available attributes and sample return values.

`Id` - The ID of the Server.

`Fqdn` - Fully Qualified Domain Name of server.

`Hostname` - short name of server, usually the same as the `id`.

`Interface` - the id reference of the network interface. Used to target cloudips.

`Ipv4AddressPrivate` - The RFC 1912 address of the server.

`Ipv6Address` - the IPv6 address of the server.

`Ipv6Hostname` - the FQDN of the IPv6 address.

`PublicHostname` - the FQDN of the public IPv4 address. Appears if a cloud ip is mapped.

`Ipv4Address` - the public IPV4 address of the server. Appears if a cloud ip is mapped.

`Locked` - True if server has been set to locked and cannot be deleted.

`Status` - Current state of the server, usually `active`, `inactive`.

`Username` - The username used to log onto the server.

## See Also

* [brightbox_server](https://www.terraform.io/docs/providers/brightbox/r/server.html) in the _Terraform Provider Documentation_