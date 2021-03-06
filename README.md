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

## AWS RDS Amazon Relational Database Service (Amazon RDS) 

Amazon Relational Database Service (Amazon RDS) makes it easy to set up, operate, and scale a relational database in the cloud. It provides cost-efficient and resizable capacity while automating time-consuming administration tasks such as hardware provisioning, database setup, patching and backups. It frees you to focus on your applications so you can give them the fast performance, high availability, security, and compatibility they need. Amazon RDS is available on several database instance types - optimized for memory, performance, or I/O - and provides you with six familiar database engines to choose from, including Amazon Aurora, MySQL, Oracle Database, etc.
web service that makes it easier to set up, operate, and scale a relational database in the AWS Cloud. It provides cost-efficient, resizable capacity for an industry-standard relational database and manages common database administration tasks.

We'll configure our Wordpress app deployed on our Minikube cluster to use RDS as its Database.

Minikube is an open-source tool that helps to run Kubernetes on a local computer. Before using minikube we need to start it so here I wrote terraform code to start minikube on my Local Computer.

## Let’s start

1) It will launch the Wordpress Application.

# Wordpress.tf file:-

![Screenshot (5)](https://user-images.githubusercontent.com/45136716/91885297-2c95df80-eca5-11ea-8f4e-c9cc8eabf77d.png)


![Screenshot (6)](https://user-images.githubusercontent.com/45136716/91885302-2f90d000-eca5-11ea-876f-d76ffd8312f8.png)


2) It will create the RDS on top of AWS.

# databasesql.tf file:-

![Screenshot (7)](https://user-images.githubusercontent.com/45136716/91885305-31f32a00-eca5-11ea-9024-88878f5c3c50.png)


3) It will provide the IP to connect to Wordpress.

# main.tf files:-

![Screenshot (8)](https://user-images.githubusercontent.com/45136716/91885311-34558400-eca5-11ea-9854-9a64204982f6.png)

## After writing the terraform code. We have to run the command:

      terraform init 

      terraform apply --auto-approve
      
 ![9](https://user-images.githubusercontent.com/45136716/91885320-37507480-eca5-11ea-8273-d82ddfef72c2.png)
 
 
 If you get everything green then you are on the right track and everything works fine. Also, we have deployed WordPress as a container on the top of Minikube.
 
 ![10](https://user-images.githubusercontent.com/45136716/91885323-3881a180-eca5-11ea-8917-3a6bcb903220.png)
 
 Now to get the IP for WordPress. In the command line type:
      
      minikube ip
      
      minikube service list
      
      kubectl get all
      
      
![21](https://user-images.githubusercontent.com/45136716/91888102-59e48c80-eca9-11ea-9a71-59b7babc47bb.png)

      
Now Open minikube-nodes-ip:40000 and proceed with installation wizard:



![12](https://user-images.githubusercontent.com/45136716/91885331-3c152880-eca5-11ea-9741-83f4eba006d6.jpg)

![13](https://user-images.githubusercontent.com/45136716/91885336-3ddeec00-eca5-11ea-9007-18b1a3fa2b51.jpg)

![14](https://user-images.githubusercontent.com/45136716/91885339-3fa8af80-eca5-11ea-8f84-37256dae5e48.jpg)

![15](https://user-images.githubusercontent.com/45136716/91885348-42a3a000-eca5-11ea-963a-8569b0c55800.jpg)


# thanks alot for giving your time.


      

