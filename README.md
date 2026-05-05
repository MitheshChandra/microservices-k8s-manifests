# Microservices Kubernetes Manifests

Kubernetes deployment manifests for microservices application.

## Structure

- **dev/** - Development environment manifests
- **prod/** - Production environment manifests

## Services

- PostgreSQL (shared database)
- API Gateway (NodePort 30080 for dev, 30081 for prod)
- User Service
- Order Service
- Payment Service

## Argo CD Applications

These manifests are synced automatically by Argo CD from this repository.

- **microservices-dev** - Auto-sync enabled
- **microservices-prod** - Manual sync (requires approval)

## Access

Dev: `http://<kubernetes-node-ip>:30080`  
Prod: `http://<kubernetes-node-ip>:30081`
