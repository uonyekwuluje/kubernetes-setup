# Ansible Kubernetes Cluster & Containerd
Ansible Kubernbetes Stack Configs

## Install RKE
```
VERSION="v1.5.5"
sudo wget -O /usr/local/bin/rke https://github.com/rancher/rke/releases/download/${VERSION}/rke_linux-amd64
sudo chmod +x /usr/local/bin/rke
rke --version
```

## Test and Install
```
# Test Ping Cluster Nodes
ansible -m ping kubernetes_stack -v -o

# Create Cluster
make create
```

## Test Cluster
```
kubectl --kubeconfig kube_config_cluster.yml get nodes
kubectl --kubeconfig kube_config_cluster.yml get pods --all-namespaces
```
