# CloudFormation stacks

A collection of miscellaneous [CloudFormation] stacks.

## Getting started

### Requirements

- [AWS Command Line Interface] 2.8+

### Deploying stacks programmatically

```bash
aws cloudformation deploy \
  --capabilities "CAPABILITY_IAM" \
  --parameter-overrides "ParameterName=ParameterValue" \
  --tags "" \
  --template "one-of-the-files-in-this-repo.yaml" \
  --stack-name "your-naming-convention"
```

### Stacks

#### bootstrap-terraform

Creates the resources necessary to safely run Terraform. This includes an S3
bucket for persisting state and a DynamoDB table for ensuring stacks cannot be
updated simultaneously.

#### iam-role-cross-account-access

Creates an IAM role.

## License

© 2022 [Daniel Morris]\
Made available under the terms of the [Apache License 2.0].

[aws command line interface]: https://aws.amazon.com/cli/
[cloudformation]: https://aws.amazon.com/cloudformation/
[apache license 2.0]: LICENSE.md
[daniel morris]: https://unfun.co
