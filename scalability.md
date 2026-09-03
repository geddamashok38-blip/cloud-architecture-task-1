# Scalability Notes

## Application Tier
Use horizontal auto-scaling. Add application instances as request rate, latency, CPU, or memory increases.

## Database
Use a managed relational database initially. Improve performance with indexing, connection pooling, query optimization, and read replicas for read-heavy workloads.

## Storage
Object storage scales independently and is appropriate for large files.

## Caching
Cache frequently requested non-authoritative data to reduce database load.

## Scaling Trade-off
Aggressive auto-scaling improves responsiveness but can increase cost. Thresholds should be tuned using observed workload metrics.
