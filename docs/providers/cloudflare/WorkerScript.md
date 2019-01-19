# Terraform::Cloudflare::WorkerScript

Provides a Cloudflare worker script resource. In order for a script to be active, you'll also need to setup a `cloudflare_worker_route`.

## Return Values

### Fn::GetAtt

Fn::GetAtt returns a value for a specified attribute of this type. The following are the available attributes and sample return values.

`ZoneId` - The zone id of the script (only for non-multi-script resources).

## See Also

* [cloudflare_worker_script](https://www.terraform.io/docs/providers/cloudflare/r/worker_script.html) in the _Terraform Provider Documentation_