# deploy-to-aws-eks-using-github-actions

First, run command choco install eksctl in vs code terminal.  
eksctl is a simple CLI tool for creating clusters on EKS 

Step by step through the process of deploying applications to AWS EKS using GitHub actions CI/CD pipeline:

1. Create an EKS Cluster and configure eks region using this commands:

eksctl create cluster --name salvadorapp --region us-east-1 --nodegroup-name linux-nodes --node-type t2.micro --nodes 2  
aws eks --region us-east-1 update-kubeconfig --name salvadorcluster

2. Then create .github folder and then create workflow folder inside .github folder 
3. Create file with .yml extension and write the workflow code
4. Create a github repository 
5. Create secrets in github repo
        Go to settings of repo
        click on secrets and variables
6. Test application by getting the dns name and going to a web browser

Clean up: Run eksctl delete cluster --name salvadorcluster

Image running on EKS:  

![image](https://github.com/felipesalvadordev/deploy-node-js-eks-github-actions/assets/13543372/f62db948-f68d-46e5-82d6-a3f4a451c333)  

Reference: https://youtu.be/9qSmFWwsxwA?si=iYg88LdX2l3zHQcU




