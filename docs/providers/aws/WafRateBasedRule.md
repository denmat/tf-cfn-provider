# Terraform::AWS::WafRateBasedRule

Provides a WAF Rate Based Rule Resource

## Properties

`MetricName` - (Required) The name or description for the Amazon CloudWatch metric of this rule.

`Name` - (Required) The name or description of the rule.

`RateKey` - (Required) Valid value is IP.

`RateLimit` - (Required) The maximum number of requests, which have an identical value in the field specified by the RateKey, allowed in a five-minute period. Minimum value is 2000.

`Predicates` - (Optional) One of ByteMatchSet, IPSet, SizeConstraintSet, SqlInjectionMatchSet, or XssMatchSet objects to include in a rule.


## Return Values

### Fn::GetAtt

`Id` - The ID of the WAF rule.

## See Also

* [aws_waf_rate_based_rule](https://www.terraform.io/docs/providers/aws/r/waf_rate_based_rule.html) in the _Terraform Provider Documentation_