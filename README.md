# aws-eks-demo
A repository to test k8s in AWS

The steps to set up a k8s cluster and monitoring with EFK stack.

# Install
Follow the article in install-eks.txt file

# EFK Stack
`kubectl appy -f storage-aws.yaml`

`kubectl appy -f fluentd-config.yaml`

`kubectl appy -f elastic-stack.yaml`