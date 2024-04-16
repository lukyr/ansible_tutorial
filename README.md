# Ansible Tutorial

ansible all --key-file ~/.ssh/ansible -i inventory -m ping

ansible all -m gather_facts --limit 192.168.56.4

ansible all -m apt -a update_cache=true --become --ask-become-pass

## Command Explanation

- **`ansible`**: This is the main command that invokes Ansible.
- **`all`**: This is the target for the Ansible command. In this case, it's set to `all`, which means the command will be run on all hosts in the inventory.
- **`-m apt`**: This part of the command specifies the module to be used. The `apt` module is used for package management in Debian-based Linux distributions.
- **`-a update_cache=true`**: The `-a` flag is used to pass arguments to the module. In this case, `update_cache=true` is passed to the `apt` module, which means the command will update the package cache on the target hosts.
- **`--become`**: This flag is used to elevate privileges, which is often necessary when making changes to a system. By default, Ansible runs tasks as the current user. If you need to perform tasks that require root or another user's permissions, you can use the `--become` option.
- **`--ask-become-pass`**: This flag prompts for the privilege escalation password. When you use the `--become` option, you might need to enter a password to gain the necessary privileges. The `--ask-become-pass` option prompts you to enter this password when you run the command.

## Install Package using CLI

ansible all -m apt -a name=vim-nox --become --ask-become-pass

ansible all -m apt -a name=tmux --become --ask-become-pass

ansible all -m apt -a name="snapd state=latest" --become --ask-become-pass

## Playbook Tags

- **`listing ansible-playbook`**
  ansible-playbook --list-tags site.yml
- **`install using tag`**
  ansible-playbook --tags ubuntu --ask-become-pass site.yml
