# ansible-provisionings

tạo file env
```bash
for var in aws ec2 vpc project var app; \
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
ansible all -m ping -i prod.ini
```

ssh to server
```bash
ssh -F ssh_config bastion-prod
```

setup ruby on rails
```bash
ansible-playbook setting_deploy_ruby.yml -i prod.ini
```
--- 
define vars/app.yml
```bash
app_name: name app
app_evironment: name evironment
name_service: name services. ex: ec2 name_tag 
user_deploy: user deploy to ec2
ruby_version: 3.2.0 ## not define
```
archivo vars/var.yml se genera al configurar servicios
