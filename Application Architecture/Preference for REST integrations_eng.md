| Name | Preference for REST integrations |
|-|-|
| Approval date | 17.07.2024 |
| Category | Principle |

# Statement

RESTful web services shall be preferred over SOAP-based integrations for all new system interfaces, and existing SOAP integrations shall be gradually replaced with RESTful services.

# Rationale

RESTful web services offer a more flexible, scalable, and efficient approach to system integration compared to SOAP. REST uses standard HTTP methods and supports various data formats, making it easier to use and more widely adopted. Replacing legacy SOAP integrations with REST will enhance interoperability, reduce complexity, and improve performance.

# Implications

## Design and Development

- All new integrations should be designed and developed using RESTful APIs.
- Development teams must be proficient in RESTful API design principles and best practices.

## Existing Systems

- A strategic plan must be developed to gradually replace existing SOAP-based integrations with RESTful services.
- Transition plans should include thorough testing and validation to ensure functional parity and data integrity.

## Interoperability

- RESTful services must be designed to support diverse client applications and platforms.
- Standardization of REST API documentation using tools like Swagger/OpenAPI is required to ensure consistency and ease of use.

## Security

- RESTful services must adhere to security best practices, including OAuth for authentication, and HTTPS for secure communication.
- Existing SOAP integrations should maintain current security standards until they are replaced.

## Performance and Scalability

- RESTful services should be optimized for performance and scalability to handle increasing loads and to deliver a responsive user experience.
- Monitoring and performance metrics should be established to track the efficiency of both RESTful and existing SOAP integrations during the transition period.

## Governance

- Establish governance policies to enforce the preference for RESTful integrations and to manage the gradual phase-out of SOAP.
- Regular reviews and audits should be conducted to ensure compliance with the principle and to monitor the progress of legacy system replacement.
