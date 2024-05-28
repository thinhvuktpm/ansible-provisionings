# ansible-provisionings

tạo file env
```bash
for var in aws ec2 vpc project var; \
do cp -v vars/$var.yml.example vars/$var.yml; done
```
- file aws.yml là file khai báo key và name các services
***
build server on the aws
```bash
ansible-playbook install_ec2.yml
```

ping to all server
```bash
ansible all -m ping -i evironment.ini
```

```bash
ssh -F ssh_config bastion-production
```
