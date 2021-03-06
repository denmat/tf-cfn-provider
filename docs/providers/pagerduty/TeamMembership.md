# Terraform::PagerDuty::TeamMembership

A [team membership](https://v2.developer.pagerduty.com/v2/page/api-reference#!/Teams/put_teams_id_users_user_id) manages memberships within a team.

## Properties

`UserId` - (Required) The ID of the user to add to the team.
* `TeamId` - (Required) The ID of the team in which the user will belong.

`TeamId` - (Required) The ID of the team in which the user will belong.


## Return Values

### Fn::GetAtt

`UserId` - The ID of the user belonging to the team.

`TeamId` - The team ID the user belongs to.

## See Also

* [pagerduty_team_membership](https://www.terraform.io/docs/providers/pagerduty/r/team_membership.html) in the _Terraform Provider Documentation_