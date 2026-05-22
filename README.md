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
