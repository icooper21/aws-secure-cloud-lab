# ☁️ AWS EC2 Web Server Deployment & Security Hardening Lab

## 📌 Project Overview

This project demonstrates the deployment of a web server on an Amazon EC2 instance, followed by intentional security misconfiguration and remediation. The goal is to simulate a real-world cloud environment, identify security risks in network access controls, and apply least-privilege principles to harden the system.

---

## 🎯 Objectives
* Launch and configure an EC2 instance
* Deploy a basic Apache web server
* Configure security groups for controlled access
* Simulate a security misconfiguration
* Identify associated risks
* Apply remediation using least-privilege access controls

---

## 🛠️ Technologies Used
* AWS EC2
* Amazon Linux 2
* Apache Web Server (httpd)
* AWS Security Groups
* SSH (Secure Shell)

---

## 🚀 Deployment Steps
### 1. EC2 Instance Setup

* An EC2 instance was launched in AWS and configured with a public IPv4 address to allow external connectivity.

![EC2 Instance Running](EC2-Instance-Running.png)


### 2. Web Server Installation

* Apache web server was installed and started:

![Installation in Progress](Installation-Progress.png)


* Web Server Active and Running

![Successful Running](Successful-Running.png)


---

### 3. Security Group Configuration

Inbound rules were configured to allow:

* SSH (port 22) for remote administration
* HTTP (port 80) for web traffic

![SG Inbound1](SG-Inbound1.png)

Once configured, the default Apache test page (“It works!”) was successfully accessible via browser using the EC2 public IP.

Validated the EC2 instance was publicly accessible over HTTP (port 80) from an external network using a mobile device on cellular data.

![Public Access](ItWorks.png)


---

## ⚠️ Security Misconfiguration & Testing
### **Misconfiguration Introduced**

* SSH access was intentionally set to:
    - Source: 0.0.0.0/0

![Misconfiguration](SG-Inbound2.png)

* This allowed unrestricted SSH access from any IP address on the internet.

### **Risk Analysis**

This configuration introduces critical security risks:

* Exposure to brute-force SSH attacks
* Unauthorized login attempts from global sources
* Violation of least-privilege access principles

### **Validation**

* Public accessibility of the instance confirmed that external networks could reach the system under the misconfigured rule set.

---

## 🔐 Remediation & Hardening

To mitigate risk, SSH access was restricted to a trusted IP address:

* Source: 38.248.95.51/32   (My public IP)

![Remediation Rule](SG-Inbound3.png)

This ensures only authorized devices can initiate SSH connections.

---

## 📚 Key Learnings
*  Security Groups function as a virtual firewall for EC2 instances
*  0.0.0.0/0 represents unrestricted public internet access and should be avoided for administrative ports
*  Least-privilege access is critical in cloud security design
*  Misconfigurations in cloud environments can directly expose infrastructure to attack
*  Proper validation and remediation are essential parts of secure cloud operations

---

## 🧠 Conclusion

This lab demonstrated the full lifecycle of a cloud-hosted service: deployment, exposure, risk identification, and remediation. It reinforces foundational cloud security principles used in real-world AWS environments.

---
