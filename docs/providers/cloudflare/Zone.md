# Terraform::Cloudflare::Zone

Provides a Cloudflare Zone resource. Zone is the basic resource for working with Cloudflare and is roughly equivalent to a domain name that the user purchases.

## Properties

`Zone` - (Required) The DNS zone name which will be added.

`Paused` - (Optional) Boolean of whether this zone is paused (traffic bypasses Cloudflare). Default: false.

`JumpStart` - (Optional) Boolean of whether to scan for DNS records on creation. Ignored after zone is created. Default: false.

`Plan` - (Optional) The name of the commercial plan to apply to the zone, can be updated once the one is created; one of `free`, `pro`, `business`, `enterprise`.


## Return Values

### Fn::GetAtt

`Id` - The zone ID.

`Plan` - The name of the commercial plan to apply to the zone.

`VanityNameServers` - List of Vanity Nameservers (if set).

`Meta.wildcardProxiable` - Indicates whether wildcard DNS records can receive Cloudflare security and performance features.

`Meta.phishingDetected` - Indicates if URLs on the zone have been identified as hosting phishing content.

`Status` - Status of the zone. Valid values: `active`, `pending`, `initializing`, `moved`, `deleted`, `deactivated`.

`Type` - A full zone implies that DNS is hosted with Cloudflare. A partial zone is typically a partner-hosted zone or a CNAME setup. Valid values: `full`, `partial`.

`NameServers` - Cloudflare-assigned name servers. This is only populated for zones that use Cloudflare DNS.

## See Also

* [cloudflare_zone](https://www.terraform.io/docs/providers/cloudflare/r/zone.html) in the _Terraform Provider Documentation_