# 🔍 Azure Misconfiguration Scanner (90-Day Challenge)

This repository contains the code, configurations, queries, and documentation for an **open-source Azure Misconfiguration Scanner**, developed over a focused 90-day execution sprint. The scanner is designed to identify insecure configurations in Azure environments using Azure Policy, Azure CLI, and scripted detection logic.

> ⚡ Status: **Day 7 Complete**  
> ✅ Phase: Initial Detection Logic + Policy Simulation  
> 🛠️ In Progress: Detection logic scaffolding, policy validation, and automation

---

## 📌 Project Goals

- Detect common Azure misconfigurations (e.g., public IPs on NICs, overly permissive roles)
- Use **Azure Policy**, **Azure CLI**, and **PowerShell** to validate and simulate findings
- Build a modular and extensible scanner that can be enhanced over time
- Reinforce hands-on learning of Azure administration and security via real-world lab tasks

---

## 📁 Repo Structure

```plaintext
.
├── detections/
│   └── nics-with-public-ips.cli           # CLI-based detection logic for public IPs on NICs
├── queries/
│   └── nics-with-public-ips-results.json  # Output from policy state list query
├── policies/
│   └── insecure_role.json                 # Custom role with overly broad permissions
├── roles/
│   └── insecure-role-create.ps1           # PowerShell script to create custom role
├── scripts/
│   └── assign-insecure-role.ps1           # Role assignment logic
├── docs/
│   └── day-3-notes.md                     # Focused notes & reflection (Day 3)
│   └── day-4-notes.md                     # Focused notes & reflection (Day 4)
│   └── day-5-notes.md                     # Focused notes & reflection (Day 5)
│   └── day-6-notes.md                     # Focused notes & reflection (Day 6)
│   └── day-7-notes.md                     # Focused notes & reflection (Day 7)
├── README.md                              # Project overview and progress

```

## Current Capabilities
- Detects role assignments at subscription level
- Flags custom roles with wildcard or IAM write permissions
- Identifies exposed storage keys

## Modules
- `identity.py`
- `network.py`
- `storage.py`

## Planned Features
- Log-based detection (Activity Logs)
- Terraform environment misconfig validator
  
```