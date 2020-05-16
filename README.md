Try to manage /etc/hosts with aliases (defined in hosts_vars)

# Setup the VM

```
vagrant up
```

# Launch ansible

```
ansible-playbook -i inventories/test playbook.yml
```

Need to be launched twice in this example because /etc/hosts is initialised with : 127.0.0.1 	hostname     hostname


# Check

```
clear; vagrant ssh p10 -c "cat /etc/hosts"; vagrant ssh p11 -c "cat /etc/hosts"; vagrant ssh p12 -c "cat /etc/hosts"
```