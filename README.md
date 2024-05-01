# Kubernetes Environment Deployment

## Overview
This project aims to deploy three separate environments (Production, Development, and Testing) using Kubernetes. Each environment consists of a deployment with five replicas, each configured with resource limits. Additionally, services are created to expose these deployments for local connections. Finally, a fanout Ingress is established to route traffic to the respective services based on specific rules.

## Deployments
### Production Environment
-Name: prod-deployment
- Replicas: 5
- Resource Limits: 
  - Memory: 128Mi
  - CPU: 500m

### Development Environment
- Name: dev-deployment
- Replicas: 5
- Resource Limits: 
  - Memory: 128Mi
  - CPU: 500m




### Testing Environment
- Name:  test-deployment
- Replicas:  5
- Resource Limits: 
  - Memory: 128Mi
  - CPU: 500m

## Services
Each deployment has a corresponding service to facilitate local connections.

•	Production Service
•	Development Service
•	Testing Service

## Ingress
A fanout Ingress is configured to direct traffic to the appropriate service based on defined rules.

- Ingress Name: my-ingress
- Rules:
  1. Path: /production → Service: prod-service
  2. Path: /development → Service: dev-service
  3. Path: /testing → Service: test-service

## Conclusion
This project sets up three distinct Kubernetes environments (Production, Development, and Testing), each with its deployment, service for local connections, and a fanout Ingress to manage incoming traffic effectively. With resource limits defined for each deployment, the project ensures efficient resource allocation and management within the Kubernetes cluster.
