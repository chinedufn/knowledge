# AWS

## Running CLI as another user

When assigning permissions to a group or user it can be useful to run commands as a user in order to verify that they have access
to things that they should have access to.

Say we want to run commands as a user named `circle-ci, in order to verify that the commands that we plan to add to our CI config will
work properly.

```sh
# Skip this step if you already have an access key and secret
aws iam create-access-key --user-name circle-ci
```

```
# ~/.aws/config

[default]
region = XXXX

[profile circle-ci]
region = XXXX
```

```
# ~/.aws/credentials

[default]
aws_access_key_id = XXXX
aws_secret_access_key = XXXX

[akigi-circle-ci]
aws_access_key_id = XXXX
aws_secret_access_key = XXXX
```

```sh
# Attempting to run a command as this user
aws ec2 describe-instances --profile circle-ci
```
