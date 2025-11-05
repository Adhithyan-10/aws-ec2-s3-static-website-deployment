<h1 align="center">🚀 AWS EC2 + S3 Static Website Deployment</h1>

<p align="center">
Deploying a cloud-hosted web application using Amazon EC2, S3, IAM Roles and Security Groups.
<br>
Built as part of a cloud internship to gain real-world AWS deployment experience.
</p>

---

## 🌐 Project Overview

This project demonstrates the deployment of a static web application hosted on an **Amazon EC2** instance, while image assets are stored and delivered from **Amazon S3**.  
Secure access was configured using **IAM Roles**, and traffic control was managed via **Security Groups**.

The goal was to understand **real-world cloud application deployment workflows**, resource permissions, and web hosting fundamentals in AWS.

---

## 🏗️ Cloud Architecture Diagram

      ┌─────────────┐
      │   User      │
      └─────┬───────┘
            │ (HTTP Request)
            ▼
    ┌───────────────────┐
    │   EC2 Instance    │  ← Runs Node.js Web Server
    └─────┬─────────────┘
          │ (Fetches Images)
          ▼
   ┌───────────────────┐
   │  S3 Buckets       │  ← Hosts static image assets
   └───────────────────┘

---

## 🧠 Key AWS Services Used

| Service | Role in Project |
|--------|----------------|
| **EC2** | Hosted the web application (Node.js server) |
| **S3** | Stored and served image files publicly |
| **IAM Role** | Allowed EC2 to interact securely (no hardcoded credentials) |
| **Security Groups** | Controlled inbound HTTP traffic (port 80) |
| **VPC** | Provided networking environment |

---

## 📂 Repository Structure

aws-ec2-s3-static-website-deployment/
│
├── app.js # Node.js backend web server
├── completion.html # Web page content displayed to users
├── README.md # Documentation (this file)
└── Adhithyan_AWS_Project_Report.pdf # Detailed screenshots & workflow document


---

## ⚙️ Deployment Steps

1. **Launched an Ubuntu EC2 Instance** (t2.micro - Free Tier)
2. Connected via **EC2 Instance Connect**
3. Installed Node.js:
   ```bash
   sudo apt update
   sudo apt install nodejs npm -y
4.Created S3 buckets and uploaded images
5.Disabled Block Public Access for the bucket
6.Added S3 Bucket Policy to allow public object access
7.Updated completion.html to reference S3 public URLs
8.Allowed inbound HTTP traffic:
  Security Group → Inbound Rules → Add → Port 80 → 0.0.0.0/0
9.Started the server:
  sudo node app.js


✅ Final Result
---------------------------
Website successfully hosted on EC2
Images served directly from S3 over HTTP
Application accessible publicly via EC2 Public IP
  http://13.126.27.91

🎯 Skills Demonstrated
Skill	                          Level Gained
-----------------------------------------------------
Cloud Infrastructure Setup	    ✅ Hands-On
Linux Server Configuration	    ✅ Practical
S3 Public Hosting & Policies	  ✅ Applied
IAM Security Best Practices	    ✅ Understood
Node.js Server Deployment	      ✅ Implemented
Network & Port Security	        ✅ Configured


🧑‍💻 Author

ADHITHYAN SIVARAMAN T
Cloud & DevOps Enthusiast
B.Tech in Computer Science & Engineering
GitHub: https://github.com/Adhithyan-10
LinkedIn: www.linkedin.com/in/adhithyan-sivaraman-t-399b5b362


