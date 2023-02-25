#  Docker and Docker Compose Auto Install with Ansible

This is a simple Ansible playbook to install Docker and Docker Compose on a remote server.

## Environment
- WSL2 (Ubuntu 22.04) on Windows 11
- ansible [core 2.13.5]

## Usage
1. Create `hosts` file and add your server IP address.
   ```bash
    [GROUP_NAME]
    YOUR_SERVER_IP
    ```
2. Install Ansible on your local machine.
   ```bash
    $ pip install ansible
    ```
3. ssh to your server and add your public key to `~/.ssh/authorized_keys`.  
   Tips: If you want to use password, add　`ansible_ssh_user=` as shown below in `hosts` file.
    ```bash
    [GROUP_NAME]
    YOUR_SERVER_IP ansible_ssh_user=YOUR_USER_NAME ansible_ssh_pass=YOUR_PASSWORD
     ```
4. Run the playbook.
   ```bash
    $ ansible-playbook -i hosts main.yml
    ```
5. Check the installation.