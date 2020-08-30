# Lab setup
## Installing Minikube
If you are using a VM you **must enable the virtualization option** first.
```bash
# Install kubectl
sudo apt install curl -y
curl -LO "https://storage.googleapis.com/kubernetes-release/release/$(curl -s https://storage.googleapis.com/kubernetes-release/release/stable.txt)/bin/linux/amd64/kubectl"
chmod +x ./kubectl
sudo mv ./kubectl /usr/local/bin/kubectl
# Update the PATH variable
source ~/.bashrc
# Ensure that kubectl is installed 
kubectl version --client
# Install virtualbox as the viertualization platform
sudo apt install virtualbox -y
# Install minkube through direct download
sudo mkdir -p /usr/local/bin/
sudo install minikube /usr/local/bin/
# Start minikube
minikube start
# Ensure that kubectl is correctly configured
kuebctl get nodes
```
