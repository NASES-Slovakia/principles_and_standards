| Name | Private Cloud Deployment Standard for Combined Virtualization and Containerization Platforms |
|-|-|
| Approval date | 03.10.2024 |
| Category | Standard |

# Definition

This standard mandates the preferred technologies for deploying a private cloud solution that supports both virtualization and containerization. The primary recommended solution is based on RedHat OpenShift, with SUSE Rancher integrated with Longhorn as a secondary option, recognizing its limitations compared to RedHat OpenShift.

# Purpose

To establish a unified approach for deploying a combined virtualization and containerization platform within the private cloud. This ensures efficient management of both traditional virtual machines and containerized applications while enabling scalability, flexibility, and improved resource utilization. The goal is to provide consistency in technology selection, allowing for seamless integration and reliable operations across the organization's infrastructure.

# Scope

This standard applies to all projects requiring private cloud deployment within the organization. It encompasses the development, testing, and production environments where a combined platform for virtualization and containerization is necessary. It supports hybrid workloads, covering both traditional applications running in virtual machines and modern containerized applications.

# Rationale

## Primary Preference for RedHat OpenShift

- Based on findings from Gartner’s research (G00803119), RedHat OpenShift is positioned as a leading platform for container management and hybrid private cloud deployments. It offers robust capabilities for scaling across on-premises, edge, and multi-cloud environments and is considered a mature solution for enterprise-grade deployment scenarios.

## Resource Availability

- There is a significantly larger pool of qualified and certified professionals available for RedHat OpenShift in Slovakia, largely due to proximity to Brno, where RedHat has a major development center. This local availability of expertise ensures faster deployment, improved operational support, and optimized use of skilled resources.

## Operational Efficiency and High Availability

- RedHat OpenShift provides comprehensive tools for managing both containerized and virtualized workloads, offering unified governance and a high level of automation, which ensures operational efficiency. SUSE Rancher with Longhorn, while a viable alternative, significantly lags behind RedHat in terms of product maturity, ecosystem integration, and enterprise functionality.

## Unified Management and Scalability

- Both platforms support multi-cloud, edge, and hybrid deployments, but RedHat OpenShift has superior integration capabilities and a stronger partnership network, providing greater confidence for strategic adoption.

# Requirements

## Technology Choice

- All private cloud deployments involving combined virtualization and containerization must primarily use RedHat OpenShift as the default platform. SUSE Rancher with Longhorn may be used only if explicitly approved, with justification, as it is considered less mature and with fewer certified resources available.

## Support for Combined Virtualization and Containerization

- The platform must support both virtual machines and containerized applications in an integrated manner. RedHat OpenShift is preferred due to its advanced features for managing mixed environments seamlessly.

## Scalability and Flexibility

- The chosen platform must support multi-cloud, hybrid cloud, and edge scenarios. This includes deployment in on-premises data centers, remote locations, and integration with public cloud services. RedHat OpenShift’s capabilities in this area are considered industry-leading.

## Operational Management

- RedHat OpenShift provides centralized management tools that support provisioning, monitoring, and lifecycle management of both virtual machines and container workloads. SUSE Rancher’s capabilities in this area are functional but considered less robust.

## High Availability and Data Protection

- The platform must include built-in high availability for both compute and storage layers. While SUSE Rancher with Longhorn provides basic data protection, RedHat OpenShift offers a more comprehensive high availability and disaster recovery solution suitable for enterprise deployments.

## Support Requirements

- Commercial support must be available for the chosen platform to ensure reliable operations and rapid response to issues. RedHat OpenShift’s support network, including the abundance of certified resources in Slovakia, makes it a more favorable choice.
- Platforms must provide a clear SLA for availability and support, aligning with organizational needs for production systems.

## Governance and Compliance

- Deployment must adhere to defined security policies, and platforms must support centralized governance and compliance, including role-based access controls, policy enforcement, and logging. RedHat OpenShift's centralized governance is superior, and this should be leveraged wherever possible.

# Compliance

## Audits

- Regular audits will be conducted to ensure that deployed private cloud platforms comply with the prescribed standard, with RedHat OpenShift being the primary solution. Audits will evaluate adherence to the use of OpenShift wherever possible, with deviations requiring substantial justification.

## Non-Compliance

- Non-compliance with this standard must be documented, and corrective actions should be planned and implemented.

# Documentation

## Platform Details

- Each deployment must be documented, including the platform used, the architecture, high-availability configuration, and details of the virtualization and containerization workloads.

## Operational Procedures

- Documentation must include operational procedures for managing and scaling the private cloud platform, covering both virtualization and container environments.
