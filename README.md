# Assignment 3.11

# Create ECS cluster with Fargate to deploy NGINX web application into AWS using Terraform Code and Github Actions.

Terraform Code will perform creation of below resources.
1. Create ECS Cluster
2. Create Task Definition, this is a json file contain all configuration.
3. Create ECS Service to deploy task definition with an application load balancer
4. Final, view the NGINX web application using public ip address and DNS name.

# Github Actions worksflow : ecs_create.yml
This worksflow will perform following tasks when git push is trigger.

- Terraform create - Apply all terraform code to create ecs cluster, ecs task definition, ecs service and application load balancer.
- Terraform wait - A waiting times of 4 minutes to check the ecs status in AWS and view the NGINX web application using IP address or DNS name.
- Terraform destroy - This will do the clean up process where all the resources created will destroy.
