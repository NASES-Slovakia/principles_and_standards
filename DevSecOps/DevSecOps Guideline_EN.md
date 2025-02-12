| Name | DevSecOps Guideline |
|-|-|
| Approval date | 6.2.2025 |
| Category | Recommendation |

# Development

All source code must be stored in a GitLab repository in a readable and well-structured form, and in English. In the case of packaged software distributed in binary form, the container image must be delivered to the appropriate container registry in GitLab. Similarly, a Kubernetes Operator or Helm chart must be provided with the necessary documentation.

Changes must adhere to the standard git trunk-based workflow, including feature branches and merge requests into the master branch.

The master branch is protected.

Merging feature branches into master is only possible via a merge request, and force-pushing to master is not allowed.

All parts of the code must have designated code owners.

The main master/main branch is automatically deployed to the testing environment with each commit.

Commits must be coherent but reasonably sized, with a suitable commit message that briefly describes the changes and references an issue in the issue tracker.

A merge request must contain a reference to the issue and, if necessary, a description providing additional justification for the changes.

When working with git, we follow a process that generates a linear git history:

- All merge requests must be rebased to the latest commit of the base branch before merging.
- We use rebase to update feature branches and resolve conflicts. We do not merge the base branch into a feature branch.
- Merge requests are merged using a merge commit.

# Code Review

Each code change must undergo a code review within the merge request by at least one reviewer.

Specific parts and types of source code must have designated owners via "CODEOWNERS." Each type or section must have a group of at least two owners for substitution purposes.

The code review assesses the correctness and completeness of changes, adherence to all rules and principles, code quality, etc. Reports from scanning tools on code quality, test coverage, or dependency vulnerabilities are also evaluated.

Reviewers comment on deficiencies directly in the merge request, and the developer incorporates them by adding commits to the merge request. Finally, they request another review in GitLab.

After approval, the maintainer or developer can squash commits before merging without further modifications. If a rebase is needed due to conflict resolution, the approach is agreed upon between the developer and the reviewer.

# CI/CD

Each project must have a functional CI/CD pipeline for building and testing, including all necessary test types according to requirements. Build outputs—packages, images, reports, etc.—must be stored in relevant registries within the GitLab repository.

The supplier is responsible for delivering:

- A CI pipeline for building and testing the module,
- A CI pipeline for creating and signing a container image,
- A Kubernetes operator or Helm chart for deployment into a Kubernetes cluster,
- Deployment configuration for Helm/operator for defined environments,
- A Terraform template for infrastructure updates,
- Documentation of dependencies, parameters, and deployment descriptions for all environments.

Deployment is expected to be performed using ArgoCD. Confidential information/secrets are stored in Hashicorp Vault. Infrastructure is managed via Terraform scripts.

Releases must be tagged and versioned according to the SemVer methodology: <https://semver.org/>.

Applications must be distributed as Docker images. The Docker image should be the result of the GitLab CI build process.

# Security

Docker images must be "hardened"—built on an official, minimal base image for the specific technology. Docker images must contain only runtime dependencies and must not include build-time dependencies. The use of multi-stage Docker builds is expected.

Each Docker image must contain only one service.

Images must comply with recommendations:

- [CIS Docker Benchmark](https://www.cisecurity.org/benchmark/docker/),
- [NIST SP 800-190](https://nvlpubs.nist.gov/nistpubs/SpecialPublications/NIST.SP.800-190.pdf),
- [OWASP Docker Security Cheat Sheet](https://cheatsheetseries.owasp.org/cheatsheets/Docker_Security_Cheat_Sheet.html).

Requirements for delivered components in a Kubernetes environment:

- Network segmentation -- Network policy, Default deny,
- Secure configuration -- secrets in HashiCorp Vault,
- Access control -- Admission Controllers, ServiceAccount,
- Resource limits for containers.

# Observability

Framework used: [OpenTelemetry](https://opentelemetry.io).

Collected data:

- Logs -- centralized processing of container logs, audit logs,
- Metrics -- Prometheus, RED metrics, USE metrics,
- Traces -- Jaeger, distributed tracing, service mesh.

Each service process must include an endpoint to determine service status for integration with monitoring.

Each pod in a Kubernetes environment must include Liveness, Readiness, and Startup probes.

Logs must be written to STDOUT or STDERR of the Docker image. The log format must be configurable.

# Documentation

Documentation must be part of the repository in a text format that GitLab can display—Markdown or AsciiDoc is preferred.

# Environment

The application will run in Oracle PCA in an OKE cluster, potentially in RedHat OpenShift in the future. Deployment uses ArgoCD.

Environments are divided by purpose:

- Development,
- Testing,
- UAT,
- Production.

The production cluster is separated from testing and development environments in a standalone production environment.

# Testing

Testing is performed using automated tests within the CI/CD pipeline. We expect the delivery of complete GitLab CI pipelines necessary for testing and builds.

Tests run automatically upon pushing new changes to a merge request in GitLab and during the build and deployment of a new release.

Tests must run in GitLab CI runners in headless mode. The runner is containerized using Docker. Output reports must be readable within the GitLab pipeline.

GitLab has an activated Ultimate license. We prefer utilizing the features this license provides and supplementing them with additional open-source tools where necessary.
## Tests assigmens to enviroment

 
 | Prostredie            | Testy                          | Spustenie
 | --------------------- | ------------------------------ | -------------------
 | Development              | Unit , SAST, Integration        | Automatic
 | Test enviroment | E2E, DAST                      | Automatic
 | Test enviroment| PEN, Load                  | Manual
 | UAT                   | UAT                            | ManuálManualne
 


# GitLab -- GitHub Workflow

All projects have a primary repository in NASES GitLab.

No git repository may contain sensitive data, tokens, passwords, certificates, or keys. All such values must be represented or described in terms of parameters.

Build-time secrets must be stored in GitLab Variables with appropriate protection and visibility settings.

Run-time secrets must be stored in Hashicorp Vault and referenced using files.

All repositories must include licensing information in a "LICENSE" file and basic information, descriptions, and guides in a "README" file with relevant links to detailed documentation, primarily expected in the `.doc` directory within the repository.

Repositories are open for reading if the license permits.

Open repositories will be automatically replicated to GitHub for better availability, audit purposes, community development contributions, and as an off-site backup.

Public contributions will initially be manually transferred to GitLab and incorporated by the project maintainers. If public contributions become too frequent to maintain this approach, the process will be reassessed.

# Kubernetes Operators

Kubernetes operators extend the Kubernetes API to automate complex operations such as deployment, scaling, backup, and recovery. Operators are particularly useful for stateful applications and services requiring specific management logic.

## When to Use a Kubernetes Operator

Operators should be considered in the following cases:

- **Stateful applications** requiring state management (e.g., databases, message brokers, or distributed systems),
- **Complex deployment logic** exceeding Helm charts or basic Kubernetes manifests,
- **Automation of operations** such as backups, recovery, scaling, or upgrades.

## Operator Requirements

- **Operator SDK:** Operators should be developed using the **Operator Framework** or **Kubebuilder**.
- **CRD (Custom Resource Definitions):** The operator should define custom Kubernetes resources (CRD) describing application configuration and state.
- **Reconciler Loop:** The operator should implement a **reconciler loop** to monitor and adjust system state as needed.
- **Testing:** The operator should be thoroughly tested, including unit and integration tests in a real Kubernetes environment.

