# 🖥️ Amazon EC2 (Elastic Compute Cloud)

## 📘 Overview

Amazon EC2 is a **core AWS service** that allows you to rent **virtual servers (instances)** in the cloud. These servers can run applications, host websites, or be used for development/testing.

---

## 🎯 Key Features

- **Elastic**: Quickly scale up or down based on your need.
- **Pay-as-you-go**: Pay only for the compute time you use.
- **Secure**: Integrated with IAM and Security Groups.
- **Customizable**: Choose OS, storage, instance type, networking, and more.

---

## 🧩 Key Concepts

| Term              | Description |
|-------------------|-------------|
| **AMI**           | Amazon Machine Image – Pre-configured OS (like Ubuntu, Windows) |
| **Instance Type** | Defines CPU, memory, network (e.g., `t2.micro`, `t3.large`) |
| **Key Pair**      | Used for SSH (secure login into instance) |
| **Security Group**| Acts as a virtual firewall to allow/deny access |
| **Elastic IP**    | A static IP address you can attach to your instance |
| **User Data**     | Scripts that run at the first boot (for automation) |

---

## 🧪 Hands-On: Launching an EC2 Instance

### Step-by-Step Guide (Free Tier)

1. **Login** to [AWS Console](https://console.aws.amazon.com/)
2. Go to **EC2 Dashboard**
3. Click **Launch Instance**
4. Fill in:
   - **Name**: `MyFirstEC2`
   - **AMI**: Choose `Ubuntu` or `Amazon Linux`
   - **Instance Type**: `t2.micro` (Free Tier)
   - **Key Pair**: Create new or use existing
   - **Network Settings**:
     - Allow **SSH (port 22)**
     - Optionally allow **HTTP (port 80)** for web access
   - **Storage**: Default 8GB is fine
5. Click **Launch Instance**
6. Wait till instance state = `Running`

---

## 🔑 SSH Access to EC2 (Linux/Mac/WSL)

```bash
# Move to folder where .pem file is downloaded
cd ~/Downloads

# Change permission
chmod 400 your-key.pem

# Connect to instance
ssh -i "your-key.pem" ubuntu@<Public-IP>
