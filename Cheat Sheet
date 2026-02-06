✅ Check install
ansible --version

📂 Inventory file
nano inventory

[servers]
IP1
IP2

🔌 Test connection
ansible servers -i inventory -m ping

▶ Run command on all servers
ansible servers -i inventory -a "uptime"
ansible servers -i inventory -a "hostname"
ansible servers -i inventory -a "df -h"

📦 Install package (Ubuntu)
ansible servers -i inventory -b -m apt -a "name=nginx state=present"

❌ Remove package
ansible servers -i inventory -b -m apt -a "name=nginx state=absent"

🔄 Restart service
ansible servers -i inventory -b -m service -a "name=nginx state=restarted"

📁 Copy file
ansible servers -i inventory -m copy -a "src=file.txt dest=/tmp/file.txt"

📄 Create file
ansible servers -i inventory -m file -a "path=/tmp/test.txt state=touch"

▶ Run playbook
ansible-playbook -i inventory playbook.yml

🎯 Run on one server only
ansible servers -i inventory --limit IP1 -a "uptime"

📜 Show all hosts
ansible servers -i inventory --list-hosts
