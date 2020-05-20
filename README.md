# ansible-linux-workstation
Ansible config for my Linux workstation setup.  This is currently geared to a Windows Subsystem for Linux (WSL) setup but could be easily adapted.  Some WSL specific settings include creation of wsl.conf file and creating a symlink to the kube config in Windows so it can be shared. 

The username is declared as a variable in playbook.yaml for assigning permissions along with the underlying Windows OS user path.  Update these accordingly.

Because the kube-tools tasks create a symlink to a path starting with /c/ that is created earlier in the play but won't appear until restart, the playbook will fail when running the first time.  Restart your WSL distro with this windows command (replacy distro name as needed) before running again.

` wsl -t Ubuntu-18.04 `


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

For all of the zsh customizations to display properly you will need to install new fonts in Windows and update your shell or code editor accordingly.  See:  
https://gist.github.com/PashCracken/b6070359486ea651eed66a5e86567ebb#install-required-nerd-fonts

https://www.nerdfonts.com/ 

https://github.com/ryanoasis/nerd-fonts/releases


# Resources

* https://gist.github.com/PashCracken/b6070359486ea651eed66a5e86567ebb
* https://itnext.io/setting-up-the-kubernetes-tooling-on-windows-10-wsl-d852ddc6699c
* https://www.edwardthomson.com/blog/git_credential_manager_with_windows_subsystem_for_linux.html

