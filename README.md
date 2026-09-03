# Cloud-Based Business Management Application
## Internship Project — Task 1: Cloud Architecture Design

### Project Overview
This project presents a provider-neutral cloud architecture for a hypothetical business management application. It demonstrates compute, database, storage, networking, DNS, security boundaries, backup, scalability, availability, data flow, and major architecture trade-offs.

> **Scope note:** This is an original hypothetical architecture created for the internship task. It does not use private R7World or customer production architecture details.

### Objectives
- Design a secure and scalable cloud architecture.
- Separate public-facing and private workloads.
- Provide highly available application compute.
- Protect transactional data with managed database services and backups.
- Store large objects separately from relational data.
- Explain DNS, networking, security, data flow, availability, backup, and scaling decisions.
- Provide editable architecture source where possible.

### Architecture Summary
Users access the application through DNS and HTTPS. Traffic reaches a CDN/load-balancer layer and is routed to application compute instances in private subnets across multiple availability zones. Application services access a private managed relational database, object storage, and cache. Monitoring, IAM, encryption, automated backups, and disaster-recovery controls provide operational resilience.

### Repository Structure
```text
cloud-architecture-task-1/
├── README.md
├── report/
│   └── Cloud_Architecture_Report.md
├── diagrams/
│   ├── cloud_architecture.drawio
│   ├── cloud_architecture.png
│   └── cloud_architecture.pdf
├── notebook/
│   └── cloud_architecture.ipynb
├── dashboard/
│   └── architecture_dashboard.pdf
├── documentation/
│   ├── security.md
│   ├── backup_and_disaster_recovery.md
│   ├── scalability.md
│   └── assumptions_and_tradeoffs.md
└── LICENSE
```

### Key Design Decisions
1. Managed relational database for transactional business data.
2. Object storage for documents and media.
3. Private application and database tiers.
4. Multi-availability-zone application deployment.
5. Horizontal auto-scaling for application compute.
6. HTTPS/TLS for data in transit and encryption at rest.
7. Automated database backups and separate backup storage.
8. DNS managed as a highly available service.
9. Monitoring, logging, and alerting for operations.

### Assumed Recovery Targets
- **RPO:** 15 minutes for critical transactional data.
- **RTO:** 1 hour for restoration of the core application.
- These values are project assumptions, not customer requirements.

### How to Review
Start with `report/Cloud_Architecture_Report.md`, then open the diagram source in diagrams.net/draw.io. The notebook provides an architecture walkthrough and validation checklist.

### Originality
The architecture, documentation, diagrams, assumptions, and repository organization are prepared specifically for this internship task and are intended as original project work.
