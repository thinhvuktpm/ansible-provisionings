# ansible-provisionings

general file var
```bash
for var in aws ec2 vpc project; \
do cp -v vars/$var.yml.example vars/$var.yml; done
```

build server on the aws
```bash
ansible-playbook install_aws.yml
```

generate file setup ansible for local
```bash
ansible-playbook config_ansible.yml
```

ping to all server
```bash
ansible all -m ping -i evironment.ini
```

build file setup ansible for local
```bash
ansible-playbook setup_server.yml -i production.ini
```

```bash
ssh -F ssh_config bastion-production
```
