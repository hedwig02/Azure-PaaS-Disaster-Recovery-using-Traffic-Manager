# Azure-PaaS-Disaster-Recovery-using-Traffic-Manager
# Azure PaaS Disaster Recovery Project using Traffic Manager

## Project Overview

This project demonstrates a Platform as a Service (PaaS) Disaster Recovery solution on Microsoft Azure using:

- Azure App Service
- Azure App Service Plan
- Azure Traffic Manager
- Multi-region deployment
- Priority-based failover routing

The goal of this project is to ensure high availability and automatic failover during regional outages.

---

# Architecture

Primary Region:
- Canada Central
- App Service: app-primary-sejal

Disaster Recovery Region:
- Central US
- App Service: app-dr-sejal

Traffic Distribution:
- Azure Traffic Manager
- Routing Method: Priority

---

# Services Used

| Service | Purpose |
|---|---|
| Azure App Service | Host web applications |
| App Service Plan | Compute resources for App Services |
| Azure Traffic Manager | Global DNS-based traffic routing |
| Resource Groups | Resource organization |
| Azure Portal | Resource deployment and management |

---

# Project Workflow

1. Created two Resource Groups in different Azure regions
2. Created two App Service Plans
3. Deployed two Web Apps
4. Configured Azure Traffic Manager
5. Added endpoints for both applications
6. Configured Priority routing method
7. Tested endpoint health monitoring
8. Simulated disaster recovery and failover

---

# Traffic Manager Configuration

| Setting | Value |
|---|---|
| Routing Method | Priority |
| Primary Endpoint Priority | 1 |
| DR Endpoint Priority | 2 |
| Monitoring Protocol | HTTP |
| Monitoring Port | 80 |
| Monitoring Path | / |

---

# Disaster Recovery Scenario

If the primary region becomes unavailable:

- Traffic Manager automatically redirects users
- Traffic is routed to the DR region
- Application remains accessible
- Downtime is minimized

---

# Business Use Case

A global company hosting customer-facing applications requires:

- High availability
- Business continuity
- Automatic failover
- Reduced downtime
- Better user experience

This solution helps organizations continue serving users even during regional outages.

---

# Key Learning Outcomes

- Azure App Service deployment
- Multi-region architecture
- Traffic Manager configuration
- Disaster Recovery concepts
- Priority routing implementation
- High availability design
- PaaS-based failover solution

---

# Screenshots

## Primary App Service
(Add screenshot here)

## DR App Service
(Add screenshot here)

## Traffic Manager Endpoints
(Add screenshot here)

## Endpoint Health Status
(Add screenshot here)

---

# Future Improvements

- Implement custom domain
- Configure HTTPS certificates
- Add Azure Front Door
- Integrate monitoring with Azure Monitor
- Automate deployment using Terraform

---

# Author

Sejal Sakhala

GitHub:
https://github.com/hedwig02
