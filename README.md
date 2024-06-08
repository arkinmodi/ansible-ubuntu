# Automated Personal Environment Setup

1. Setup GitHub SSH keys
1. Install [Ansible](https://docs.ansible.com/ansible/latest/installation_guide/installation_distros.html#installing-ansible-on-ubuntu)
   via their PPA

    > Note: `python3-psutil` is needed for the `community.general.dconf` Ansible
    > Module

    ```sh
    sudo apt update
    sudo apt install software-properties-common
    sudo add-apt-repository --yes --update ppa:ansible/ansible
    sudo apt install ansible python3-psutil
    ```

1. Run setup playbook

    ```sh
    ansible-pull --ask-become-pass --url https://github.com/arkinmodi/ansible-ubuntu

    # Or if cloned locally
    ansible-playbook --ask-become-pass local.yml
    ```
