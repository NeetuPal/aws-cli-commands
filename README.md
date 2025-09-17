# aws-cli-commands

### Get the region of your current identity
```
aws configure list
```
### List available AWS profiles
```
aws configure list-profiles
```
### Show details of a specific profile
```
aws configure list --profile dev

```
### Open it in a code editor like VS Code
[dev]
aws_access_key_id = XXXXXXXXXXX
aws_secret_access_key = YYYYYYYYYYY

```
code ~/.aws/credentials
```
[profile dev]
region = ap-south-1

```
code ~/.aws/config
```
