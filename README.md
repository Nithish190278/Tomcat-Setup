🚀 Apache Tomcat Setup using Ansible

This repository contains an Ansible automation to install and configure Apache Tomcat on a single Amazon Linux server.
The goal of this project is to simplify Tomcat installation using Ansible and make the setup easy to repeat in the future.

📌 Overview

In this setup, Ansible and Tomcat run on the same server.
No inventory file is required because the playbook executes locally.
This approach is useful for learning, testing, and quick deployments.

⚙️ Prerequisites

You need an Amazon Linux server with internet access and sudo or root permissions.
Port 8080 must be allowed in the server security group to access Tomcat.

🔐 Step 1: Login to the Server

Login to the server and switch to root user.

sudo -i

📦 Step 2: Install Required Packages

Install Git to clone the repository.

yum install git -y


Install Ansible.

yum install ansible -y


(Optional) Install Python dependencies if required.

yum install python3 python-pip python-devel -y

📥 Step 3: Clone the Repository

Clone the GitHub repository.

git clone https://github.com/Nithish190278/Tomcat-Setup.git


Move into the project directory.

cd Tomcat-Setup

▶️ Step 4: Run the Ansible Playbook

Execute the Ansible playbook to install and configure Tomcat.

ansible-playbook tomcat.yml


This command installs Java, downloads Apache Tomcat, configures users and manager access, and starts the Tomcat service automatically.

🌐 Verification

After the playbook completes successfully, open a browser and access Tomcat.

Tomcat home page:

http://SERVER_IP:8080


Tomcat Manager page:

http://SERVER_IP:8080/manager/html

🔑 Default Login Credentials

Username: tomcat
Password: nithish123

These credentials are for learning purposes only and should not be used in production environments.

📝 Notes

This setup does not require an inventory file because it runs on a single server.
The same playbook can later be used for multiple servers by adding an inventory file.
This project follows standard DevOps automation practices using Ansible.

👨‍💻 Author

Nithish Kumar Palla
