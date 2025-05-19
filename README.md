#  Kubernetes with Minikube on EC2

This project demonstrates how to build a single-node Kubernetes cluster using Minikube on an Ubuntu EC2 instance and deploy a containerized application (Nginx) using YAML manifests. It simulates real-world Kubernetes workflows such as application deployment, scaling, service exposure, and cluster inspection.

##  Tools Used

- Docker: Used as the container runtime
- Minikube: Local Kubernetes cluster manager
- kubectl: Command-line tool to interact with the Kubernetes cluster
- Ubuntu EC2 Instance: Cloud environment for setup and execution
- YAML: Used to define Kubernetes manifests

##  Objective

- Set up Minikube on an EC2 instance to simulate a local Kubernetes cluster
- Deploy a sample application using Kubernetes Deployment
- Expose the deployed application via Kubernetes Service
- Scale the application and inspect pods and services

##  Project Structure

 `README.md`       - Main documentation explaining the full workflow 
 `deployment.yaml` - YAML file to deploy a containerized Nginx app    
 `service.yaml`    - YAML file to expose the app using NodePort       
 `screenshots/`    - Folder containing screenshots of output commands 

##  Key Workflow Summary

### 1️. Environment Setup

An Ubuntu EC2 instance was prepared. Docker was installed to serve as the container runtime. Minikube was installed and configured to use Docker as the driver.

### 2️. Starting the Kubernetes Cluster

Minikube was started successfully, initializing a single-node Kubernetes cluster inside the EC2 instance.

### 3️. Application Deployment

A sample application using the Nginx image was defined in a Deployment YAML file. This Deployment specified the number of replicas and labels for pod selection.

### 4️. Exposing the Application

The deployed application was made accessible using a Service defined in a separate YAML file. The type of service used was NodePort, allowing access via a specific port.

### 5️. Verification and Scaling

Kubernetes commands were used to verify:

- The pods running in the cluster
- The services and assigned ports
- Logs of the deployed application
- The application’s ability to scale (replica increase)

##  Screenshots

Screenshots are saved in the `screenshots/` folder and include:

- Minikube cluster startup confirmation
- List of pods and services
- Deployment and service status
- Scaling and description outputs

## Outcome

- Successfully built and managed a Kubernetes cluster using Minikube on EC2
- Deployed and exposed an application using standard Kubernetes YAML manifests
- Verified deployment, scaled replicas, and captured outputs
- Project structured and documented for sharing and future reference
