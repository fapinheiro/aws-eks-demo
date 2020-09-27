# aws-eks-demo
A repository to test k8s in AWS

The steps to set up a k8s cluster and monitoring with EFK stack.

# Install
Follow the article in install-eks.txt file to set up a EC2 with kubectl, eks-cli, and AWS permitions for a k8s cluster.

# List Cluster
`aws eks list-cluster`

# Create Cluster
`eksctl create cluster --name cib-cross-services-k8s --nodes-min=2`

# Delete Cluster
`eksctl delete cluster cib-cross-services-k8s`

# Start EFK Stack
`kubectl apply -f storage-aws.yaml`

`kubectl apply -f fluentd-config.yaml`

`kubectl apply -f elastic-stack.yaml`

# Kibana Endpoint
`kubectl get svc -n kube-system`