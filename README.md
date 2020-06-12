# Packer Create Nginx Ubuntu AMI

## Requirements

- HashiCorp [Packer](https://www.packer.io/downloads/)
- [AWS Account](https://aws.amazon.com/console/)

## System Requirements

This can be executed on either a Windows or Linux system

## Execution Instructions

```bash
# Clone the respository
git clone git@github.com:nukdcbear/packer-nginx-ubuntu-ami.git

# cd in the directory
cd packer-nginx-ubuntu-ami

# Execute packer
packer build -var 'aws_access_key=XXXXXXXXXXX' -var 'aws_secret_key=XXXXXXXXXXXXXXXXXXXXXXXX' ubuntu-nginx.json
```

### Notes

The Pack json has a vpc_id and subnet_id defined but that is only required when Packer cannot determine the default VPC for t2.micro, see https://learn.hashicorp.com/packer/getting-started/build-image#known-issue.

Also the `ami_name` should be customized.
