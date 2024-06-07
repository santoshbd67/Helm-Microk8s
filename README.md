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
newgrp microk8s ```

### Create .kube dir


