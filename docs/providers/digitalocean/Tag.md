# Terraform::DigitalOcean::Tag

Provides a DigitalOcean Tag resource. A Tag is a label that can be applied to a
Droplet resource in order to better organize or facilitate the lookups and
actions on it. Tags created with this resource can be referenced in your Droplet
configuration via their ID or name.

## Properties

`Name` - (Required) The name of the tag.


## Return Values

### Fn::GetAtt

`Id` - The id of the tag.

`Name` - The name of the tag.

## See Also

* [digitalocean_tag](https://www.terraform.io/docs/providers/digitalocean/r/tag.html) in the _Terraform Provider Documentation_