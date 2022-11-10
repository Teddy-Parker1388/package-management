### PRE_REQUISITES
+ Install AWS CLI – Command line tools for working with AWS services, including Amazon EKS.

+ Install eksctl – A command line tool for working with EKS clusters that automates many individual tasks.

+ Install kubectl  – A command line tool for working with Kubernetes clusters. 



### INSTALL EKSCTL 

```
curl --silent --location "https://github.com/weaveworks/eksctl/releases/latest/download/eksctl_$(uname -s)_amd64.tar.gz" | tar xz -C /tmp

# Move the extracted binary to /usr/local/bin. 

sudo mv /tmp/eksctl /usr/local/bin

eksctl version
```

### INSTALL KUBECTL
```
sudo curl --silent --location -o /usr/local/bin/kubectl   https://s3.us-west-2.amazonaws.com/amazon-eks/1.22.6/2022-03-09/bin/linux/amd64/kubectl


sudo chmod +x /usr/local/bin/kubectl 

#Verify if kubectl got installed

kubectl version --short --client
```
### ATTACH ADMINISTRATOR ACCESS IAM ROLE TO EC2 INSTANCE
+ Create Admin Access IAM Role in AWS Console
+ Attach to EC2 Instance

### CREATE K8 CLUSTER
```
eksctl create cluster --name demo-eks --region us-east-2 --nodegroup-name my-nodes --node-type t3.small --managed --nodes 2 

eksctl get cluster --name demo-eks --region us-east-2 
#This should confirm that EKS cluster is up and running.

aws eks update-kubeconfig --name demo-eks --region us-east-2
```
