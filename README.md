# circleci-crossplane-demo
Simple Crossplane.io deployment using CircleCI.  The pipeline does the following:

1. Clones this repo
2. Installs AWS CLI and kubectl
3. Authenticates with AWS EKS without storing credentials locally:
  a. Uses an OIDC token to authenticate with AWS
  b. Once authenticated, generates a kubeconfig file for the target EKS cluster
4. Applies a PostgreSQL AWS managed resource


## Prerequisites
For this demo, I simply followed the [setup instructions on the crossplane.io site](https://crossplane.io/docs/v1.10/getting-started/install-configure.html).  This project's prerequisites are:

1. Crossplane installed and running on your cluster 
2. Crossplane AWS provider configured
3. AWS credentials file stored in k8s secret `aws-creds` in the Crossplane namespace

