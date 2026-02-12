# Kubernetes

wsl -l -v
![finding-images](image.png)

wsl -d ubuntu
![moving-to-ubuntu](image-1.png)


# installing Kubernetes in windows system post logging into wsl -d ubuntu:

'''
sudo apt update
'''
'''
sudo apt install -y apt-transport-https ca-certificates curl
'''
'''
curl -fsSL https://pkgs.k8s.io/core:/stable:/v1.30/deb/Release.key | \
sudo gpg --dearmor -o /etc/apt/keyrings/kubernetes-apt-keyring.gpg
'''
'''
echo 'deb [signed-by=/etc/apt/keyrings/kubernetes-apt-keyring.gpg] https://pkgs.k8s.io/core:/stable:/v1.30/deb/ /' | \
sudo tee /etc/apt/sources.list.d/kubernetes.list
'''
'''
sudo apt update
'''
'''
sudo apt install -y kubectl
'''
'''
kubectl version --client
'''
'''
kubectl completion bash >> ~/.bashrc
'''
'''
source ~/.bashrc
'''
