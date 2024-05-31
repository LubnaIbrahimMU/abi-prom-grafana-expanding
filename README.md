
# Ansible WordPress Deployment

A brief description of what this project does and who it's for


This repository contains Ansible roles and a playbook for deploying WordPress on an EC2 instance along with MySQL database setup. Additionally, it includes roles for managing EC2 instances and setting up Prometheus and Grafana on the same machine.




## Roles :


* ec2-instance: Creates an EC2 instance of type t3.small with Ubuntu 22.04 OS.
* mysql: Installs MySQL 8 on the EC2 instance and sets up a daily backup cron job.
* wordpress: Installs and configures WordPress along with all necessary configurations (Nginx).
* prometheus-grafana: Installs Prometheus and Grafana on the same WordPress    EC2 instance and configures Grafana accessible from a sub-URI.







## Playbook
The wordpress.yml playbook orchestrates the deployment, including all necessary roles for creating the EC2 instance, installing WordPress and MySQL, and setting up Prometheus and Grafana.

## Usage
Running the Playbook
To deploy WordPress and associated services, run the following command:

To deploy this project run

```bash
ansible-playbook -i demo.aws_ec2.yml --private-key lu2  wordpress.yml -e "@all.yml"
```


## Accessing WordPress and Grafana

* WordPress: Accessible at http://<EC2_Instance_IP>
* Grafana: Accessible at http://<EC2_Instance_IP>:3000


