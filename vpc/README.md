### Cloudformation snippets to create simple infra
* 1x AZ, 1x VPC, 1x IGW, 1x NGW, 1x public and private subnets
* 2x AZ, 1x VPC, 1x IGW, 2x NGW, 2x public and private subnets
* 2x AZ, 1x VPC, 1x IGW, 2x NGW, 1x EC2, 1x ELB, 2x public and private subnets

### Command-line
```
aws cloudformation create-stack --stack-name one-az-vpc --template-body file://./one-az-vpc.yml --parameters ParameterKey=EnvironmentName,ParameterValue=dev

aws cloudformation create-stack --stack-name two-az-vpc --template-body file://./two-az-vpc.yml --parameters ParameterKey=EnvironmentName,ParameterValue=dev

aws cloudformation create-stack --stack-name two-az-ec2 --template-body file://./two-az-ec2.yml --parameters ParameterKey=EnvironmentName,ParameterValue=dev
```