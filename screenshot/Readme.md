# Node.js Calculator App on AWS EC2

This repository demonstrates the deployment of a Node.js Calculator application on an **Amazon EC2 instance**. The following steps show the complete process from EC2 creation to accessing the app via a web browser.

---

## 1. EC2 Instance Creation
Shows the initial configuration and creation of the Amazon EC2 instance within the AWS Management Console.

![EC2 create](01%20EC2%20create.png)

---

## 2. Security Group Configuration
Displays the Security Group settings, establishing the firewall rules for the instance.

![Security Group](02%20Security%20Group.png)

---

## 3. Inbound Rules
A detailed look at the specific inbound traffic rules (SSH, HTTP, and HTTPS) allowed to reach the server.

![Inbound Rules](03%20Inbound%20Rules.png)

---

## 4. SSH Login to EC2
Confirms a successful remote connection to the Amazon Linux 2023 instance via Terminal using SSH.

![SSH EC2 login](04%20SSH%20EC2%20login.png)

---

## 5. Node.js App Execution on EC2
Shows the application setup (`npm install`) and the Node.js server starting on **Port 3000**.

![Node.js app execution on EC2](05%20Node.js%20app%20execution%20on%20EC2.png)

---

## 6. Browser Output
The final verification showing the live Calculator app being accessed via a web browser.

![Browser output](06%20Browser%20output.png)

---
