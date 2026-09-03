# Assumptions and Trade-offs

## Assumptions
- Hypothetical business application.
- Moderate initial traffic.
- Authenticated users.
- Transactional relational data.
- Object storage for large files.
- Two availability zones.
- RPO 15 minutes and RTO 1 hour are assumed targets.

## Trade-offs
### Managed vs self-managed database
Managed is simpler operationally; self-managed offers more control.

### Containers vs VMs
Containers support rapid deployment and scaling; VMs may be simpler for legacy workloads.

### Single-region vs multi-region
Single-region multi-zone is simpler and cheaper. Multi-region improves disaster tolerance but increases complexity.

### Performance vs cost
Caching and additional replicas improve performance but add cost and operational complexity.
