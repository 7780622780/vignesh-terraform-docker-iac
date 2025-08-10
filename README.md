🚀 Terraform Docker Container - Task 3 (DevOps Internship)
📌 Objective
Provision a local Docker container using Terraform to demonstrate Infrastructure as Code (IaC) concepts.

🛠 Tools Used
Terraform → For provisioning infrastructure

Docker → For running the container locally

📂 Project Structure
bash
Copy
Edit
terraform-docker-container/
├─ main.tf              # Terraform configuration file
├─ .gitignore           # Ignore state files & other unnecessary files
├─ logs/                # Command execution logs (optional)
└─ README.md            # Project documentation

📋 Steps to Run
1️⃣ Prerequisites
Install Docker Desktop and make sure it's running.

Install Terraform.

Ensure both are accessible from the terminal:

bash
Copy
Edit
docker --version
terraform -v
2️⃣ Initialize Terraform
bash
Copy
Edit
terraform init
This downloads the Docker provider plugin.

3️⃣ Preview Changes
bash
Copy
Edit
terraform plan
Shows the resources Terraform will create.

4️⃣ Apply Configuration
bash
Copy
Edit
terraform apply
Type yes when prompted.
This will:

Pull the nginx:latest image

Create a container named my-nginx-container

Map host port 8080 to container port 80

5️⃣ Verify
Check running containers:

bash
Copy
Edit
docker ps
Visit:
http://localhost:8080 → You should see the NGINX welcome page.

6️⃣ Destroy Resources
bash
Copy
Edit
terraform destroy
Type yes to confirm.

📷 Screenshots (Examples)
terraform apply output in terminal

docker ps showing the container running

Browser showing NGINX welcome page

terraform destroy output

📜 Notes
.gitignore is configured to avoid committing terraform.tfstate, .terraform/ folder, and any sensitive files.

Logs are stored in the logs/ folder for reference.

This project is for learning purposes only.

📚 Concepts Learned
Basics of Infrastructure as Code (IaC)

Using Terraform providers

Managing local Docker containers via Terraform

Understanding Terraform state, plan, apply, and destroy commands