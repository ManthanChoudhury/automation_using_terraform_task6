# automation_using_terraform_task6
Deploy the WordPress application on Kubernetes and RDS for Storage | AWS | Terraform

## Use_Case:-

1.  Write an Infrastructure as code using terraform, which automatically deploy the Wordpress application.

2.  On AWS, use RDS service for the relational database for Wordpress application.

3. Deploy the Wordpress as a container either on top of Minikube or EKS or Fargate service on AWS

4. The Wordpress application should be accessible from the public world if deployed on AWS or through workstation if deployed on Minikube.

## Task Description:

I have written Infrastructure as code using terraform, which automatically deploy the Wordpress application. On AWS, I have used RDS service for the relational database for Wordpress application. Then I deployed the Wordpress as a container on top of Minikube, the Wordpress application is accessible to the public world.

## Pre-requisite:
1) AWS account
   
2) Minikube (Kubernetes) installed:
           https://kubernetes.io/docs/tasks/tools/install-minikube/

3) Terraform installed:
           https://learn.hashicorp.com/tutorials/terraform/install-cli
      
      

## Kubernetes

Kubernetes is a portable, extensible, open-source platform for managing containerized workloads and services, that facilitates both declarative configuration and automation.
Kubernetes is an open-source container-orchestration system for automating computer application deployment, scaling, and management. It was originally designed by Google and is now maintained by the Cloud Native Computing Foundation.



A Kubernetes cluster is a set of node machines for running containerized applications. If you’re running Kubernetes, you’re running a cluster. At a minimum, a cluster contains a control plane and one or more compute machines, or nodes. The control plane is responsible for maintaining the desired state of the cluster, such as which applications are running and which container images they use. Nodes actually run the applications and workloads.

For this task, I'll use Minikube, a tool that runs a single-node Kubernetes cluster in a virtual machine on your personal computer.
