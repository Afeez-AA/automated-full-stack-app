# Automated Deployment of Application and Monitoring Stack  

This project automates the provisioning of cloud infrastructure and the deployment of an application stack along with a monitoring solution. It leverages **Terraform** for infrastructure provisioning and **Ansible** for configuration management, application deployment, and monitoring setup.  

## Features  
- **Infrastructure as Code (IaC)**: Provision cloud infrastructure using Terraform.  
- **Application Deployment**: Automate the deployment of pre-built application images using Ansible roles.  
- **Monitoring Setup**: Deploy a monitoring stack alongside the application stack.  
- **Load Balancer Configuration**: Set up Traefik/Nginx for routing and load balancing.  
- **End-to-End Automation**: Trigger all tasks with a single `terraform apply -auto-approve` command.  

## Tools and Technologies  
- **Terraform**: For provisioning infrastructure and generating dynamic Ansible inventories.  
- **Ansible**: For server configuration, application deployment, and monitoring setup.  
- **Docker Hub**: For storing pre-built application images.  
- **Traefik/Nginx**: For application routing and load balancing.  

## How It Works  
1. **Infrastructure Provisioning**:  
   - Use Terraform to provision servers and networking resources in the cloud.  
   - Automatically generate Ansible inventories based on Terraform outputs.  

2. **Application Deployment**:  
   - Pre-build application images and push them to Docker Hub.  
   - Use Ansible roles to pull and deploy the images on provisioned servers.  

3. **Monitoring Stack Setup**:  
   - Configure monitoring tools for observing application health and system performance.  

4. **Automation**:  
   - Run `terraform apply -auto-approve` to provision infrastructure, configure servers, deploy the application, and set up monitoring in a single step.  

## Prerequisites  
- Terraform installed locally.  
- Ansible installed locally.  
- Docker Hub account with application images pre-built and pushed.  

## Usage  
1. Clone this repository:  
   ```bash  
   git clone <repository-url>  
   cd <repository-folder>  
   ```  

2. Initialize Terraform:  
   ```bash  
   terraform init  
   ```  

3. Apply Terraform configurations:  
   ```bash  
   terraform apply -auto-approve  
   ```  

4. Verify the deployment:  
   - Check the application URL via Traefik/Nginx.  
   - Verify monitoring metrics for system health.  
