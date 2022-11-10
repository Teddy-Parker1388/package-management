### PRE_REQUISITES
+ Install AWS CLI – Command line tools for working with AWS services, including Amazon EKS.

+ Install eksctl – A command line tool for working with EKS clusters that automates many individual tasks.

+ Install kubectl  – A command line tool for working with Kubernetes clusters. 



### INSTALL EKSCTL 

```
curl --silent --location "https://github.com/weaveworks/eksctl/releases/latest/download/eksctl_$(uname -s)_amd64.tar.gz" | tar xz -C /tmp

# Move the extracted binary to /usr/local/bin. 

sudo mv /tmp/eksctl /usr/local/bin

eksctl version`
```
