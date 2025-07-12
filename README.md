# Azure Misconfiguration Scanner

This tool identifies high-risk misconfigurations in Azure environments, focusing on identity, network, and storage layers.

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

