# Public Health Data Center of Practice (PDCP) Innovation Sandbox Incident Management Policy

This policy defines the process for dealing with security incidents and events in the PDCP Innovation Sandbox. This document provides repeatable steps and guidelines for reporting, investigating, and managing security incidents and events.

## Definitions

**Compromise**: A breach of PDCP security. Includes, but is not limited to, unauthorized access to, disclosure, modification, use, interruption, removal, or destruction of sensitive information or assets, causing a loss of confidentiality, integrity, availability, or value. An event causing a loss of integrity or availability of PDCP services or activities.

**Security event**: Any event, act, omission, or situation that may be detrimental to PDCP security, including threats, vulnerabilities, and security incidents.

**Security incident**: Any event (or collection of events), act, omission, or situation that has resulted in a compromise. Every security incident is a security event (or collection of security events), but not every security event is a security incident.

**Threat**: Any potential event or act, deliberate or unintentional, or natural hazard that could result in a compromise.

**Vulnerability**: A factor that could increase susceptibility to compromise.

## Policy

The PDCP Innovation Sandbox Incident Management Policy is designed to encourage secure and responsible innovation while ensuring that the confidentiality, integrity, and availability of PDCP data and information are maintained. The PDCP acknowledges the importance of timely and effective response to security incidents and events.

To ensure appropriate management of security incidents and events, the following steps must be followed:

1. Report incident: If a security incident is suspected or detected, the incident must be reported to the PDCP Incident Management team as soon as possible.

2. Investigate incident: Once the incident is reported, the PDCP Incident Management team will appoint an incident investigation lead who will investigate the incident. The Pathfinder owner and leads will be notified that an incident event has occurred, and that the investigation process is about to begin. Pathfinders will be included in the process and information gathering/sharing.

3. Validate event information: The incident investigation lead will validate event information with Pathfinder subject matter experts and determine if the event is a false positive or a positive event.

4. False positive: If the event is a false positive, the Pathfinder owner will be given advice on how to remediate the issue. Any auto-remediation actions that may have been triggered will be removed. If the issue is not properly remediated or acted on, please refer to the Incident Abuse section.

5. Positive event: If the event is a positive event, the PDCP Incident Management team will be contacted, and the GC-CSEMP process will be followed.

6. Document and publish: All incidents will be documented and published in the PDCP incident management system.

## Auto Remediations

Runbooks need to be developed for the following auto-remediations:

- Removal of Pathfinder owner and contributor groups from the cloud subscription
- Disconnect from the internet
- Remove IP
- Implement NSG/firewalls

## Incident Abuse

The PDCP Innovation Sandbox is designed to encourage secure innovation. In the event that the security incident was caused by intentional or reckless behavior, the following three-strike system will be implemented:

- Warning
- Escalated Warning
- Removal of subscription and resources

The PDCP acknowledges that the Innovation Sandbox is a work in progress and is committed to continuously improving this policy to align with best practices and changing business needs.

If you have any questions or concerns about the PDCP Innovation Sandbox Incident Management Policy, please contact the PDCP
