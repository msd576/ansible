# ansible
Setup: 3 VMs - 1 Controller, 2 Hosts (Linux systems).<br>
Controller contains: inventory and playbook.<br>
Controller connect to Hosts using SSH.<br>

### Install Ansible on controller
$ sudo apt update <br>
$ sudo apt install software-properties-common <br>
$ sudo add-apt-repository --yes --update ppa:ansible/ansible <br>
$ sudo apt install ansible <br>

### Create an 'ansible' user
on control node:<br>
$ sudo useradd ansible <br>
$ ssh <host> -> repeat for each host <br>
$ sudo useradd ansible<br>
$ sudo passwd ansible<br>
$ logout<br>

### Configure Pre-shared key for ansible
$ sudo su - ansible <br>
$ ssh-keygen<br>
$ ssh-copyid <host><br>
$ ssh <host> -> to verify we can login without password<br>
$ logout<br>

### Add ansible to sudoers list
$ ssh <host> <br>
$ sudo visudo <br>
add this line at the end of the file: <br>
ansible      ALL=(ALL)      NOPASSWD: ALL<br>
save and quit, logout.<br>

### Configure inventory and run playbook
Create a simple inventory in /home/ansible/inventory, consisting of hosts <br>
Create a simple playbook and run using the below command: <br>
$ ansible-playbook -i /home/ansible/inventory /path/to/ansible-playbook.yml <br>


