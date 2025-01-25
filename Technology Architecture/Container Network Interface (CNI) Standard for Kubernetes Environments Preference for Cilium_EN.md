| Name | Container Network Interface (CNI) Standard for Kubernetes Environments Preference for Cilium |
|-|-|
| Approval date | 03.10.2024 |
| Category | Standard |

# Definition

This standard mandates the preferred Container Network Interface (CNI) for Kubernetes environments deployed within the organization. Cilium is positioned as the clearly preferred CNI due to its superior performance, networking evolution capabilities, and ongoing support from Cisco following the acquisition of Isovalent.

# Purpose

To ensure a high-quality, scalable, and secure networking solution for Kubernetes clusters across the organization by standardizing on a single, high-performance CNI. Cilium is preferred due to its compatibility with modern network architectures, integration with Kubernetes and RedHat OpenShift, and its ongoing evolution and stability backed by Cisco’s networking expertise.

# Scope

This standard applies to all Kubernetes deployments within the organization, including but not limited to development, testing, staging, and production environments. The standard encompasses both new deployments and upgrades of existing clusters.

# Rationale

## Performance and Quality

- Cilium has been consistently ranked as one of the top-performing CNIs for Kubernetes environments, offering low latency and high throughput, as demonstrated by benchmarking studies. According to the ITNEXT Benchmark Results of Kubernetes Network Plugins CNI, Cilium provides industry-leading performance over 40Gbps networks.

## Cisco’s Acquisition of Isovalent

- With Isovalent, the primary developer behind Cilium, now under Cisco’s ownership, there is increased assurance regarding the long-term stability, evolution, and integration of Cilium with future networking technologies. This strategic acquisition aligns with Cisco's strength in networking and ensures compatibility with next-generation architectures.

## Integration with RedHat OpenShift

- The Isovalent Blog on Deploying Red Hat OpenShift with Cilium outlines how Cilium can seamlessly integrate with RedHat OpenShift, further strengthening its position as the preferred CNI for enterprise Kubernetes deployments.

## Scalability and Security

- Cilium's use of eBPF (extended Berkeley Packet Filter) provides advanced networking, observability, and security features that meet the needs of modern Kubernetes deployments at scale. The ability to implement security policies at the kernel level allows for a high level of control and visibility.

# Requirements

## Preferred CNI - Cilium

- Cilium must be used as the Container Network Interface for all Kubernetes deployments. Any deviation must be explicitly approved, accompanied by a comprehensive justification.

## Networking Performance

- Cilium must be configured to leverage high-performance features to maximize network throughput and minimize latency.

## Compatibility and Integration

- The CNI must be compatible with all major Kubernetes distributions in use within the organization, including RedHat OpenShift, as demonstrated by successful integrations.
- The CNI must support seamless integration with Cisco network infrastructure, ensuring compatibility with existing on-premises, hybrid, and multi-cloud environments.

## Operational Management and Observability

- Cilium’s native observability features must be enabled to provide deep visibility into network flows, policy enforcement, and performance metrics.
- The use of Hubble, Cilium's observability component, is mandated to support monitoring, tracing, and auditing of network traffic within Kubernetes clusters.

## Security Policies

- Cilium’s security policies must be utilized to enforce fine-grained network controls within Kubernetes clusters.
- Policies should leverage eBPF capabilities to enable efficient, kernel-level enforcement without affecting application performance.

## Scalability Considerations

- Cilium must be deployed in a manner that supports the scalability requirements of large Kubernetes environments, particularly those involving multi-cloud or hybrid deployments.
- Automated provisioning and configuration must be implemented to ensure that Cilium deployments are consistently aligned with the organization’s growth and scaling strategies.

## Support and Maintenance

- Given Cisco's backing, Cilium deployments must be supported with a commercial SLA to ensure high availability and prompt issue resolution.
- The organization must maintain up-to-date versions of Cilium, benefiting from the latest improvements in performance, security, and compatibility.

# Compliance

## Audits

- Regular audits will be conducted to ensure that Cilium is deployed and configured according to this standard. The audits will verify the correct use of Cilium’s observability tools, the implementation of security policies, and compliance with scalability requirements.

## Non-Compliance

- Any deviation from this standard must be documented, and corrective actions should be implemented. Non-compliance requires formal approval and should be supported by a risk assessment and an alternative plan.

# Documentation

## Deployment Details

- All Cilium deployments must be documented, including integration settings, configurations, and observed performance metrics.

## Operational Guidelines

- Comprehensive operational procedures must be provided, covering installation, configuration, monitoring, and troubleshooting of Cilium-based networks.
