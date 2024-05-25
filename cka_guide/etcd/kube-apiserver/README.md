Installation of Kube-apiserver
wget https://storage.googleapis.com/kubernetes-release/release/v1.13.0/bin/linux/amd64/kube-apiserver

To view the kube-system pods
kubectl get pods -n kube-system