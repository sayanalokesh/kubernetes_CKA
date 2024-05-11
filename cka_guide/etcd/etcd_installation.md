ETCDCTL is the CLI tool used to interact with ETCD.

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


ETCDCTL can interact with ETCD Server using 2 API versions - Version 2 and Version 3.  By default its set to use Version 2. Each version has different sets of commands.

For example ETCDCTL version 2 supports the following commands:

etcdctl backup
etcdctl cluster-health
etcdctl mk
etcdctl mkdir
etcdctl set


Whereas the commands are different in version 3

etcdctl snapshot save 
etcdctl endpoint health
etcdctl get
etcdctl put

To set the right version of API set the environment variable ETCDCTL_API command

export ETCDCTL_API=3

When API version is not set, it is assumed to be set to version 2. And version 3 commands listed above don't work. When API version is set to version 3, version 2 commands listed above don't work.

