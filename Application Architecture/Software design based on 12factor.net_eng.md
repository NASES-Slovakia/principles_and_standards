| Name | Software design based on 12factor.net |
|-|-|
| Approval date | 15.01.2025 |
| Category | Principle |

# Definition

All services designed by NASES or for NASES should be designed according to / in compliance with the 12 Factor Apps manifesto.

# Purpose

To ensure high-quality and maintainable app design.

# Scope

This standard applies to all custom-made software owned by the organization.

Off-the-shelf products that violate the 12 Factor App design should be avoided.

# Rationale

The 12 Factor manifesto is a well-known set of industry best practices in software development and design.

It is a platform and technology-agnostic methodology applicable to most of the software projects within NASES.

# Requirements

Project detailed technical specification should include an explanation of how each factor is addressed.

# Compliance

- All project requirements should include a reference to the 12 Factor manifesto.
- Project specifications missing information on how the 12 factors are addressed or directly proposing designs breaking the 12 Factor manifesto should be rejected.

# The 12 Factors

## I. Codebase

One codebase tracked in revision control, many deploys.

## II. Dependencies

Explicitly declare and isolate dependencies.

## III. Config

Store config in the environment.

## IV. Backing services

Treat backing services as attached resources.

## V. Build, release, run

Strictly separate build and run stages.

## VI. Processes

Execute the app as one or more stateless processes.

## VII. Port binding

Export services via port binding.

## VIII. Concurrency

Scale out via the process model.

## IX. Disposability

Maximize robustness with fast startup and graceful shutdown.

## X. Dev/prod parity

Keep development, staging, and production as similar as possible.

## XI. Logs

Treat logs as event streams.

## XII. Admin processes

Run admin/management tasks as one-off processes.
