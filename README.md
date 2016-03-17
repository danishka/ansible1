#Ansible Test

## How to setup

01. Update inventory/hosts file with ip address and the private_key
02. Currect host IP addess and private_key filename should be update in group_vars/config file
03. Disable host key check
  
 Add following entry to /etc/ansible/ansible.cfg file, under {default] block if you need to disable host key check.  
```sh  
  [defaults]
  host_key_checking = false 
```  

## How to run

01). Please run the following command you once replaced above mentioned variables. 

```sh
ansible-playbook -i  inventory/hosts site.yml 
```
 
02). for a verbose output:
```sh
ansible-playbook -i  inventory/hosts site.yml  -vvv
```

##Additional Information

* This project has been tested on AWS using CentOS community AMI (ami-106aa373).
* Host node and all type_a and type_b servers were deployed on same VPC with same security group and same keypair.
