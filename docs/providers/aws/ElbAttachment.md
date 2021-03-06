# Terraform::AWS::ElbAttachment

Attaches an EC2 instance to an Elastic Load Balancer (ELB). For attaching resources with Application Load Balancer (ALB) or Network Load Balancer (NLB), see the [`Terraform::AWS::LbTargetGroupAttachment` resource](/docs/providers/aws/r/lb_target_group_attachment.html).

~> **NOTE on ELB Instances and ELB Attachments:** Terraform currently provides
both a standalone ELB Attachment resource (describing an instance attached to
an ELB), and an [Elastic Load Balancer resource](elb.html) with
`instances` defined in-line. At this time you cannot use an ELB with in-line
instances in conjunction with an ELB Attachment resource. Doing so will cause a
conflict and will overwrite attachments.

## Properties

`Elb` - (Required) The name of the ELB.

`Instance` - (Required) Instance ID to place in the ELB pool.


## See Also

* [aws_elb_attachment](https://www.terraform.io/docs/providers/aws/r/elb_attachment.html) in the _Terraform Provider Documentation_