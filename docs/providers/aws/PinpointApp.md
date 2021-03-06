# Terraform::AWS::PinpointApp

Provides a Pinpoint App resource.

## Properties

`Name` - (Optional) The application name. By default generated by Terraform.

`NamePrefix` - (Optional) The name of the Pinpoint application. Conflicts with `Name`.

`CampaignHook` - (Optional) The default campaign limits for the app. These limits apply to each campaign for the app, unless the campaign overrides the default with limits of its own.

`Limits` - (Optional) The default campaign limits for the app. These limits apply to each campaign for the app, unless the campaign overrides the default with limits of its own.

`QuietTime` - (Optional) The default quiet time for the app. Each campaign for this app sends no messages during this time unless the campaign overrides the default with a quiet time of its own.

### CampaignHook Properties

`LambdaFunctionName` - (Optional) Lambda function name or ARN to be called for delivery. Conflicts with `WebUrl`.

`Mode` - (Required if `LambdaFunctionName` or `WebUrl` are provided) What mode Lambda should be invoked in. Valid values for this parameter are `DELIVERY`, `FILTER`.

`WebUrl` - (Optional) Web URL to call for hook. If the URL has authentication specified it will be added as authentication to the request. Conflicts with `LambdaFunctionName`.

### Limits Properties

`Daily` - (Optional) The maximum number of messages that the campaign can send daily.

`MaximumDuration` - (Optional) The length of time (in seconds) that the campaign can run before it ends and message deliveries stop. This duration begins at the scheduled start time for the campaign. The minimum value is 60.

`MessagesPerSecond` - (Optional) The number of messages that the campaign can send per second. The minimum value is 50, and the maximum is 20000.

`Total` - (Optional) The maximum total number of messages that the campaign can send.

### QuietTime Properties

`End` - (Optional) The default end time for quiet time in ISO 8601 format. Required if `Start` is set.

`Start` - (Optional) The default start time for quiet time in ISO 8601 format. Required if `End` is set.


## Return Values

### Fn::GetAtt

`ApplicationId` - The Application ID of the Pinpoint App.

## See Also

* [aws_pinpoint_app](https://www.terraform.io/docs/providers/aws/r/pinpoint_app.html) in the _Terraform Provider Documentation_