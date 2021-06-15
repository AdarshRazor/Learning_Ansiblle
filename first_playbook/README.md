# Ansible Playbook

Ansible playbooks are written using the YAML language. It create a file with **.yml** or **.yaml** extension.

It begins with a **three dash (---)**                                      
Then immediately begins with **singl dash (-)** with name.                  
Then hosts expects a value like all or group.
Then specify do you want to become root.

Then start with the tasks. 
Name of the task.
What that service will going to do.

### Prerequisites

Edit the ansible-hosts file and add the ip address of the node machine ( client machine )

```cat /etc/ansible/hosts```

add the ip address of the node under the client group with user and pass

>192.168.45.137 ansible_ssh_user=root ansible_ssh_pass=password

To check the YAML file is correct you can either check in the cmd line or using this [link](http://www.yamllint.com/) to check.

```ansible-playbook sample.yml --syntax-check```

If nothing goes wrong then it just print the name of the playbook

Now send the playbook to client machine

```ansible-playbook sample.yml```

#### Alternate 

If you have spefic file of the ip address then use the below command

```ansible-playbook -i <name-of-the-file> sample.yml```