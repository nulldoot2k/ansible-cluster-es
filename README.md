# ELK Stack Version 8.X Auto Deployment with Ansible Playbook

This ansible collection will install and configure a high available Elasticsearch cluster.

## How it works!

Ansible setup and pre-flight check

### Edit file host

The ELK Stack cluster uses many master nodes and many worker nodes, so change it yourself to your liking.

- file edited: `site/cluster_elk``

Change version cluster elk
- file edited: `group_vars/all``
- version elastics: `es_version: "8.3.3"`
- version logstash: `lo_version: "1:8.3.3-1"`

Change dns
- dns_kibana: ''

Change parameter MEM
- es_heap_size: `"1g"`
- lo_jvm_xmx: `"1g"`
- lo_jvm_xms: `"1g"`

### Deploy ELK with Ansible

```bash
ansible-playbook -i site/cluster_els cluster.yml
```

### Uninstall Cluster ELK Stack

```bash
ansible-playbook -i site/cluster_els cluster.yml --tag uninstall
```