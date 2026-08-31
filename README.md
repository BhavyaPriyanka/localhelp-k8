# LocalHelp – Kubernetes Deployment

LocalHelp is a 3-tier application deployed on **Amazon EKS** using Kubernetes.

### Application Stack

- Frontend – React
- Backend – Java
- Database – MySQL

## High-Level Flow

**User → AWS ALB → Ingress → Frontend Service → React Frontend → Backend Service → Java Backend → MySQL Service → MySQL + AWS EBS**

The Backend uses an **Init Container** to wait for MySQL to become reachable before starting the application container.

Resource requests and limits are configured for the application containers, and **HPA** is used to scale workloads based on resource utilization.
---------------------------------------------
* Deployed the LocalHelp frontend, backend, and MySQL components successfully on Amazon EKS using Kubernetes manifests.
* Configured Nginx frontend → Backend API communication through Kubernetes ClusterIP Services.
* Exposed the frontend externally through an AWS Load Balancer (ALB/NLB) with health checks and verified application connectivity


