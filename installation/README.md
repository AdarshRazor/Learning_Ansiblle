### Installation

Prerequisites:
1. RHEL OS
2. Node System - Client System
3. Server System - Master System

Master System: ```yum install ansible -y``` 

### Setting up

Ansible host file: ```nano /etc/ansible/hosts```

add the ipaddress under the collection of hosts belonging to the 'webservers' group

```192.168.2.11 ansible_ssh_user=root ansible_ssh_pass=password``` (ipaddress node_server_username node_server_pass)

### Writing Code

Then write playbook which is written in YAML.

```nano sample.yml```

Use this [YAML file](./sample.yml) as an example.

Check the yaml file by typing this command.

```ansible-playbook sample.yml --syntax-check```

If nothing goes wrong then it just print the name of the playbook

### Execution 

Now send the playbook to client machine

```ansible-playbook sample.yml```

Check the output as it will gives the details of things which got changed and get successful.

Example:
> 192.168.2.11          : ok=4  changed=2   unreached=0     failed=0
