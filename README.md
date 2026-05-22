# Azure PaaS & IaaS Disaster Recovery Project

## 📌 Project Overview

This project demonstrates the implementation of Disaster Recovery (DR) and High Availability architectures in Microsoft Azure using both Platform as a Service (PaaS) and Infrastructure as a Service (IaaS) components.

The project includes:

- Azure App Services
- Azure Traffic Manager
- Azure Virtual Machines
- Azure Load Balancer
- Azure Application Gateway
- IIS Web Server
- High Availability & Disaster Recovery concepts

---

# ☁️ Module 1 – PaaS Disaster Recovery

## 🔹 Objective

Implement Disaster Recovery for Azure App Services using Azure Traffic Manager with priority-based routing.

---

## 🛠️ Services Used

- Azure App Service
- Azure App Service Plan
- Azure Traffic Manager
- Azure Resource Groups

---

## 🏗️ Architecture

Users → Traffic Manager → Primary App Service / DR App Service

---

## ✅ Tasks Performed

### 1. Created Resource Groups
- rg-paas-primary-sejal
- rg-paas-dr-sejal

### 2. Created App Services
- app-primary-sejal
- app-dr-sejal

### 3. Configured Traffic Manager
- Routing Method: Priority
- Added Primary Endpoint
- Added DR Endpoint

### 4. Verified Endpoint Health
- Both endpoints configured and monitored successfully

---

# ☁️ Module 2 – IaaS Disaster Recovery

## 🔹 Objective

Implement High Availability architecture using Azure Virtual Machines, Load Balancer, and Application Gateway.

---

## 🛠️ Services Used

- Azure Virtual Machines
- Azure Virtual Network
- Azure Load Balancer
- Azure Application Gateway
- IIS Web Server
- Azure Bastion

---

# 🏗️ Architecture

Users  
↓  
Application Gateway  
↓  
Azure Load Balancer  
↓  
VM-Web1 + VM-Web2 (IIS)

---

# ✅ Tasks Performed

## 1. Created Resource Groups
- rg-iaas-prod-sejal
- rg-iaas-dr-sejal

---

## 2. Created Virtual Networks
- vnet-prod-sejal
- vnet-dr-sejal

---

## 3. Deployed Windows Virtual Machines
- vm-web1
- vm-web2

Both VMs were deployed in Canada Central region.

---

## 4. Installed IIS Web Server 

---

## 5. Configured Azure Load Balancer

### Components Configured

- Frontend Public IP
- Backend Pool
- Health Probe
- Load Balancing Rule

### Backend Pool
- vm-web1
- vm-web2

### Health Probe
- Protocol: HTTP
- Port: 80

### Load Balancing Rule
- Frontend Port: 80
- Backend Port: 80

---

## 6. Configured Azure Application Gateway

### Features Configured

- Public Frontend IP
- Backend Pool
- HTTP Listener
- Routing Rule
- Backend HTTP Settings

### Routing Flow

Users  
↓  
Application Gateway  
↓  
Load Balancer  
↓  
VM-Web1 + VM-Web2

---

# 🔄 Disaster Recovery Concepts

## RTO (Recovery Time Objective)

RTO defines the maximum acceptable downtime during a disaster.

Example:
- RTO = 30 Minutes
- System must recover within 30 minutes.

---

## RPO (Recovery Point Objective)

RPO defines the maximum acceptable data loss during disaster recovery.

Example:
- RPO = 15 Minutes
- Only 15 minutes of data loss is acceptable.

---

# 🚀 Phase 6 – Azure Site Recovery (Planned)

## 🔹 Objective

Implement Azure Site Recovery (ASR) for VM replication and automated disaster recovery between regions.

---

## 🛠️ Planned Services

- Azure Site Recovery
- Recovery Services Vault
- VM Replication
- Failover & Failback
- Disaster Recovery Testing

---

## 🔹 Planned DR Workflow

### 1. Create Recovery Services Vault
- Configure replication infrastructure

### 2. Enable VM Replication
- Replicate production VMs to DR region

### 3. Configure Replication Policies
- Recovery Point Retention
- Snapshot Frequency
- Failover Settings

### 4. Test Failover
- Simulate disaster scenario
- Verify VM recovery in DR region

### 5. Planned Failback
- Restore services back to primary region

---

# 📚 Key Concepts Learned

- High Availability
- Disaster Recovery
- Azure Networking
- Load Balancing
- Health Probes
- Application Gateway
- IIS Configuration
- VM Architecture
- RTO & RPO
- Traffic Routing
- Failover Architecture

---

# 💡 Real-World Use Cases

This architecture is commonly used in:

- Banking Applications
- Healthcare Systems
- E-Commerce Platforms
- Enterprise Web Applications
- SaaS Platforms

---

# 🧠 Interview Explanation

This project demonstrates the implementation of enterprise-grade Disaster Recovery and High Availability architecture in Microsoft Azure.

The environment includes:
- Azure App Services with Traffic Manager for PaaS DR
- Azure Virtual Machines with IIS for IaaS hosting
- Azure Standard Load Balancer for traffic distribution
- Azure Application Gateway for Layer 7 routing
- Planned Azure Site Recovery for VM replication and failover

The solution was designed to improve:
- Availability
- Scalability
- Fault Tolerance
- Disaster Recovery readiness

---

---

# 🛠️ Technologies Used

- Microsoft Azure
- Azure App Service
- Azure Traffic Manager
- Azure Virtual Machines
- Azure Load Balancer
- Azure Application Gateway
- Azure Site Recovery
- IIS Web Server
- Azure Networking

---

# 👩‍💻 Author

Sejal Sakhala

GitHub:
https://github.com/hedwig02
