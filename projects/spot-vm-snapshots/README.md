# Spot VM Snapshot Automation

> Status: imported implementation; deployment and end-to-end behavior have not been validated during consolidation. See [review notes](docs/review.md).

An Azure serverless automation solution designed to create scheduled disk snapshots for Azure Spot Virtual Machines. Built using Python Azure Functions, Bicep, and managed identities, the project demonstrates automated infrastructure management, Azure resource authentication, and infrastructure-as-code deployment.
---

## Features
- Hourly snapshot automation (CRON scheduled)
- Uses Azure Managed Identity to access VM resources
- Snapshots tagged by VM name and timestamp
- Deployed via Azure Bicep + Azure CLI

---

## Tech Stack
- **Azure Functions (Python)**
- **Bicep (Infrastructure as Code)**
- **Azure CLI**
- **Azure Compute + Storage**

---

## Folder Structure
```
spotvm-snapshot-automation/
├── function-app/              # Azure Function code
│   ├── __init__.py
│   ├── function.json
│   ├── host.json
│   └── requirements.txt
├── main.bicep                # Bicep template to deploy infrastructure
├── .gitignore
└── README.md                
```

---

## ⚙️ How to Deploy

### 1. Deploy infrastructure with Bicep:
```bash
az deployment group create \
  --resource-group <your-rg> \
  --template-file Bicep/main.bicep
```

### 2. Deploy the Function (from local machine):
```bash
cd function-app
func azure functionapp publish <your-function-app-name>
```

---

## To-Do / Improvements
- [ ] Add email or Teams alert on snapshot failure
- [ ] Add snapshot retention policy automation

---

## Author

Developed by [LabsByNateJ](https://github.com/LabsByNateJ).

This project demonstrates Azure automation using serverless computing, managed identities, and Infrastructure as Code (IaC).

**Portfolio:** [labsbynatej.com](https://labsbynatej.com)
