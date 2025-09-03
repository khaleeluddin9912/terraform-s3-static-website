# Terraform S3 Static Website

This repository contains Infrastructure as Code (IaC) written in **Terraform** to deploy a static website on **AWS S3**.  
It automatically provisions:
- An **S3 bucket** for hosting
- **Bucket policy / ACLs** for public access
- **Website configuration** with index document
- Upload of `index.html` as the website entry point

---

## 🚀 Features
- Fully automated S3 static website hosting
- Randomized bucket name to avoid conflicts
- Public access enabled for hosting
- Terraform-managed infrastructure

---

## 📂 Project Structure
.
├── index.html # Example website file
├── main.tf # Terraform configuration
└── README.md # Documentation

yaml
Copy code

---

## 🛠 Prerequisites
- [Terraform](https://developer.hashicorp.com/terraform/downloads) v1.0+
- [AWS CLI](https://aws.amazon.com/cli/) configured with valid credentials  
  ```bash
  aws configure
An AWS account with permissions for S3

⚡ Usage
Clone the repo

bash
Copy code
git clone https://github.com/khaleeluddin9912/terraform-s3-static-website.git
cd terraform-s3-static-website
Initialize Terraform

bash
Copy code
terraform init
Preview the resources

bash
Copy code
terraform plan
Deploy the infrastructure

bash
Copy code
terraform apply -auto-approve
Get your website endpoint
After apply, run:

bash
Copy code
aws s3 ls
Or check the AWS Console → S3 → your bucket → Properties → Static website hosting.

🧹 Cleanup
To avoid unwanted AWS charges, destroy the resources when done:

bash
Copy code
terraform destroy -auto-approve
📌 Notes
Ensure that Block Public Access is disabled at the account/bucket level for website hosting.

This setup is meant for learning / portfolio projects. For production, use CloudFront + Route53 + ACM (HTTPS).

👨‍💻 Author
Khaleel Uddin

GitHub: @khaleeluddin9912
