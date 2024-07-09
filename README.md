# deploy-to-eks-using-github-actions
1. Create an EKS Cluster using this command:

run command choco install eksctl in vs code terminal

eksctl create cluster --name salvadorapp --region us-east-1 --nodegroup-name linux-nodes --node-type t2.micro --nodes 2

2. Then create .github folder and then create workflow folder inside .github folder 
3. Create file with .yml extension and write the workflow code
4. Create a github repository 
5. Create secrets in github repo
        Go to settings of repo
        click on secrets and variables
6. Test application by getting the dns name and going to a web browser

Clean up: Run: eksctl delete cluster --name salvadorapp
