# Ansible-VMware
> An ansible project which automates the virtual machines deployment procedure on VMware environments

## v1.0 features

This version is created with the following settings as an input:

- CPU (sockets x cpu)
- Memory (ram in MB)
- Disk (one disk and its type thin/thick)

## How to use 

> Edit deploy.yml

    datastore_name: your_datastore_name
    template_name: your_template_name
    datacenter_name: your_vmware_datacenter_name
    cluster_name: your_vmware_cluster_name


> Edit ansible vault (secrets.yml)


`ansible-vault edit secrets.yml ("password")`


    username: administrator@vsphere.local
    password: password
    hostname: vcenter.hostname

> Edit vms list (vms.yml)

     - name: test1-ansible
        folder: ansible
        cpus: 1
        sockets: 1
        memory: 64
        disksize: 1
        disktype: thin
