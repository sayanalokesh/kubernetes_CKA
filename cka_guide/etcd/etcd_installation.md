## Installation [guide](https://linuxconfig.org/how-to-install-etcd-on-ubuntu)

You can check the latest version in this [repository](https://github.com/etcd-io/etcd/releases/)

```
sudo apt-get update
sudo apt-get install etcd
sudo apt-get update
sudo apt-get install wget curl -y
wget https://github.com/etcd-io/etcd/releases/download/v3.5.6/etcd-v3.5.6-linux-amd64.tar.gz  # the latest version is 3.5.13 replace if you want to
tar xvf etcd-v3.5.6-linux-amd64.tar.gz
mv etcd-v3.5.6-linux-amd64 etcd
cd etcd
sudo mv etcd etcdctl etcdutl /usr/local/bin/
etcd --version
etcdctl version
etcdutl version
```
We need to change the API version to 3. To do that, use the below command.

```
export ETCDCTL_API=3 etcdctl version
etcdctl version
```
![image](https://github.com/sayanalokesh/kubernetes_CKA/assets/105637305/4be0d8a5-2ad1-4234-a99e-780f159a0959)
![image](https://github.com/sayanalokesh/kubernetes_CKA/assets/105637305/d4b19e82-173c-40e9-b696-c71f89f4a032)

