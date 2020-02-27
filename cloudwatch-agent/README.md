## cloudwatch-agent

A chart to deploy the AWS Cloudwatch agent and related flunetd image to enable data feeds for ContainerInsights and CloudWatch logs. 

The Pod Role will need the follow AWS managed Policy: `arn:aws:iam::aws:policy/CloudWatchAgentServerPolicy`

