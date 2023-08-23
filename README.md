# Deploy ELK 8.X Automation with Ansible

## How it works!

> run command line herer:

```bash
ansible-playbook -i site/cluster_els cluster.yml
```

# Reference


#### - {{ hostvars[host]['ansible_host'] }}

### Fix Stack Monitoring "access denied" after 8.0.0 upgrade
Add line to file kibana.yml
```bash
monitoring.ui.ccs.enabled: false
```
