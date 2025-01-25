| Name | Infrastructure as code (IaC) |
|-|-|
| Approval date | 15.1.2025 |
| Category | Standard |

# Definition

This standard mandates that all infrastructure resources must be managed using Infrastructure as Code. Terraform / OpenTofu ecosystem is used for IaC.

# Purpose

To ensure a flexible, maintainable, replicable, and secure approach to managing infrastructure resources.

# Scope

This standard applies to all deployed infrastructure within the organization that requires some stateful configuration.

It will be introduced gradually to ensure smooth integration into existing processes and infrastructure. It will be introduced into existing projects gradually, based on projects or resource types case-by-case.

It encompasses testing and production environments.

All newly introduced projects must implement all relevant resources in IaC according to the current status of IaC implementation in NASES.

# Rationale

IaC brings environment replicability and improves security by allowing peer reviews and automated tests.

Only exclusive use of IaC can guarantee proper environment consistency, security, and allow the environment to be truly replicated or rebuilt if needed. Any manual interventions bypassing IaC break these guarantees.

# Requirements

- All resources in defined environments should be provisioned by IaC only.
- Manual infrastructure interventions are allowed only in emergency situations, and all changes should be incorporated into the IaC codebase ASAP after the emergency is resolved.
- Select technologies that can be properly provisioned by IaC.
- Adhere to proper development workflow also during IaC development.
- Parameterize IaC code properly so it is reusable and does not contain any secrets.

# Compliance

- Regular audits will be conducted to ensure adherence to this standard.
- All resources that do not exist in IaC must be documented, and corrective actions should be planned and implemented.
