| Name | HTTP(S) |
|-|-|
| Approval date | 15.1.2025 |
| Category | Standard |

# Definition

All HTTP communication should be secured using HTTPS. Insecure communication is only allowed for redirects to secure connections and for domain verification purposes.

Only certificates signed by trusted Certificate Authorities should be accepted.

# Purpose

To ensure secure communication.

# Scope

This standard applies to all services working with HTTP.

# Rationale

HTTPS guarantees secure communication only when the authenticity of the Certificate Authority (CA) is properly validated. When using self-signed CAs, the risk of skipping validation or accepting an invalid CA is higher.

Let's Encrypt provides trusted certificates for free with automation tools, providing only minimal overhead compared to insecure communication.

# Requirements

- All certificate provisioning should be automated.
- Certificate expiration has to be monitored, as an expired certificate will result in a denial of service (DoS).

# Compliance

- Regular audits will be conducted to ensure adherence to this standard.
- All services that do not adhere must be documented, and corrective actions should be planned and implemented.
