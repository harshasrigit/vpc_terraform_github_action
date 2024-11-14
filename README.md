# VPC_Terraform_Github_Action
Link: https://www.youtube.com/watch?v=v4MP7fvLw44
https://www.notion.so/DevOps-Project-Mastering-VPC-Creation-with-Terraform-GitHub-Actions-Automation-13598ddfef5480d9bd55c16c5fd17661?pvs=4



Creating VPC Iaac and github Action as CICD

![Alt text](image/projectfow.png)
![Alt text](image/image.png)
creating a Virtual Private Cloud (VPC) infrastructure using Terraform and then automating the deployment of  Terraform code using GitHub Actions.


1. Setting up Terraform:  initial setup of Terraform on your local machine

    To add an interactive guide to your README file for setting up VPC infrastructure using Terraform, here’s a structured way to include the steps you mentioned. You can break it down into clear, actionable steps for users to follow:

---

# Writing Terraform Code: VPC Infrastructure

Follow these steps to get started with deploying VPC infrastructure using Terraform.

### Prerequisites

Before you start, ensure that the following tools are installed on your Windows machine:

1. **Install Git Bash**  
   Git Bash is an essential tool for running shell commands on Windows. If you haven’t installed it yet, follow these steps:  
   - Download Git Bash from the official site: [Git for Windows](https://git-scm.com/)
   - Run the installer and follow the prompts to install.

2. **Install Terraform**  
   Terraform is a powerful Infrastructure as Code (IaC) tool used to define and provision infrastructure.  
   - Download the Terraform binary for Windows: [Terraform Downloads](https://www.terraform.io/downloads.html)
   - Extract the downloaded ZIP file to a directory of your choice (e.g., `C:\Terraform`).
   - Add the directory to your `PATH` environment variable to make Terraform accessible globally from the command line.

3. **Install AWS CLI**  
   To manage your AWS infrastructure, you'll need the AWS Command Line Interface (CLI).  
   - Download and install the AWS CLI for Windows: [AWS CLI Setup](https://docs.aws.amazon.com/cli/latest/userguide/install-cliv2-windows.html)
   - After installation, configure the AWS CLI with your credentials by running:  
     ```bash
     aws configure
     ```
   - Provide your AWS Access Key, Secret Key, region, and output format when prompted.

### Terraform VPC Infrastructure Example

Once you've completed the setup, you can begin writing Terraform code to create a VPC.

```hcl
provider "aws" {
  region = "us-west-2"  # Update to your desired AWS region
}

resource "aws_vpc" "main_vpc" {
  cidr_block = "10.0.0.0/16"
  enable_dns_support = true
  enable_dns_hostnames = true

  tags = {
    Name = "main-vpc"
  }
}
```

### Next Steps
1. **Initialize Terraform**  
   In your project directory, run:
   ```bash
   terraform init
   ```

2. **Plan the Deployment**  
   To check what will be created:
   ```bash
   terraform plan
   ```

3. **Apply the Configuration**  
   Deploy the VPC to AWS:
   ```bash
   terraform apply
   ```

That's it! You’ve successfully created your VPC using Terraform.

---

This structure makes it easy for users to follow along with the setup process. You can also add links to relevant documentation if necessary.
    
2. Writing Terraform Code:  VPC infrastructure

       a.  installed git bash 
       b.  installed terraform to windows 
       c.  installed aws cli
   
      a.   networks
      b.   subnets
      c.   security groups

4. Initializing and Applying Terraform:
   
5. GitHub Repository Setup:setting up a GitHub repository to store

     a.   Terraform code
     b.   README
     c.   .gitignore
     d.   essential files.
   
6. GitHub Actions Configuration: configure GitHub Actions workflows to automate the deployment of your Terraform code.

    a.   secrets management and workflow triggers on pushing the code to a specific branch.
    
7. Push to GitHub: See how to push  Terraform code to GitHub repository and trigger the GitHub Actions workflow.

8. Monitor and Verify: Learn how to monitor the progress of your GitHub Actions workflow and verify the successful deployment of  VPC infrastructure.

