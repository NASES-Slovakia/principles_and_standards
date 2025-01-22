| Name | Application Deliveries Use Operator Pattern |
|-|-|
| Approval date | 17.7.2024 |
| Category | Standard |

# Definition

Application delivery and lifecycle management must employ the Operator pattern to enhance automation, scalability, and reliability in Kubernetes environments.

# Purpose

To ensure that all applications deployed within the organization follow a consistent approach to operational automation, leveraging Kubernetes Operators for efficient management.

# Scope

This standard applies to all new application deployments and significant updates to existing applications within the organization that are managed on Kubernetes.

# Rationale

## Automation

Operators automate complex operational tasks, reducing manual intervention and operational overhead.

## Scalability

Efficiently manage application deployments at scale, ensuring consistent operations across environments.

## Reliability

Reduce the risk of human error and increase system reliability through codified best practices.

## Consistency

Ensure consistent application lifecycle management and operations across different environments.

## Customization

Allow for tailored management of stateful and complex applications to meet specific requirements.

# Development

- Applications must be designed to use the Operator pattern for lifecycle management tasks.
- Utilize established frameworks (e.g., Operator Framework, Kubebuilder) for developing Operators.

# Skills

- Development and operations teams must be trained in creating and managing Kubernetes Operators.

# Tools and Frameworks

- Implement and use tools that support the development and deployment of Operators.
- Maintain and version-control Operator code and configurations using infrastructure as code (IaC) practices.

# Governance

- Establish best practices and governance for developing and maintaining Operators.
- Ensure Operators comply with organizational security, compliance, and performance standards.

# Monitoring and Management

- Implement robust monitoring and alerting mechanisms for Operators.
- Ensure Operators can handle failure scenarios and provide adequate logging and diagnostics.

# Compliance

Regular audits will be conducted to ensure adherence to this standard.

Non-compliance must be documented, and corrective actions should be planned and implemented.

# Example Implementations

- **Database Management**: Operators must manage database lifecycle tasks, including provisioning, scaling, and backups.
- **Application Upgrades**: Operators should handle rolling upgrades and rollbacks to ensure zero downtime.
- **Custom Resources**: Define and manage complex applications using Custom Resource Definitions (CRDs) and corresponding Operators.
- **Service Mesh**: Use Operators for deploying and managing service meshes, ensuring consistent configuration and observability.
