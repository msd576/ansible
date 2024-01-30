# ansible
Setup: 3 VMs - 1 Controller, 2 Hosts (Linux systems).<br>
Controller contains: hosts.ini and playbook.<br>
Controller connect to Hosts using SSH.<br>

Run ssh-keygen on controller machine to generate SSH key-pair.<br>
Copy public key to host machines using ssh-copy-id.<br>
Ensure connection between controller and host machines.
