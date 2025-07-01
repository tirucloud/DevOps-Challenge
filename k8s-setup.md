# ON MASTER

sudo hostnamectl set-hostname k8s-master
sudo hostnamectl set-hostname k8s-node-1

echo "[+] Updating /etc/hosts file with cluster node entries..."

cat <<EOF >> /etc/hosts

# Kubernetes Cluster Nodes
172.31.83.108   k8s-master
172.31.88.243   k8s-node-1
EOF


master.sh
================================================
#!/bin/bash

set -e

echo "[1/6] Disabling swap..."
swapoff -a
sed -i '/ swap / s/^/#/' /etc/fstab

echo "[2/6] Installing containerd..."
apt update -y
apt install -y containerd
mkdir -p /etc/containerd
containerd config default > /etc/containerd/config.toml
systemctl restart containerd
systemctl enable containerd

echo "[3/6] Adding Kubernetes repository..."
apt install -y apt-transport-https ca-certificates curl gpg
curl -fsSL https://pkgs.k8s.io/core:/stable:/v1.32/deb/Release.key | gpg --dearmor -o /etc/apt/keyrings/kubernetes-apt-keyring.gpg
echo "deb [signed-by=/etc/apt/keyrings/kubernetes-apt-keyring.gpg] https://pkgs.k8s.io/core:/stable:/v1.32/deb/ /" | tee /etc/apt/sources.list.d/kubernetes.list

echo "[4/6] Installing Kubernetes components..."
apt update -y
apt install -y kubelet kubeadm kubectl
apt-mark hold kubelet kubeadm kubectl

echo "[5/6] Initializing Kubernetes master node..."
kubeadm init --pod-network-cidr=172.31.0.0/16

echo "[6/6] Setting up kubeconfig for current user..."
mkdir -p $HOME/.kube
cp -i /etc/kubernetes/admin.conf $HOME/.kube/config
chown $(id -u):$(id -g) $HOME/.kube/config

echo "✅ Master setup completed. You can now apply a CNI plugin like Calico or Flannel."
=============================================================================================================




