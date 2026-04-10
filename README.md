☁️ AWS EC2 Web Server Deployment & Security Hardening Lab
📌 Project Overview

This project demonstrates the deployment of a web server on an Amazon EC2 instance, followed by intentional security misconfiguration and remediation. The goal is to simulate a real-world cloud environment, identify security risks in network access controls, and apply least-privilege principles to harden the system.

🎯 Objectives
* Launch and configure an EC2 instance
* Deploy a basic Apache web server
* Configure security groups for controlled access
* Simulate a security misconfiguration
* Identify associated risks
* Apply remediation using least-privilege access controls

🛠️ Technologies Used
* AWS EC2
* Amazon Linux 2
* Apache Web Server (httpd)
* AWS Security Groups
* SSH (Secure Shell)

.....

# ☁️ Secure Cloud Environment Lab (AWS EC2)

## 📌 Project Overview

Built and secured a cloud-based virtual server using AWS EC2.
This project demonstrates basic cloud deployment, network configuration, and security hardening.

---

## 🎯 Objectives

* Launch virtual server (EC2 instance)
* Configure network access (using security groups)
* Connect securely via SSH
* Fixed security misconfigurations from errors in initial setup
* Document and verify system functionality

---

## 🧱 Architecture

* **Cloud Provider:** AWS
* **Service:** EC2 (Elastic Compute Cloud)
* **OS:** Amazon Linux 2023
* **Access Method:** SSH (Port 22)
* **Public Access:** using Public IPv4

---

## ⚙️ Steps Performed

### 1. EC2 Setup  

* Created EC2 instance (t3.micro)
* Selected Amazon Linux 2023 AMI
* Generated key pair (.pem file)

### 2. Network Configuration

* Allowed SSH access (Port 22)
* Initially allowed broad access (for testing)
* Verified public IP assignment

### 3. SSH Connection

* Connected using terminal:

```bash
ssh -i TestKeyPair.pem ec2-user@54.204.131.244>
```

### 4. System Verification

* Confirmed successful login
* Executed basic Linux commands (`ls`, `pwd`)

### 5. Security Hardening

* Identified overly permissive security group rules
* Restricted SSH access to **My IP only**
* Removed unnecessary open ports

---

## 5. 🔐 Security Concepts Demonstrated

* Principle of Least Privilege
* Secure Remote Access (SSH)
* Network Access Control (Security Groups)
* Cloud Security Best Practices

---

## 📸 Screenshots

![EC2 Instance Running](EC2-Instance-Running.png)

![SG-Restricted](SG-Restricted.png)

![SG-PublicAccess](SG-PublicAccess.png)

![Successful SSH Connection](Successful%20SSH%20Connection.png)


---

## 🧠 Key Takeaways

* Learned how to deploy and access cloud infrastructure
* Understood importance of restricting network access
* Gained hands-on experience with AWS security controls

---

## 🚀 Next Steps

* Install and configure a web server (HTTP/HTTPS)
* Simulate and fix additional vulnerabilities
* Implement logging and monitoring (CloudTrail)

---

## 📁 Repository Structure

* README.md → Project documentation
* /screenshots → Supporting images
* /notes → Commands and configuration details

---
