# Ansible role: Configure servers as Kubernetes master and nodes

## A fair note

This is untested as of late and still a big Work in progress.

## Prerequisites

The servers used in this playbook must be Ubuntu based, have a predefined admin user and your SSH pub key for keyless authentication must be configured.

## Running the playbook

```bash
ansible-playbook configure_k8s_cluster.yaml -i inventory/hosts/kubernetes.yaml
```

## Discovering MicroK8s

The start command will start all enabled Kubernetes services: `microk8s start`
The inspect command will give you the status of services: `microk8s inspect`
The stop command will stop all Kubernetes services: `microk8s stop`
You can easily enable Kubernetes add-ons, eg. to enable “kubedns”: `microk8s enable dns`
To get the status of the cluster`: microk8s kubectl cluster-info`

## Documentation

The commands and structure for this repo is based on [these instructions](https://ubuntu.com/tutorials/how-to-kubernetes-cluster-on-raspberry-pi#1-overview)

The Microk8s documentation can be found [by visiting this link](https://microk8s.io/docs/)

General documentation [how to install and configure microk8s](https://www.server-world.info/en/note?os=Ubuntu_20.04&p=microk8s&f=1) by server-world.info
