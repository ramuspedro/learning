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

## Running kubectl

- First run minikube (if you run kubernetes on minikube)

```sh
$ minikube start
```

## Commands

```sh
# delete all pods of ns
$ kubectl delete --all pods --namespace=kube-system
```

- If you have deployment

```sh
# change ns

$ kubectl config set-context --current --namespace=ns

$ kubectl delete ns kube-system

$ kubectl get deployment --all-namespaces

$ kubectl delete deploy name-deployment -n ns
```

## Problems

### The connection to the server

- https://discuss.kubernetes.io/t/the-connection-to-the-server-host-6443-was-refused-did-you-specify-the-right-host-or-port/552/5

```sh
$ kubectl get nodes
# The connection to the server 10.0.2.15:6443 was refused - did you specify the right host or port?
```

1. sudo -i
2. swapoff -a
3. exit
4. strace -eopenat kubectl version
