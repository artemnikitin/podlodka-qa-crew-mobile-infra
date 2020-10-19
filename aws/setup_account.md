# AWS account setup

### Pre-requisites
- Valid AWS account (every new account got some resources for free https://aws.amazon.com/free, but it will not be enough for this demo)
- Go to https://console.aws.amazon.com/iam/home and create a new user 
- Set access rights for this user. At minimum they should be equal to needed for [EC2 Jenkins plugin](https://plugins.jenkins.io/ec2/)
- Go to [https://console.aws.amazon.com/vpc/home#vpcs:](fhttps://console.aws.amazon.com/vpc/home#vpcs:) and create a new VPC. Check https://docs.aws.amazon.com/vpc/latest/userguide/VPC_Scenarios.html for examples 
- Go to [https://console.aws.amazon.com/ec2/v2/home#KeyPairs:](https://console.aws.amazon.com/ec2/v2/home#KeyPairs:) and create a new SSH key. Keep it safely!
