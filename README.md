# Web Application Deployment on AWS using EC2 and S3

This project demonstrates the deployment of a static web application in the AWS cloud environment. The application is hosted on an Amazon EC2 instance, while image assets are stored and publicly served through Amazon S3. The project focuses on compute resource provisioning, object storage management, identity and access configuration, and secure network-level access control.

## Project Overview
An Ubuntu-based EC2 instance was configured to run a Node.js web server that renders the application frontend. Multiple S3 buckets were created to store image files, which were accessed using publicly available S3 object URLs. IAM Roles were used to allow secure communication between EC2 and S3 without the need to embed credential keys in the application. Security Groups were configured to allow HTTP (port 80) traffic to ensure public access to the hosted site. This project replicates real-world cloud deployment and highlights practical cloud operational workflows.

## Architecture Diagram

                +----------------------+
                |        USER          |
                +----------+-----------+
                           |
                           |  HTTP Request (Port 80)
                           |
                +----------v-----------+
                |     EC2 INSTANCE     |
                |  (Node.js Web App)   |
                +----------+-----------+
                           |
                           |  Requests Image Assets
                           |
                +----------v-----------+
                |      S3 BUCKETS      |
                | (Public Image Files) |
                +----------------------+

## AWS Services Used
- Amazon EC2: Virtual machine hosting the web server
- Amazon S3: Storage service containing static web assets
- IAM Role and Policies: Secure resource access control mechanism
- Security Groups: Network traffic filtering and inbound access control
- VPC Networking: Underlying network infrastructure

## Repository Structure
aws-ec2-s3-static-website-deployment/
│
├── app.js                           (Node.js server handling requests)
├── completion.html                  (Webpage content presented to the user)
├── README.md                        (This documentation)
└── Adhithyan_AWS_Project_Report.pdf (Full step-by-step report with screenshots)

## Deployment Steps

1. Launched an Ubuntu EC2 instance (t2.micro, Free Tier eligible).
2. Connected to the instance using EC2 Instance Connect.
3. Installed Node.js and transferred application files.
4. Created S3 buckets and uploaded image assets.
5. Disabled "Block Public Access" for required buckets.
6. Applied S3 bucket policies to enable object-level public read access.
7. Updated `completion.html` to reference S3 public object URLs.
8. Configured EC2 Security Group to allow inbound HTTP (Port 80) access.
9. Started the application using:
   sudo node app.js

## Result
The web application was successfully hosted and made accessible over the internet using the EC2 Public IP address. Image content was retrieved directly from S3 and displayed within the webpage.

Example Access Pattern:
http://<EC2_Public_IP>

## Skills Demonstrated
- AWS Compute and Storage Configuration
- Linux Server Setup and Package Management
- S3 Object Storage Hosting and Access Policy Configuration
- IAM Role and Identity-Based Access Control
- Network-Level Access Control using Security Groups
- Node.js Application Hosting in Cloud Environment

## Author
ADHITHYAN SIVARAMAN T
Cloud and DevOps Learner
GitHub: https://github.com/Adhithyan-10
LinkedIn: www.linkedin.com/in/adhithyan-sivaraman-t-399b5b362
