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