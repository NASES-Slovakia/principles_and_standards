| Name | Security by Design |
|-|-|
| Approval date | 03.10.2024 |
| Category | Principle |

# Statement

Security must be embedded throughout the lifecycle of system design, development, and operation, rather than relying on obscurity as a means of protecting systems. Every architectural component must be designed with the highest level of security as a core priority, with an emphasis on adopting a "shift left" strategy to address security concerns early in the development process.

# Rationale

Building security into the architecture from the outset ("Security by Design") ensures a robust and resilient infrastructure. Relying on secrecy, undocumented features, or hidden details to provide security ("Security by Obscurity") is insufficient, as these elements may be easily discovered by attackers. By following a proactive security-by-design approach and shifting security measures to the earliest stages of the development process ("shift left"), the enterprise can mitigate vulnerabilities before they become risks, minimize the attack surface, and ensure compliance with regulations and best practices. This principle reduces the likelihood of critical security flaws and enhances the organization’s overall cybersecurity posture.

# Implications

## Early Security Integration (Shift Left)

- Security requirements must be identified and addressed at the earliest stages of solution development and architecture planning.
- The "shift left" approach, as recommended by CNCF, ensures that security is considered during requirements gathering, design, and even during initial development phases, rather than waiting until testing or deployment.

## Transparent Security Controls

- Security mechanisms and controls must be transparent and testable, relying on robust security methods instead of secrecy.
- Security controls such as encryption, access control, and auditing should be well-documented and implemented following industry standards.

## Defense in Depth

- A layered approach to security must be applied, ensuring that multiple safeguards exist to protect sensitive data and systems.
- No single security control should be considered sufficient, and redundancy is key to mitigating risk.

## Consistent Security Standards

- Common security standards and frameworks, such as CIS, ISO 27001, and OWASP, should be applied consistently across all systems.
- This reduces the likelihood of errors and ensures a consistent approach to mitigating risks.

## Security Testing and Validation

- Regular security reviews, including code reviews, vulnerability assessments, and penetration testing, must be carried out to verify the effectiveness of security controls.
- Emphasizing "shift left" also means conducting automated security testing as early as possible, integrating security into CI/CD pipelines.
