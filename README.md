# ansible-linux-workstation
Ansible config for my Linux workstation setup


1. Install Ansible

    ```
    sudo apt update
    sudo apt install software-properties-common
    sudo apt-add-repository --yes --update ppa:ansible/ansible
    sudo apt install ansible
    ```

2. Run playbook

```
sudo ansible-playbook playbook/playbook.yaml