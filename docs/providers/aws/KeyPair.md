# Terraform::AWS::KeyPair

Provides an [EC2 key pair](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ec2-key-pairs.html) resource. A key pair is used to control login access to EC2 instances.

Currently this resource requires an existing user-supplied key pair. This key pair's public key will be registered with AWS to allow logging-in to EC2 instances.

When importing an existing key pair the public key material may be in any format supported by AWS. Supported formats (per the [AWS documentation](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ec2-key-pairs.html#how-to-generate-your-own-key-and-import-it-to-aws)) are:

* OpenSSH public key format (the format in ~/.ssh/authorized_keys)
* Base64 encoded DER format
* SSH public key file format as specified in RFC4716

## Properties

`KeyName` - (Optional) The name for the key pair.

`KeyNamePrefix` - (Optional) Creates a unique name beginning with the specified prefix. Conflicts with `KeyName`.

`PublicKey` - (Required) The public key material.


## Return Values

### Fn::GetAtt

`KeyName` - The key pair name.

`Fingerprint` - The MD5 public key fingerprint as specified in section 4 of RFC 4716.

## See Also

* [aws_key_pair](https://www.terraform.io/docs/providers/aws/r/key_pair.html) in the _Terraform Provider Documentation_