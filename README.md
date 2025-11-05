# AWS EC2 and S3 Static Website Deployment

This project involves deploying a static web application on Amazon Web Services using an EC2 instance as the compute layer and S3 buckets for hosting static image assets. The project replicates a real-world cloud deployment workflow, where the frontend application is hosted on a cloud virtual machine and static resources are stored in object storage. The implementation focuses on building an understanding of cloud infrastructure setup, access policy configuration, networking control, and application hosting within a scalable cloud environment.

## Project Overview

The primary objective of this project was to gain practical experience with AWS services by deploying an application in a controlled and production-like environment. In this project, an Ubuntu-based EC2 instance was configured to run a Node.js web server that serves the application frontend. Multiple S3 buckets were used to store required image files, which were then accessed via publicly available object URLs. IAM role-based access control was implemented to ensure secure resource interactions without embedding credentials in the application. Network traffic flow was managed using Security Group rules to allow controlled HTTP access to the server. 

This project provides hands-on exposure to essential cloud computing concepts including virtualization, object storage management, identity and access control, and web hosting with publicly accessible endpoints. It demonstrates how different AWS services integrate to create a functional and scalable cloud-hosted application.

## Architecture

User Request → EC2 Web Server (Node.js) → Requests Image Assets → S3 Buckets

AWS Services Used:
- Amazon EC2 (Virtual server hosting the application)
- Amazon S3 (Object storage containing publicly served image files)
- IAM Role and Policies (For permission and access control)
- Security Groups (For network level access configuration)
- VPC Networking (Underlying cloud network structure)

## Repository Structure

aws-ec2-s3-static-website-deployment/
│
├── app.js                        # Node.js web server
├── completion.html               # Webpage displayed to the user
├── README.md                     # Project documentation
└── Adhithyan_AWS_Project_Report.pdf   # Detailed implementation report with screenshots

## Steps Performed

1. Launched an Ubuntu-based EC2 instance (t2.micro, Free Tier eligibility).
2. Installed Node.js runtime environment and uploaded the application files.
3. Created three Amazon S3 buckets and uploaded the project’s image assets.
4. Configured S3 bucket permissions by disabling "Block Public Access" and enabling controlled public read access.
5. Applied a bucket policy to allow object-level public access where required.
6. Updated the HTML file to reference S3 object URLs for embedded images.
7. Configured EC2 Security Group to allow inbound HTTP (port 80) traffic.
8. Started the application using:


## Result

- The web application was successfully hosted on the EC2 instance.
- Images were served directly from the S3 buckets through public object links.
- The application was accessible via the EC2 Public IP in a standard web browser.

## Skills Demonstrated

- AWS Compute and Storage Configuration
- Linux Server and Package Management
- S3 Object Hosting and Access Control
- IAM Role and Policy Configuration
- Network Security Implementation using Security Groups
- Hosting and Running a Node.js Application on Cloud Infrastructure

## Author

ADHITHYAN SIVARAMAN T  
Cloud & DevOps Enthusiast  
GitHub: https://github.com/Adhithyan-10  
LinkedIn: www.linkedin.com/in/adhithyan-sivaraman-t-399b5b362
