# ansible-provisionings

general file var
```bash
for var in aws ec2 vpc; \
do cp -v vars/$var.yml.example vars/$var.yml; done
```