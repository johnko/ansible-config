# pbj

Playbooks and j...

## Run upgrades:

```
ansible-playbook playbook/upgrades.yml --inventory inventory/home.yml --become --ask-become-pass --limit servers
```

## Run ad-hoc commands:

```
ansible all --inventory inventory/home.yml --become --ask-become-pass --module-name=shell --args='apt-get update && apt-get --yes dist-upgrade && apt-get --yes autoremove'

ansible servers --inventory inventory/home.yml --become --ask-become-pass --module-name=shell --args='apt-get update && apt-get --yes dist-upgrade && apt-get --yes autoremove'
```

## Reference

- http://docs.ansible.com/ansible/playbooks.html
