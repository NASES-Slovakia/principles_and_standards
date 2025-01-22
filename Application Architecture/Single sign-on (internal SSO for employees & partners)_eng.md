| Name | Single sign-on (internal SSO for employees & partners) |
|-|-|
| Approval date | 15.01.2025 |
| Category | Standard |

# Definition

All internal tools used by the organization requiring authentication must use SSO if possible. OpenID Connect is preferred.

All tools should have a local admin account that allows tool reconfiguration in case of identity provider failure.

# Purpose

To ensure a flexible, maintainable, replicable, and secure user access.

# Scope

This standard applies to all deployed tools within the organization that require user authentication.

It encompasses development, testing, and production environments.

# Rationale

SSO improves security and standardization in user management as well as authentication itself.

# Requirements

- To maintain this standardization, all authentication in an integrated tool should be done using SSO.
- To allow for emergency configuration recovery, all tools must have local admin accounts for tool administration that allows tool reconfiguration in case of identity provider connection failure.

# Compliance

- Regular audits will be conducted to ensure adherence to this standard.
- All tool accounts that do not exist in the identity provider must be documented, and corrective actions should be planned and implemented.
