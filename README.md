# 🚀 Deploying a Node.js Application on AWS EC2

This project demonstrates how to deploy a **Node.js web application** on an **AWS EC2 instance**, configure **Security Groups**, and expose the application to the internet using a **custom TCP port (3000)**.

This project is designed from a **cloud & placement perspective**, focusing on core AWS concepts such as EC2, security groups, SSH access, and Linux-based deployments.

---

## 📌 Project Overview

- Launch an **EC2 instance** with a new key pair
- Configure **inbound rules** in a security group
- Connect to EC2 securely using **SSH**
- Install **Node.js and Git** on the server
- Clone and run a Node.js application
- Access the application using **public IPv4 address**

---

## 🧰 Tech Stack & Services Used

- **AWS EC2 (Amazon Elastic Compute Cloud)**
- **Amazon Linux 2**
- **Security Groups**
- **SSH**
- **Node.js (v18)**
- **Git**
- **Linux (yum package manager)**

---

# 🎯 Key Learnings 
Hands-on experience with AWS EC2
Understanding of cloud networking & security groups
Real-world Node.js deployment
Linux server administration basics
End-to-end cloud application hosting

---

## 🧠 Concepts & AWS Topics Covered

- EC2 instance lifecycle
- Key pair–based authentication
- Security group inbound rules
- Custom TCP ports
- Public IPv4 addressing
- Linux server setup
- Application deployment on cloud VM

---

# project architecture is:
User (Browser)
     |
     | HTTP :3000
     v
Internet
     |
     v
AWS Security Group
(Allow 3000, 80, 443)
     |
     v
EC2 Instance (Amazon Linux 2)
     |
     v
Node.js Application (app.js)

---

## ⚙️ EC2 & Security Group Configuration

### EC2 Setup
- Instance Type: `t2.micro` (Free Tier eligible)
- Key Pair: Newly created `.pem` key
- OS: Amazon Linux 2

### Security Group – Inbound Rules

| Type        | Protocol | Port | Source    |
|------------|----------|------|-----------|
| SSH        | TCP      | 22   | My IP     |
| HTTP       | TCP      | 80   | Anywhere  |
| HTTPS     | TCP      | 443  | Anywhere  |
| Custom TCP| TCP      | 3000 | Anywhere  |

> Port **3000** is required to expose the Node.js application.

---

## 🔐 Connect to EC2 Instance (Mac Terminal)

Navigate to the folder where the key pair is downloaded:

```bash
cd ~/Downloads
```
# Set secure permissions for the key file:

```bash
chmod 400 new-key.pem
```
# Connect to the EC2 instance using SSH:

```bash
ssh -i new-key.pem ec2-user@<EC2_PUBLIC_IPV4>
```

# 🛠️ Server Setup on EC2
Update the system packages:

```bash
sudo yum update -y
```
Install Node.js (v18):
```bash
curl -fsSL https://rpm.nodesource.com/setup_18.x | sudo bash -
sudo yum install -y nodejs
```
Install Git:
```bash
sudo yum install git -y
```
# 📦 Clone & Run the Application
Clone the GitHub repository:

```bash
git clone https://github.com/SairajPatil15/EC2-Deploy.git
cd EC2-Deploy
```
Install dependencies:
```bash
npm install
```
Start the application:

```bash
node app.js
```
# 🌐 Access the Application
Open your browser and visit:

```bash
http://<EC2_PUBLIC_IPV4>:3000
```
If the security group is configured correctly, the application will be accessible publicly.

👨‍💻 Author


Sairaj Patil


AWS Cloud & DevOps Enthusiast





