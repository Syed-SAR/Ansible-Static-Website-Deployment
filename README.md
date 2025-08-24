# Ansible Static Website Deployment
Deploying a Static Website on Remote Server Using Ansible

![Ansible](https://img.shields.io/badge/Ansible-Automation-blue?logo=ansible)
![License](https://img.shields.io/badge/License-MIT-green)
![Apache](https://img.shields.io/badge/Apache-HTTPD-orange?logo=apache)

A simple Ansible playbook that installs, configures, and starts the Apache HTTPD web server on target machines.  
It also deploys a custom **index.html** page and automatically restarts the service if the file changes.

---

## 📌 Features

✅ Installs the `httpd` package  
✅ Starts and enables the HTTPD service  
✅ Copies a custom web page to `/var/www/html/index.html`  
✅ Restarts HTTPD automatically if the page changes  


---

## 📋 Prerequisites

- **Ansible** installed on the control node
- SSH access to the target host(s)
- Target host(s) listed under `[target1]` in your Ansible inventory
- A `index.html` file at `/home/ansible/index.html` on the control node

---

## 🚀 Usage

1️⃣ **Clone the Repository**
```bash
git clone https://github.com/your-username/ansible-httpd-playbook.git
cd ansible-httpd-playbook

## Add Inventory Details
[target1]
server1 ansible_host=192.168.1.100 ansible_user=ec2-user

## Run the Playbook
ansible-playbook -i hosts playbook.yml

## Verify it
http://<target-host-public-ip>


