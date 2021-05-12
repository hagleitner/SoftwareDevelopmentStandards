---
layout: default
title: DNS
nav_order: 350
has_children: false
permalink: /documentation/dns
---

# DNS

All HsM related resources get DNS hostnames in the hsm.digital domain.

## DNS naming scheme

For all HsM services we use ```<workload-dns-nams>[-<environment>].hsm.digital```
For all Hagleitner services we use ```<workload-dns-nams>[-<environment>].hagleitner.com```
For services consisting of multiple tiers we append the tier name to the service name: ```<workload-dns-nams>-<tiername>[-<environment>].hsm.digital```

Examples

* catalog.hsm.gigital
* catalog-dev.hsm.digital
* catalog-db-stage.hsm.digital

## hsm.digital

|Application / Workload | DNS name
|-------------|----|
HsM Catalog Service| catalog.hsm.digital
HsM Catalog Service Database | catalog-db.hsm.digital
HsM Client Service| clientservice.hsm.digital
| | hsm.hygieneportal&#46;com
| | www.hsm.digital
HsM Client Service Database| clientservice-db.hsm.digital
HsM Data Analysis Service | dataanalysis.hsm.digital
HsM Data Link Monitoring Service| datalinkmonitoring.hsm.digital
HsM Data Link Monitoring Cache| datalinkmonitoring-cache.hsm.digital
HsM Device Provisioning Service | deviceprovisioning.hsm.digital
HsM Digital Twin Service| digitaltwin.hsm.digital
HsM Digital Twin Service Database| digitaltwin-db.hsm.digital
HsM Inter Service Communication | interservicecommunication.hsm.digital
HsM IotHub | iothub.hsm.digital
HsM Temporary TV Monitor| tv.hsm.digital
HsM TimeSeries Database | timeseriesdb.hsm.digital

### hagleitner&#46;com

|Application / Workload | DNS name
|-------------|----|
Hagleitner Business Data Proxy | businessdataproxy.hagleitner.com _On-premise but accessed from Azure