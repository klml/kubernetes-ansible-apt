# kubernetes-ansible-apt

ansible playbook to setup a kubernetes cluster with one master and worker nodes using apt based nodes

This is inspired by [kubernetes-and-ansible](https://github.com/learnitguide/kubernetes-and-ansible) (for centos) and [Kubernetes Setup Using Ansible and Vagrant](https://kubernetes.io/blog/2019/03/15/kubernetes-setup-using-ansible-and-vagrant/)

There are many other similar projects, but with diffrent aproaches:
* This playbook only installs kubernetes, but __no virtualization__ like Vagrant or KVM.


This was tested with plain ubuntu hosts on [hetzner.com/cloud](https://www.hetzner.com/cloud), but without proprietary [hcloud](https://github.com/hetznercloud/cli).


## usage

* create your local inventory: `cp inventories/cluster.ini.example inventories/cluster.ini`
* add node host IP or Domain to inventories/cluster.ini

```
ansible-playbook playbooks/install_cluster.yaml -i inventories/cluster.ini
```


