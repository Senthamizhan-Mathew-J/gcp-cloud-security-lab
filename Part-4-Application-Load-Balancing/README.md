# Part 4 – Google Cloud Application Load Balancer

## Overview

This project demonstrates how to deploy a highly available web application using Google Cloud Application Load Balancer. Multiple Compute Engine instances are grouped into a Managed Instance Group and exposed through an external HTTP Load Balancer.

---

## Objectives

- Deploy multiple Apache web servers
- Configure firewall rules
- Create an Instance Template
- Deploy a Managed Instance Group
- Configure HTTP Health Checks
- Create Backend Service
- Configure URL Map
- Create Target HTTP Proxy
- Configure Global Forwarding Rule
- Verify Load Balancer functionality

---

## Architecture

```
Internet
    │
    ▼
External HTTP Load Balancer
    │
    ▼
Target HTTP Proxy
    │
    ▼
URL Map
    │
    ▼
Backend Service
    │
    ▼
HTTP Health Check
    │
    ▼
Managed Instance Group
 ├─────────────┬─────────────┤
 VM1          VM2          VM3
```

---

## Technologies

- Google Cloud Platform
- Compute Engine
- Managed Instance Groups
- HTTP Health Checks
- Firewall Rules
- External HTTP Load Balancer
- Apache Web Server

---

## Results

- Successfully deployed three web servers.
- Configured a Managed Instance Group.
- Created backend service.
- Configured HTTP Health Check.
- Created URL Map.
- Configured Target HTTP Proxy.
- Created Global Forwarding Rule.
- Successfully verified healthy backend instances.

---

## Screenshots

Refer to the Screenshots folder.

---

## Author

Senthamizhan J
Integrated M.Tech Software Engineering
VIT Vellore