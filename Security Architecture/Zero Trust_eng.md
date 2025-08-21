| Name | Zero Trust |
|-|-|
| Approval date | 07.08.2025 |
| Category | Principle |

## Statement
Zero Trust is a security model where no user, device, or system is inherently trusted, regardless of network location.  
All access is continuously authenticated, authorized, and encrypted based on identity, context, and risk.  

## Rationale
Modern eGovernment environments involve complex infrastructure including cloud services, third-party integrations, and remote access, which make traditional perimeter-based security insufficient.  
The Zero Trust model addresses these challenges by enforcing strict identity verification, minimizing trust zones, and ensuring that access is granted only after continuous validation.  

This approach supports legislative obligations under:  
- [Act no. 95/2019 Coll – IT measures in public administration](https://www.slov-lex.sk/ezbierky/pravne-predpisy/SK/ZZ/2019/95/)  
- [Act no. 69/2018 Coll – security measures](https://www.slov-lex.sk/ezbierky/pravne-predpisy/SK/ZZ/2018/69/)  
- [Directive (EU) 2022/2555 (NIS2) – reinforced network and information system security](https://eur-lex.europa.eu/eli/dir/2022/2555/oj?locale=sk)  

## Implications
- Replacing implicit trust within internal networks with continuous identity and device validation  
- Applying least privilege access, RABAC, multi-factor authentication, and micro-segmentation  
- Encrypting all communication and monitoring user and system behavior in real time  
- Adjusting legacy systems and architectures to support Zero Trust principles  
- Aligning all digital public services with a security-by-design and security-by-default mindset  

## Requirements
- Access control is enforced based on identity, role, device posture, and behavioral patterns  
- MFA (multi-factor authentication) is mandatory for all administrative, privileged, and remote access  
- Regular reviews and audits of access rights, system logs, and anomaly detection must be performed  
- Security policies must reflect Zero Trust principles across architecture, operations, and governance  
