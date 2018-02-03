# Configuration Management

## Roles

### 1) CoffeeMaker:

    To create CoffeeMaker Server and install all the dependencies requrired and then run it.
    

### 2) Selenium:

    To create Selenium Server and install all the dependencies requrired and then test the server running on 192.168.33.11

## Setup

### Vagrant Machines

You need three vagrant machines:

1. Ansible Server (192.168.33.10)
    
    I have added Vagrantfile, you can have a look, keep it similar.

2. CoffeeMaker (192.168.33.11)

    Increase the virtual memory to 2048 because server needs memory. Copy the private key .vagrant folder into Ansible-Server/keys 
    and change the permission to 600 using chmod 600 CoffeeMaker_private_key
3. Selenium (192.168.33.12)

    Copy the private key .vagrant folder into Ansible-Server/keys and change the permission to 600 using chmod 600 Selenium_private_key
    
 Once three of the VMs are set up, you just need to run this command on ansible-server VM ` ansible-playbook playbook.yml -i inventory -vvv `
 
 


