## cloudwatch-agent

A chart to deploy the AWS Cloudwatch agent and related flunetd image to enable data feeds for ContainerInsights and CloudWatch logs. 

### IAM Role

Below is an example Terrafomr policy doc for the required IAM Role:

```
data "aws_iam_policy_document" "cloudwatch_policy_doc" {
  statement {
    sid = 1

    effect = "Allow"
    actions = [
      "cloudwatch:PutMetricData",
      "logs:PutDestination",
      "logs:PutLogEvents"
    ]
    resources = ["*"]
  }
}
```