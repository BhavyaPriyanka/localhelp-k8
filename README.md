## Traffic Flow

User traffic enters through an **AWS Application Load Balancer (ALB)** managed by the **AWS Load Balancer Controller**.

The Kubernetes **Ingress** defines the routing rules and forwards traffic to the Frontend Service.

Frontend → Backend Service → Java Backend → MySQL Service → MySQL

MySQL data is persisted using **PVC → PV → AWS EBS**.
