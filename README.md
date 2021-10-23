# ec2-automation

This is a simple terraform automation to launch ubuntu 18.x instance with port 8080 and 22 open with default vpc and install python jdk and jenkins with ansible

HOW TO USE 

1 .install aws-cli and configure (aws configure) it with your private key and public key

2 install terraform and

2.1 navigate to terraform-file and add your ssh key on main.tf file (if you do not have one generate it using ssh-keygen)
2.2 run terraform Init
this will initialize your terraform
2.3 run terraform validate 
this will check and validate your file
2.4 run terraform plan and terraform apply
2.5 navigate to your ec2 page and confirm new ec2 instance running

3 install ansible and

configure your /etc/ansible/hosts file

3.1 navigate to your ansible-file/playbook
3.2 run ansible-playbook install-python.yaml
3.3 run ansible-playbook install-java.yaml
3.4 run ansible-playbook jenkins-install.yaml

this will install python, java and jenkins on your slave node

navigate to your <public-address>:8080 and verify jenkins is running
