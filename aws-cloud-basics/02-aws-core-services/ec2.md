# 🖥 Amazon EC2 (Elastic Compute Cloud)

EC2 allows you to launch virtual servers in the cloud.

## Key Concepts:
- **Instance Types**: t2.micro (Free tier eligible)
- **AMI**: Amazon Machine Image (OS templates)
- **Security Groups**: Virtual firewall
- **Key Pair**: Secure login using SSH

## Hands-On:
1. Go to AWS Console → EC2 → Launch Instance
2. Choose Ubuntu AMI
3. Select t2.micro
4. Add Storage (default is fine)
5. Add Security Group: Allow SSH (port 22)
6. Launch and connect via SSH
