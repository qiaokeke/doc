### /etc/ansible/hosts
```
192.168.1.50
aserver.example.org
bserver.example.org
```

### ansible all -m ping
```
# as bruce
$ ansible all -m ping -u bruce
# as bruce, sudoing to root
$ ansible all -m ping -u bruce --sudo
# as bruce, sudoing to batman
$ ansible all -m ping -u bruce --sudo --sudo-user batman

```
