# 🚀 Multi-Tier Web Architecture using AWS EC2 & Ansible

## 📌 Overview
This project demonstrates a multi-tier web architecture deployed on AWS EC2 instances and automated using Ansible.  
The system is designed to simulate a real-world DevOps environment with frontend and backend separation.

---

## 🏗️ Architecture

Control Node (Ansible)         ↓ Frontend Servers (Nginx)         ↓ Backend Servers (Node.js)

---

## ⚙️ Technologies Used

- ☁️ AWS EC2  
- ⚙️ Ansible  
- 🌐 Nginx (Frontend)  
- 🟢 Node.js (Backend)  
- 🔐 SSH  

---

## 🔥 Features

- Automated server configuration using Ansible  
- Multi-server architecture (Frontend + Backend)  
- Reverse proxy setup using Nginx  
- Login system with modern UI  
- Dashboard showing system status  
- Scalable and modular design  

---

## 📁 Project Structure

devops-ansible-aws-project/ │ ├── frontend.yml          # Installs Nginx & deploys UI ├── backend.yml           # Installs Node.js & runs backend ├── frontend-proxy.yml    # Configures reverse proxy ├── hosts.ini             # Inventory file (server details) ├── README.md             # Project documentation

---

## 🔑 Login Credentials

Username: admin Password: 1234

---

## 🚀 How to Run the Project

### 1️⃣ Connect to Control Node
bash ssh -i ansible-key.pem ubuntu@<CONTROL_NODE_IP> 

---

### 2️⃣ Check Connectivity
bash ansible -i hosts.ini all -m ping -u ubuntu --private-key=ansible-key.pem 

---

### 3️⃣ Deploy Frontend
bash ansible-playbook -i hosts.ini frontend.yml --private-key=ansible-key.pem -u ubuntu 

---

### 4️⃣ Deploy Backend
bash ansible-playbook -i hosts.ini backend.yml --private-key=ansible-key.pem -u ubuntu 

---

### 5️⃣ Configure Reverse Proxy
bash ansible-playbook -i hosts.ini frontend-proxy.yml --private-key=ansible-key.pem -u ubuntu 

---

### 6️⃣ Access Application
Open in browser:
http://<FRONTEND_PUBLIC_IP>

---

## 🔄 Working Flow

1. User accesses the frontend via browser  
2. Nginx serves the UI  
3. Login request is sent to backend via reverse proxy  
4. Backend validates credentials  
5. Dashboard is displayed with system status  

---

## 📊 Output

- Modern login UI  
- Dashboard displaying:
  - Frontend status  
  - Backend status  
- Fully automated deployment  

---

## 🧠 DevOps Concepts Used

- Infrastructure as Code (Ansible Playbooks)  
- Configuration Management  
- Multi-Tier Architecture  
- Reverse Proxy  
- Automation  

---

## ⚠️ Common Issues & Fix

| Issue | Solution |
|------|--------|
| Permission denied | chmod 400 ansible-key.pem |
| SSH connection failed | Check security group |
| Backend not working | Re-run backend.yml |
| UI not loading | Re-run frontend.yml |
| API not responding | Check proxy configuration |

---

## 🔗 GitHub Repository

👉 https://github.com/Devviratt/devops-ansible-aws-project

---

## 🌐 Live Demo

👉 http://3.110.182.4  

(Hosted on AWS EC2)

---

## 📸 Output Screenshot

Add your screenshot here

![Dashboard](screenshot.png)

---

## 🔮 Future Improvements

- Load balancing with multiple backend servers  
- Docker containerization  
- Kubernetes deployment  
- Monitoring with CloudWatch  
- CI/CD pipeline integration  

---

## 🎤 Final Statement

> This project demonstrates how DevOps tools like Ansible can automate cloud infrastructure deployment and create a scalable multi-tier architecture on AWS.

---
