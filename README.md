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
### Open it in a code editor like VS Code using <br>
[dev] <br>
aws_access_key_id = XXXXXXXXXXX <br>
aws_secret_access_key = YYYYYYYYYYY

```
code ~/.aws/credentials
```
[profile dev] <br>
region = ap-south-1

```
code ~/.aws/config
```
### Test the profile directly
```
aws sts get-caller-identity --profile dev

```
### Get InstanceId + Name Tag + Public IP + State
```
aws ec2 describe-instances \
  --query "Reservations[*].Instances[*].[InstanceId,Tags[?Key=='Name'].Value|[0],State.Name,PublicIpAddress]" \
  --output table --profile dev
```
