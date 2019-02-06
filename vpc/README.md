aws cloudformation create-stack --stack-name single-az-vpc --template-body file://./single-az-vpc.yml --parameters ParameterKey=EnvironmentName,ParameterValue=dev
