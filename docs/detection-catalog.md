## Detection Catalog

### NICs with Public IPs
- **ID**: `network-nic-public-ip`
- **Severity**: High
- **Category**: Networking
- **Policy**: Network interfaces should not have public IPs
- **Detection Logic**: `ipConfigurations[*].publicIpAddress.id != null`
