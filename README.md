# AWS EC2 NGINX Web Server Deployment

## Project Overview

This project demonstrates deploying a web server using AWS EC2 and NGINX. A custom HTML webpage was hosted publicly using an Amazon Linux EC2 instance.

---

## Services Used

* AWS EC2
* VPC
* Security Groups
* NGINX
* Linux Commands

---

## Architecture

User → EC2 Instance → NGINX Web Server → Custom Website

---

## Steps Performed

### 1. Created EC2 Instance

* Launched Amazon Linux EC2 instance
* Allowed HTTP and SSH traffic

### 2. Connected to EC2

Used SSH to connect to the instance.

```bash
ssh -i key.pem ec2-user@public-ip
```

### 3. Installed NGINX

```bash
sudo yum update -y
sudo yum install nginx -y
```

### 4. Started NGINX

```bash
sudo systemctl start nginx
sudo systemctl enable nginx
```

### 5. Created Custom Webpage

```html
<!DOCTYPE html>
<html>
<head>
<title>Mahesh AWS Project</title>
</head>

<body>
<h1>Mahesh AWS NGINX Project</h1>
<p>Hosted on AWS EC2 using NGINX Web Server</p>
</body>

</html>
```

### 6. Hosted Website Publicly

Accessed the website using the EC2 public IP.

---

## Screenshots

* EC2 Instance Running
* Security Group Configuration
* NGINX Installation
* Website Output

---

## Challenges Faced

* SSH connectivity issues
* Security group configuration
* Understanding NGINX web hosting

---

## Outcome

Successfully deployed a public web server using AWS EC2 and NGINX.
