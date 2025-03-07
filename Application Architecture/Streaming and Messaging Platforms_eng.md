| Name | Streaming and Messaging Platforms |
|-|-|
| Approval date | 06.03.2025 |
| Category | Standard |


## Definition
The primary streaming and messaging platform for NASES is Apache Kafka. If specific messaging features are required and the cost of adaptation exceeds an acceptable budget, RabbitMQ may be considered as an alternative.

## Purpose
This standard defines the guidelines for data streaming and service-to-service messaging communication within NASES.

## Scope
This standard applies to all services managed by NASES.

## Rationale
- The technology stack should remain as lean as possible to ensure operational efficiency.
- Apache Kafka is the most robust open-source solution, widely recognized as the de facto standard for streaming and messaging, and is already in use at NASES.
- Designing applications around Kafka’s limitations is a common industry practice.
- If the cost of adapting an application to Kafka exceeds the acceptable budget, RabbitMQ can be considered as an alternative.

## Requirements
- All services managed by NASES must adhere to this standard.
- Preference is given to off-the-shelf products that are natively compatible with Apache Kafka.
- Custom software using alternative streaming platforms must be rejected or modified to comply with this standard unless an approved exemption is granted.

## Compliance
- Solutions should prioritize Apache Kafka integration where possible.
- Any deviation from this standard requires a justified business case and approval from the relevant authority.
- The use of alternative streaming platforms must be avoided unless explicitly approved.
