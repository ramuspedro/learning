# Kubernetes

## Instalation on VM

```sh
$ swapoff -a

# comment the swap disk if it exits
$ vi /etc/fstab

# add Google's apt repository gpg key
$ curl -s https://packages.cloud.google.com/apt/doc/apt-key.gpg | sudo apt-key add -
```

Add the kubernetes apt repository

```
bash -c 'cat <<EOF >/etc/apt/sources.list.d/kubernetes.list
deb https://apt.kubernetes.io/ kubernetes-xenial main
EOF'
```

```sh
# update packages
$ apt-get update

# see the versions
$ apt-cache policy kubelet | head -n 20

$ apt-cache policy docker.io | head -n 20

# install required packages
$ apt-get install -y kubelet kubeadm kubectl docker.io

# not upgradable
$ apt-mark hold kubelet kubeadm kubectl docker.io

# status
$ systemctl status kubelet.service

$ systemctl status docker.service
```
