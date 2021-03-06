# Terraform::AzureStack::VirtualNetworkGatewayConnection

Manages a connection in an existing Virtual Network Gateway.

## Properties

`Name` - (Required) The name of the connection. Changing the name forces a
new resource to be created.

`ResourceGroupName` - (Required) The name of the resource group in which to
create the connection Changing the name forces a new resource to be created.

`Location` - (Required) The location/region where the connection is
located. Changing this forces a new resource to be created.

`Type` - (Required) The type of connection. Valid options are `IPsec`
(Site-to-Site), `ExpressRoute` (ExpressRoute), and `Vnet2Vnet` (VNet-to-VNet).
Each connection type requires different mandatory arguments (refer to the
examples above). Changing the connection type will force a new connection
to be created.

`VirtualNetworkGatewayId` - (Required) The ID of the Virtual Network Gateway
in which the connection will be created. Changing the gateway forces a new
resource to be created.

`AuthorizationKey` - (Optional) The authorization key associated with the
Express Route Circuit. This field is required only if the type is an
ExpressRoute connection.

`ExpressRouteCircuitId` - (Optional) The ID of the Express Route Circuit
when creating an ExpressRoute connection (i.e. when `Type` is `ExpressRoute`).
The Express Route Circuit can be in the same or in a different subscription.

`PeerVirtualNetworkGatewayId` - (Optional) The ID of the peer virtual
network gateway when creating a VNet-to-VNet connection (i.e. when `Type`
is `Vnet2Vnet`). The peer Virtual Network Gateway can be in the same or
in a different subscription.

`LocalNetworkGatewayId` - (Optional) The ID of the local network gateway
when creating Site-to-Site connection (i.e. when `Type` is `IPsec`).

`RoutingWeight` - (Optional) The routing weight. Defaults to `10`.

`SharedKey` - (Optional) The shared IPSec key. A key must be provided if a
Site-to-Site or VNet-to-VNet connection is created whereas ExpressRoute
connections do not need a shared key.

`EnableBgp` - (Optional) If `true`, BGP (Border Gateway Protocol) is enabled
for this connection. Defaults to `false`.

`Tags` - (Optional) A mapping of tags to assign to the resource.


## Return Values

### Fn::GetAtt

`Id` - The connection ID.

## See Also

* [azurestack_virtual_network_gateway_connection](https://www.terraform.io/docs/providers/azurestack/r/virtual_network_gateway_connection.html) in the _Terraform Provider Documentation_