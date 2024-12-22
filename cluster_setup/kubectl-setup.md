# command to download binary

```bash
curl -LO "https://dl.k8s.io/release/$(curl -L -s https://dl.k8s.io/release/stable.txt)/bin/linux/amd64/kubectl"

```

# command to download checksum file

```bash
curl -LO "https://dl.k8s.io/release/$(curl -L -s https://dl.k8s.io/release/stable.txt)/bin/linux/amd64/kubectl.sha256"
# valiadte checksum
echo "$(cat kubectl.sha256)  kubectl" | sha256sum --check

```

# install kubectl

```bash
sudo install -o root -g root -m 0755 kubectl /usr/local/bin/kubectl

#test kubectl version
kubectl version --client

```