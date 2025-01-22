| Name | Prefer Cloud Native Design of Systems |
|-|-|
| Approval date | 17.07.2024 |
| Category | Principle |

# Statement

Design and develop systems using cloud-native principles to ensure scalability, resilience, and agility.

# Rationale

- **Scalability**: Cloud-native architectures are inherently designed to scale horizontally, meeting demand efficiently.
- **Resilience**: Leveraging cloud-native patterns, such as microservices and distributed systems, increases fault tolerance and system resilience.
- **Agility**: Cloud-native design supports rapid development, deployment, and iteration of applications, aligning with DevOps and CI/CD practices.
- **Cost Efficiency**: Pay-as-you-go models and elastic scaling reduce infrastructure costs by matching resources to demand.
- **Portability**: Cloud-native applications are often designed to be platform-agnostic, increasing flexibility in cloud provider choices.

# Implications

## Architecture

- Embrace microservices, serverless computing, and other cloud-native architectures.
- Design systems to be stateless where possible and to use cloud services for state management.

## Development

- Adopt practices such as CI/CD, automated testing, and continuous monitoring to support rapid development and deployment cycles.

## Skills

- Invest in training for development and operations teams on cloud-native technologies and practices.

## Security

- Implement security best practices for cloud environments, including identity and access management, encryption, and compliance with relevant standards.

## Infrastructure

- Utilize managed cloud services for infrastructure needs, ensuring infrastructure as code (IaC) practices are in place for reproducibility and automation.

## Vendor Neutrality

- Design systems to avoid vendor lock-in by using open standards and ensuring portability across different cloud platforms when feasible.

# Example Implementations

- **Microservices Architecture**: Break down monolithic applications into microservices that can be deployed and scaled independently.
- **Serverless Computing**: Use serverless frameworks to build applications that automatically scale based on demand and reduce the overhead of managing servers.
- **Containers and Kubernetes**: Deploy applications using containers orchestrated by Kubernetes for efficient scaling and management.
- **Cloud-native Databases**: Utilize cloud-native databases and data services that provide high availability, scalability, and managed operations.
