# circleci-crossplane-demo
Simple Crossplane.io deployment using CircleCI.


## Prerequisites
For this demo, I simply followed the [setup instructions on the crossplane.io site](https://crossplane.io/docs/v1.10/getting-started/install-configure.html).  This project's prerequisites are:

1. Crossplane installed and running on your cluster 
2. Crossplane AWS provider configured
3. AWS credentials file stored in k8s secret `aws-creds` in the Crossplane namespace

