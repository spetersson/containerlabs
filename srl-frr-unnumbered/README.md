# Nokia SR Linux and FRR unnumbered lab

## Introduction

There are two toplogies in this directory. One for a full deployment with 2
spines, 4 leafs and 4 servers.

To launch the full topology:

``` shell
sudo containerlab deploy -c -t top-full.clab.yml
```

To launch the small topology:
``` shell
sudo containerlab deploy -c -t top-small.clab.yml
```

To destroy the full topology:
``` shell
sudo containerlab destroy -c -t top-full.clab.yml
```

To destroy the small topology:
``` shell
sudo containerlab destroy -c -t top-small.clab.yml
```


How to run the ansible playbook in order to install and configure FRR:
``` shell
ansible-playbook -i clab-nokia-srl-ip-fabric/ansible-inventory.yml ansible_generic_vm.yaml --diff
```
