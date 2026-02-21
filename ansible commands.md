---

ansible-playbook playbook.yml — we use it to execute an Ansible playbook

ansible-playbook -i inventory.ini playbook.yml — we use it to run a playbook using a specific inventory file

ansible-playbook playbook.yml --limit webservers — we use it to run a playbook only on selected hosts

ansible-playbook playbook.yml -e "var=value" — we use it to pass extra variables at runtime

ansible-playbook playbook.yml --check — we use it to perform a dry run and preview changes

ansible-playbook playbook.yml --diff — we use it to show configuration differences before applying

ansible-playbook playbook.yml -vvv — we use it to get detailed verbose debugging output

ansible-playbook playbook.yml --ask-become-pass — we use it to prompt for sudo password

ansible-playbook playbook.yml --start-at-task "task name" — we use it to start execution from a specific task

ansible-playbook playbook.yml --tags "tagname" — we use it to run only tasks with a specific tag

ansible-playbook playbook.yml --skip-tags "tagname" — we use it to skip tasks with a specific tag

---

ansible all -m ping — we use it to test connectivity to all hosts

ansible webservers -m command -a "uptime" — we use it to run a command on remote hosts

ansible webservers -m shell -a "df -h" — we use it to run shell commands

ansible webservers -m copy -a "src=file dest=/tmp/file" — we use it to copy files

ansible webservers -m service -a "name=nginx state=started" — we use it to manage services

ansible webservers -m package -a "name=nginx state=present" — we use it to install packages

ansible webservers -m user -a "name=dev state=present" — we use it to manage users

ansible webservers -m file -a "path=/tmp/test state=touch" — we use it to manage files

---

ansible-inventory --list -i inventory.ini — we use it to display inventory in JSON format

ansible-inventory --graph -i inventory.ini — we use it to view host group hierarchy

ansible-inventory --host hostname -i inventory.ini — we use it to see variables of a host

---

ansible-config view — we use it to display the active configuration

ansible-config dump — we use it to list all configuration settings

ansible-config list — we use it to view all configurable options

---

ansible-doc -l — we use it to list all available modules

ansible-doc module_name — we use it to view documentation of a module

---

ansible-galaxy init role_name — we use it to create a new role structure

ansible-galaxy install role_name — we use it to download a role from Galaxy

ansible-galaxy list — we use it to list installed roles

ansible-galaxy remove role_name — we use it to delete an installed role

ansible-galaxy collection install collection_name — we use it to install a collection

ansible-galaxy collection list — we use it to list installed collections

---

ansible-vault create secrets.yml — we use it to create an encrypted file

ansible-vault encrypt secrets.yml — we use it to encrypt an existing file

ansible-vault decrypt secrets.yml — we use it to decrypt a file

ansible-vault edit secrets.yml — we use it to edit encrypted files

ansible-vault view secrets.yml — we use it to view encrypted content

ansible-vault rekey secrets.yml — we use it to change vault password

---

ansible-pull -U repository_url — we use it to pull and run playbooks from a Git repo

ansible-console — we use it to run Ansible commands interactively

ansible localhost -m setup — we use it to gather system facts

---
