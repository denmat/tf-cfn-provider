# Terraform::AWS::WafregionalXssMatchSet

Provides a WAF Regional XSS Match Set Resource for use with Application Load Balancer.

## Properties

`Name` - (Required) The name of the set.

`XssMatchTuple` - (Optional) The parts of web requests that you want to inspect for cross-site scripting attacks.


## Return Values

### Fn::GetAtt

`Id` - The ID of the Regional WAF XSS Match Set.

## See Also

* [aws_wafregional_xss_match_set](https://www.terraform.io/docs/providers/aws/r/wafregional_xss_match_set.html) in the _Terraform Provider Documentation_