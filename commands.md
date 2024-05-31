ansible-playbook -i demo.aws_ec2.yml --private-key lu2  wordpress.yml -e "@all.yml"  --ask-vault-pass


ansible-vault encrypt main.yml

ansible-inventory -i demo.aws_ec2.yml --graph


