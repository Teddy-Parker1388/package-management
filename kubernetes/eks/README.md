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
