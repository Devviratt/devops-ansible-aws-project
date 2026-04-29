# DevOps Project: Multi-Tier Web Architecture using AWS & Ansible

## Overview
This project demonstrates a multi-tier architecture using AWS EC2 instances and Ansible automation.

## Architecture
Control Node → Frontend (Nginx) → Backend (Node.js)

## Features
- Automated deployment using Ansible
- Frontend server using Nginx
- Backend server using Node.js
- Reverse proxy configuration
- Login system with dashboard

## Playbooks
- frontend.yml → installs Nginx
- backend.yml → installs Node.js
- frontend-proxy.yml → configures reverse proxy

## Usage
1. Connect to control node
2. Run playbooks:
   ansible-playbook -i hosts.ini frontend.yml
   ansible-playbook -i hosts.ini backend.yml
   ansible-playbook -i hosts.ini frontend-proxy.yml


## ⚙️ Tech Stack
AWS EC2, Ansible, Nginx, Node.js

## 🔑 Login
Username: admin  
Password: 1234
