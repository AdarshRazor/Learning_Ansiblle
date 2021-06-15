# Ansible

### What it is ?

It is a tool developed by Red Hat to automate the configuration of all  the system. People can write simple code in YAML, and these codes are deployed on 100s of server which config. them to desired states.
It does the following things:
1. Configuration Management - Configuring you system
2. Automates Orchestration - Brings together a no. of application decides in which order these are execited.
3. Deployment - Automates deployment of an application

### Why Ansible ?

Imagine being in a company as system admin. and you have to configure some servers with the same environment. It's easy to do, but what if the number of server increases and the same task must be repeated multiple times. Moreover, humans are prone to make errors. 

Here comes the **Ansible** comes to rescue, which is written in code once for the installation and deployed multple times.
Now you just have to write the script onces and can be deployed multiple times.

### Where Ansible can be used ?

1. IT Automation - Instructions are written to automate the IT professional's work
2. Configuration Managment - Consistency of all systems in the infrastructure is maitained.
3. Automatic deployment - Applications are deployed automatically on a variety of environments.

> Ansible is a push type of configuration management tool. It allows to push the configuration in the node machine.

### Ansible architecture

![Images](https://github.com/AdarshRazor/Learning_Ansiblle/blob/main/architecture.png "architecture of ansible")

### Playbook 

```ansible
---                             # starting the playbook
-name: play1                        # Play 1
 hosts: webserver                       # node 1
 tasks:                                 # tasks
  -name: install apache                     # name of task
   yum:                                         # to do the task we need these service to perform
      name: apache                                  # name
      state: present                                # state of the service
  -name: start apache                       # name of task
   service:                                     # to do the task we need these service to perform
      name: apache                                  # name
      state: start                                  # state of the service
-name: play2                        # Play 2
 hosts: databaseserver                  # node 2
 tasks:                                 # tasks
  -name: install MySQL                      # name of task
   yum:                                         # to do the task we need these service to perform
      name: MySQL                                   # name
      state: present                                # state of the service
```

### Inventory 

**webserver** (names or ip of the machines)

web1.machine   

web2.machine

web3.machine

**databaseserver**

db1.machine
