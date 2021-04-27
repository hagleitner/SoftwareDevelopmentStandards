---
layout: default
title: Azure
nav_order: 350
has_children: false
permalink: /documentation/azure
---

# Azure DevOps

## Naming conventions
We stick to [Microsoft's conventions](https://docs.microsoft.com/en-us/azure/cloud-adoption-framework/ready/azure-best-practices/resource-naming) if not defined otherwise below.

### Resource groups naming scheme
```rg-hsm-<workload/Application>-<environment>```

### Resources naming scheme
```<resorucetype>-hsm-<4-letter-abbreviation workload/Application>-<environment>```

|Application / Workload | 4-letter abbreviation |
|-------------| ----------------------|
| Hagleitner Business Data Proxy | hbdp
HsM Catalog Service	| cata
HsM Client Service | clie
HsM Data Analysis Service |	daan
HsM Data Link Monitoring Service|dlmo
HsM Digital Twin Service|ditw
HsM Primary Data Processing|pdpr
HsM Temporary TV Monitor|ttmo
HsM v1 Data Migration|wepo

|Environment | Abbreviation |
|-------------| ----------------------|
Development | dev
Integration	| int
Staging | stage
Production | prod