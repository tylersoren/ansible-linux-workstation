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
```

# Resources

* https://gist.github.com/PashCracken/b6070359486ea651eed66a5e86567ebb
* https://itnext.io/setting-up-the-kubernetes-tooling-on-windows-10-wsl-d852ddc6699c

