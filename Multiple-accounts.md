# How to use AWS CLI with multiple accounts

As explained in the [official documentation](https://docs.aws.amazon.com/cli/latest/userguide/cli-multiple-profiles.html), the credential file at `~/.aws/credentials` can contain more than one credentials.

```console
~/Desktop/AWS
(AWS) ❯ cat ~/.aws/credentials
[default]
aws_access_key_id = {Some ID Value}
aws_secret_access_key = {Some Key Value}

[Alice]
aws_access_key_id = {Some ID Value}
aws_secret_access_key = {Some Key Value}

[Bob]
aws_access_key_id = {Some ID Value}
aws_secret_access_key = {Some Key Value}
```

You can invoke the `aws` command with profiles other than the default user as long as you provide all the information.

```console
~/Desktop/AWS
(AWS) ❯ aws cloudformation list-stacks --profile=Alice --region=eu-west-1 --output=json
```
