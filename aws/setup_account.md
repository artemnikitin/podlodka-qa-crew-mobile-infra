# AWS account setup

### Pre-requisites
- Valid AWS account (every new account got some resources for free https://aws.amazon.com/free, but it will not be enough for this demo)
- Go to https://console.aws.amazon.com/iam/home and create a new user 
- Set access rights for this user. At minimum they should be equal to needed for [EC2 Jenkins plugin](https://plugins.jenkins.io/ec2/)
- Go to [https://console.aws.amazon.com/vpc/home#vpcs:](fhttps://console.aws.amazon.com/vpc/home#vpcs:) and create a new VPC. Check https://docs.aws.amazon.com/vpc/latest/userguide/VPC_Scenarios.html for examples 
- Go to [https://console.aws.amazon.com/ec2/v2/home#KeyPairs:](https://console.aws.amazon.com/ec2/v2/home#KeyPairs:) and create a new SSH key. Keep it safely!
- Go to [https://console.aws.amazon.com/ec2/v2/home#SecurityGroups:](https://console.aws.amazon.com/ec2/v2/home#SecurityGroups:) and create a new security group

Everything created during setup will be needed to configure Jenkins to create new instances in AWS.

### Creating base AMI
We will use [Packer](https://www.packer.io/) for that. 
- Install Packer according to https://learn.hashicorp.com/tutorials/packer/getting-started-install
- Run it to verify our `ami-base-.json` using command `packer validate ami_base.json`
- Create an AMI using command (for that you will need AWS credentials created previously)
```shell
packer build \
  -var 'aws_access_key=<key>' \
  -var 'aws_secret_key=<secret>' \
  ami_base.json
```


