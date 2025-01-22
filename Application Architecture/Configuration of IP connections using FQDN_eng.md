| Name | Configuration of IP connections using FQDN |
|-|-|
| Approval date | 17.7.2024 |
| Category | Standard |

# Definition

This standard mandates that IP connections be configured using Fully Qualified Domain Names (FQDN) instead of direct IP addresses, with configuration parameters stored in external configuration files or parameters rather than being hard-coded in the source code.

# Purpose

To ensure a flexible, maintainable, and secure approach to configuring IP connections in applications by using FQDNs and external configuration mechanisms.

# Scope

This standard applies to all software applications and services developed, maintained, or deployed within the organization that require IP connections.

It encompasses development, testing, and production environments.

# Rationale

## Flexibility and Maintenance

Using FQDNs and external configuration files allows for easier updates and changes to network configurations without modifying the source code.

## Scalability

Facilitates the deployment of applications across different environments by allowing environment-specific configurations to be managed separately.

## Security

Minimizes the risk of exposing sensitive information in the source code by keeping configuration details in controlled external files.

# Requirements

## Use of FQDN

All IP connections must be defined using Fully Qualified Domain Names instead of direct IP addresses.

## External Configuration

Configuration parameters for IP connections must be stored in configuration files or application parameters, not hard-coded in the source code.

## Configuration Management

Configuration files must be easily accessible and editable without requiring changes to the application’s source code. Version control for configuration files should be implemented to track changes.

## Documentation

Adequate documentation must be provided to describe the configuration parameters and their usage.

# Compliance

Regular audits will be conducted to ensure adherence to this standard.

Non-compliance must be documented, and corrective actions should be planned and implemented.
