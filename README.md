# Terraform AWS Infrastructure
As part of the NTI DevOps and Automation Initiative course, this repository contains the Terraform code for establishing a scalable and robust infrastructure in AWS. The architecture consists of load balancers, application servers, Auto Scaling Groups (ASGs), and a Virtual Private Cloud (VPC) with numerous subnets dispersed among various Availability Zones (AZs).

## Features

    Modular Architecture: Terraform modules are used in the infrastructure's design to facilitate code reuse and maintenance.
    High Availability: To guarantee fault tolerance and high availability, resources are spread across several AZs.
    Two types of subnets are utilized: public subnets are used for resources that need to be accessed directly from the internet, and private subnets are used for resources that are used internally.
    Auto Scaling: To ensure best performance and cost efficiency, Auto Scaling Groups are utilized to automatically modify the number of instances based on traffic demand.
    Load balancing: To improve scalability and availability, traffic is distributed among instances using both internal and external load balancers.
    Reverse Proxy settings: To direct incoming requests to the correct backend services, Nginx is installed with reverse proxy settings on public instances.
    Internal Load Balancer: To provide secure communication within the VPC, traffic is sent to the private instances via an internal load balancer.
## Usage

Take the following actions to deploy the infrastructure:

    Required conditions: Make sure your local machine has Terraform installed.
    Clone the Repository: Copy the contents of this repository to your desktop.
    Start Terraform: To start the Terraform configuration, run terraform init.
    Configure Variables: Add your AWS credentials and any other necessary variables to the terraform.tfvars file.
    Deploy Infrastructure: To deploy the infrastructure to AWS, run Terraform apply.

