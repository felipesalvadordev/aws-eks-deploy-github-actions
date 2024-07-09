# deploy-to-eks-using-github-actions
run command choco install eksctl in vs code terminal

1. Create an EKS Cluster and configrue eks using this commands:

eksctl create cluster --name salvadorapp --region us-east-1 --nodegroup-name linux-nodes --node-type t2.micro --nodes 2  
aws eks --region us-east-1 update-kubeconfig --name salvadorcluster

2. Then create .github folder and then create workflow folder inside .github folder 
3. Create file with .yml extension and write the workflow code
4. Create a github repository 
5. Create secrets in github repo
        Go to settings of repo
        click on secrets and variables
6. Test application by getting the dns name and going to a web browser

Clean up: Run: eksctl delete cluster --name salvadorapp
