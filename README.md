# Super Mario Project  
This project showcases the deployment of a Kubernetes cluster on AWS EKS (Elastic Kubernetes Service) using Terraform for infrastructure provisioning. The cluster is hosted on AWS EC2 instances, managed through Terraform configurations.


## Table of Contents

- [Installation](#installation)
  - [Prerequisites](#prerequisites)
  - [Installation Steps](#installation-steps)
- [Usage](#usage)
- [Features](#features)
- [Contributing](#contributing)
- [Testing](#testing)
- [License](#license)
- [Contact](#contact)

## Installation

### Prerequisites
- AWS Account
- Basic AWS
- Basic Terraform

### Installation Steps

1. Login to AWS Console:  
   [AWS Console](https://signin.aws.amazon.com/signin?redirect_uri=https%3A%2F%2Fconsole.aws.amazon.com%2Fconsole%2Fhome%3FhashArgs%3D%2523%26isauthcode%3Dtrue%26nc2%3Dh_ct%26oauthStart%3D1721572611104%26src%3Dheader-signin%26state%3DhashArgsFromTB_eu-north-1_12611e03d90dac77&client_id=arn%3Aaws%3Asignin%3A%3A%3Aconsole%2Fcanvas&forceMobileApp=0&code_challenge=D4Ktb8P_0xWesTfL03ap7mBUCoqtJPd26-VeacA0aJw&code_challenge_method=SHA-256)

2. Launch EC2 Instance:  
3. Lets get Root and Update: 
   
      ```bash
         sudo su
         apt update -y
         sudo apt install wget -y
         sudo apt install curl -y
4. Lets Install Docker:
   ```bash
   apt install docker.io
   usermod -aG docker $USER # Replace with your username e.g ‘ubuntu’
   newgrp docker

5. Terraform SetUp:
   ```bash
   wget -O- https://apt.releases.hashicorp.com/gpg | sudo gpg --dearmor -o /usr/share/keyrings/hashicorp-archive-keyring.gpg
   echo "deb [signed-by=/usr/share/keyrings/hashicorp-archive-keyring.gpg] https://apt.releases.hashicorp.com $(lsb_release -cs) main" | sudo tee /etc/apt/sources.list.d/hashicorp.list
   sudo apt update && sudo apt install terraform

6. Setup AWS cli:
   ```bash
   curl "https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip" -o "awscliv2.zip"
   unzip awscliv2.zip
   sudo ./aws/install

7. Kubectl Setup:
   ```bash
   curl -LO https://dl.k8s.io/release/$(curl -L -s https://dl.k8s.io/release/stable.txt)/bin/linux/amd64/kubectl
   sudo install -o root -g root -m 0755 kubectl /usr/local/bin/kubectl

8. Creating and Attaching IAM role to EC2 instance
9. Building the INFRA:  
    a. Connect to the EC2 Instance  
    b. Get root and create a new Directory "SuperMario"  
    ```bash
    sudo su
    mkdir SuperMario
    cd SuperMario

    ```
    c. Clone the Git Repo
   ```bash
   git clone https://github.com/Cyber-Cloud-Pro/SuperMarioProject.git
   ```
   d.  Change Dir to SuperMarioProject
   ```bash
   cd SuperMarioProject
   ```
   




