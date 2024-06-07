### Step 1: Install Docker
``` shell
sudo apt-get update
sudo apt install docker.io
docker ps
sudo chown $USER /var/run/docker.sock
```

### Step 2: Install kubectl
``` shell
curl -o kubectl https://amazon-eks.s3.us-west-2.amazonaws.com/1.19.6/2021-01-05/bin/linux/amd64/kubectl
chmod +x ./kubectl
sudo mv ./kubectl /usr/local/bin
kubectl version --short --client
```

### Install MicroK8s on Linux

``` sudo snap install microk8s --classic
microk8s status --wait-ready
sudo usermod -a -G microk8s ubuntu
newgrp microk8s
```

### Create .kube dir
```
cd $HOME
mkdir .kube
cd .kube
microk8s config > config
```
### Helm installation
```
sudo apt update
sudo apt upgrade -y
sudo apt install curl -y
curl https://baltocdn.com/helm/signing.asc | sudo apt-key add -
sudo apt-get install apt-transport-https --yes
echo "deb https://baltocdn.com/helm/stable/debian/ all main" | sudo tee /etc/apt/sources.list.d/helm-stable-debian.list
sudo apt update
sudo apt install helm -y
helm version
```

