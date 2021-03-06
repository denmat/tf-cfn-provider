# Triton Provider

## Configuration

To configure this resource, you must create an AWS Secrets Manager secret with the name **terraform/triton** or add [template metadata](https://github.com/iann0036/tf-cfn-provider/blob/master/examples/metadata.yaml). The below arguments may be included as the key/value or JSON properties in the secret or metadata object:

* `account` - (Required) This is the name of the Triton account.
* `user` - (Optional) This is the username to interact with the triton API.
* `key_material` - (Optional) This is the private key of an SSH key associated
with the Triton account to be used. If this is not set, the private key corresponding
to the fingerprint in `key_id` must be available via an SSH Agent.
* `key_id` - (Required) This is the fingerprint of the public key matching the key
specified in `key_path`. It can be obtained via the command `ssh-keygen -l -E md5 -f /path/to/key`.
* `url` - (Optional) This is the URL to the Triton API endpoint. It is required
if using a private installation of Triton. The default is to use the Joyent public
cloud us-west-1 endpoint. Valid public cloud endpoints include: `us-east-1`, `us-east-2`,
`us-east-3`, `us-sw-1`, `us-west-1`, `eu-ams-1`.
* `insecure_skip_tls_verify` (Optional - defaults to false) This allows skipping
TLS verification of the Triton endpoint. It is useful when connecting to a temporary
Triton installation such as Cloud-On-A-Laptop which does not generally use a certificate
signed by a trusted root CA.


## Supported Resources

* [Terraform::Triton::Fabric](Fabric.md)
* [Terraform::Triton::FirewallRule](FirewallRule.md)
* [Terraform::Triton::InstanceTemplate](InstanceTemplate.md)
* [Terraform::Triton::Key](Key.md)
* [Terraform::Triton::Machine](Machine.md)
* [Terraform::Triton::ServiceGroup](ServiceGroup.md)
* [Terraform::Triton::Snapshot](Snapshot.md)
* [Terraform::Triton::Vlan](Vlan.md)