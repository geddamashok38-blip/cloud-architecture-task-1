# Security Notes

## Security Boundaries
- Internet-facing access terminates at the edge/load-balancer layer.
- Application compute is private.
- Database services are private.
- Administrative access is restricted and logged.

## Access Control
- Least privilege
- Role-based access
- Separate service identities
- Secrets manager
- Credential rotation

## Network Controls
- Firewall/security groups
- Explicit inbound/outbound rules
- No public database endpoint
- HTTPS only for user-facing traffic

## Data Security
- TLS in transit
- Encryption at rest
- Protected backups
- Restricted backup access

## Application Security
- Authentication
- Authorization
- Input validation
- Rate limiting
- Security logging
