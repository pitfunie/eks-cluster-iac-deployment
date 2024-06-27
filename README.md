#Building a shopping cart application

#Ploygolt
#Microservices
#Serialization


#CloudShell is a standalone, general-purpose tool that you can use to run commands on AWS to deploy CloudFormation Template to build a stack physical EKS Cluster
#AWS Cloud9 is an integrated development environment (IDE) that gives users access to a terminal when using a Cloud9 environment that requires an EC2 instance in #an AWS account. 

#The provision of the EKS Cluster and Cleanup section provides a guide to preventing further charges.

#Wycliffe outlines how to set up the environment to run in your AWS account. These instructions have been tested in the following AWS regions and are not #guaranteed to work in others without modification:

#us-west-2
#eu-west-1

#Open CloudShell with the link below or follow this documentation:

#https://console.aws.amazon.com/cloudshell/home
#![image](https://github.com/pitfunie/eks-cluster-iac-deployment/assets/32913487/51ecc3a4-9e46-4d71-8328-8bf54dcb6eb4)

#Once Cloudshell is running follow these commands for CloudFormation Template to create a stack:


#wget -q https://raw.githubusercontent.com/pitfunie/eks-cluster-iac-deployment/main/eks-wycliffe-ide-cfn.yaml -O eks-wycliffe-ide-cfn.yaml
#aws cloudformation deploy --stack-name eks-wycliffe-ide \
#    --template-file ./eks-wycliffe-ide-cfn.yaml \
#    --parameter-overrides RepositoryRef=stable \
#    --capabilities CAPABILITY_NAMED_IAM


#Once the CloudFormation is completed you can retrieve the URL for the Cloud9 IDE like so:

#aws cloudformation describe-stacks --stack-name eks-wycliffe-ide \
#    --query 'Stacks[0].Outputs[?OutputKey==`Cloud9Url`].OutputValue' --output text

#Now open this URL in a web browser to access the IDE.
#aws sts get-caller-identity

#AWS EKS Kubernetes eksctl utility has been pre-installed in your Amazon Cloud9 Environment, so we can immediately create the cluster. 
#So I attached an eksctl file that can be used to create a Cluster


#I Recommended Terraform and attached the tf files that will create the Cluster



