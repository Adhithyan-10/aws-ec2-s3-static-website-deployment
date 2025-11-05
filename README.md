<h1 align="center" style="color:#2F80ED;">🌐 Web Application Deployment on AWS (EC2 + S3)</h1>

This project demonstrates deploying a static web application on **Amazon EC2** while storing image assets in **Amazon S3**. The deployment showcases core cloud configuration concepts including compute provisioning, object storage access, IAM role-based authorization, and network access management through security groups.

---

<h2 style="color:#2F80ED;">📌 Project Overview</h2>

An Ubuntu-based EC2 instance was configured to run a Node.js server which delivers the application's webpage. Images displayed on the site were uploaded to S3 buckets and accessed via public object URLs. Secure authorization was ensured using an IAM role attached to the EC2 instance. Security Group rules were configured to allow inbound HTTP traffic on port 80. This project replicates a practical cloud-hosted deployment scenario and builds experience with real operational workflows.

---

<h2 style="color:#2F80ED;">🏗 Architecture</h2>

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
                       |  Retrieves Image Assets
                       |
            +----------v-----------+
            |      S3 BUCKETS      |
            | (Public Image Files) |
            +----------------------+


---

<h2 style="color:#2F80ED;">🧰 AWS Services Used</h2>

| Service | Role |
|--------|------|
| **Amazon EC2** | Hosted the web application |
| **Amazon S3** | Stored static image assets |
| **IAM Role / Policies** | Enabled secure access without stored credentials |
| **Security Groups** | Controlled inbound HTTP traffic |
| **VPC Networking** | Provided cloud network environment |

---

### 📂 Repository Structure

| File / Folder Name                     | Description                                      |
|----------------------------------------|--------------------------------------------------|
| `app.js`                               | Node.js backend server to host static webpage.   |
| `completion.html`                      | Main HTML page displayed to users.               |
| `README.md`                            | Project documentation with deployment steps.     |
| `Adhithyan_AWS_Project_Report.pdf`     | Full project report with screenshots.            |



## Deployment Steps Performed
1. Launched Ubuntu EC2 instance (t2.micro – Free Tier).
2. Installed Node.js and uploaded required files.
3. Created separate S3 buckets and uploaded images.
4. Disabled *Block Public Access* for buckets.
5. Applied bucket policy to allow object-level public read access.
6. Updated `completion.html` to reference the S3 object URLs.
7. Configured EC2 Security Group to allow inbound HTTP (Port 80).
8. Started the web application:
   sudo node app.js


---

<h2 style="color:#2F80ED;">✅ Result</h2>

- Web application hosted successfully on EC2.
- Image assets loaded from S3 using public URLs.
- Application accessed from browser using:
-   http://13.126.27.91



---

<h2 style="color:#2F80ED;">🎯 Skills Demonstrated</h2>

- Cloud Deployment & Server Configuration
- Linux Command-line Administration
- S3 Object Storage Management
- IAM Role & Policy Permissions
- Security Group Network Configuration
- Node.js Application Hosting

---

<h2 align="center" style="color:#2F80ED;">👨‍💻 Author</h2>

<p align="center">
<b>Adhithyan Sivaraman T</b><br>
Cloud & DevOps Learner<br>
GitHub: <a href="https://github.com/Adhithyan-10">github.com/Adhithyan-10</a><br>
LinkedIn: www.linkedin.com/in/adhithyan-sivaraman-t-399b5b362
</p>
