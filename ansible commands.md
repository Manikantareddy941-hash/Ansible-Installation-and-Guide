Here is the **full Ansible command list**

---

# 🧾 Ansible Basics & Info

ansible --version — we use it to check the installed Ansible version

ansible --help — we use it to list all Ansible CLI options

ansible-doc -l — we use it to list all available modules

ansible-doc module_name — we use it to view documentation of a module

---

# 📡 Ad-Hoc Commands (Quick Tasks)

ansible all -m ping — we use it to test connectivity to hosts

ansible webservers -m command -a "uptime" — we use it to run a command

ansible webservers -m shell -a "df -h" — we use it to run shell commands

ansible webservers -m copy -a "src=file dest=/tmp/file" — we use it to copy files

ansible webservers -m service -a "name=nginx state=started" — we use it to manage services

ansible webservers -m package -a "name=nginx state=present" — we use it to install packages

ansible webservers -m user -a "name=dev state=present" — we use it to manage users

ansible webservers -m file -a "path=/tmp/test state=touch" — we use it to manage files

ansible localhost -m setup — we use it to gather system facts

---

# 🚀 Playbook Execution

ansible-playbook playbook.yml — we use it to execute a playbook

ansible-playbook -i inventory.ini playbook.yml — we use it to run with a specific inventory

ansible-playbook playbook.yml --limit webservers — we use it to run on selected hosts

ansible-playbook playbook.yml -e "var=value" — we use it to pass variables

ansible-playbook playbook.yml --tags "tagname" — we use it to run specific tagged tasks

ansible-playbook playbook.yml --skip-tags "tagname" — we use it to skip tasks

ansible-playbook playbook.yml --start-at-task "task name" — we use it to resume from a task

ansible-playbook playbook.yml --ask-become-pass — we use it to prompt for sudo password

---

# 🧪 Debugging & Dry Runs

ansible-playbook playbook.yml --check — we use it to preview changes (dry run)

ansible-playbook playbook.yml --diff — we use it to show file differences

ansible-playbook playbook.yml -vvv — we use it to get detailed debug output

---

# 📂 Inventory Management

ansible-inventory --list -i inventory.ini — we use it to display inventory details

ansible-inventory --graph -i inventory.ini — we use it to show group hierarchy

ansible-inventory --host hostname -i inventory.ini — we use it to show host variables

---

# ⚙️ Configuration

ansible-config view — we use it to display active configuration

ansible-config dump — we use it to list all config settings

ansible-config list — we use it to see configurable options

---

# 🔐 Ansible Vault (Security)

ansible-vault create secrets.yml — we use it to create encrypted file

ansible-vault encrypt secrets.yml — we use it to encrypt a file

ansible-vault decrypt secrets.yml — we use it to decrypt a file

ansible-vault edit secrets.yml — we use it to edit encrypted file

ansible-vault view secrets.yml — we use it to view encrypted content

ansible-vault rekey secrets.yml — we use it to change vault password

ansible-playbook playbook.yml --ask-vault-pass — we use it to run playbook with vault

---

# 📦 Roles & Galaxy

ansible-galaxy init role_name — we use it to create a role structure

ansible-galaxy install role_name — we use it to download a role

ansible-galaxy list — we use it to list installed roles

ansible-galaxy remove role_name — we use it to delete a role

ansible-galaxy collection install collection_name — we use it to install a collection

ansible-galaxy collection list — we use it to list collections

---

# 🔄 Advanced Execution

ansible-pull -U repository_url — we use it to pull playbooks from Git and run

ansible-console — we use it to run Ansible interactively

ansible localhost -m debug -a "msg='test'" — we use it to print debug messages

---

# 🧹 Maintenance & Utilities

ansible all -m setup --tree /tmp/facts — we use it to save facts to files

ansible-playbook playbook.yml --syntax-check — we use it to validate playbook syntax

ansible-playbook playbook.yml --list-tasks — we use it to list tasks

ansible-playbook playbook.yml --list-hosts — we use it to list target hosts

ansible-playbook playbook.yml --list-tags — we use it to list all tags

---
