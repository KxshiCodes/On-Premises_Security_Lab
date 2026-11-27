# On-Premises Security Lab

A self-hosted security monitoring environment built to explore Active Directory, endpoint telemetry, SIEM integration, and network threat detection.

**Status:** Decommissioned

## Environment

| Component | Purpose |
|---|---|
| Windows Server | Active Directory, DNS, DHCP |
| Windows 11 | Domain-joined endpoint |
| Ubuntu 22.04 | Linux endpoint |
| Wazuh | SIEM and log management |
| Security Onion | Network monitoring and IDS |
| Kali Linux | Security testing |

## Implementation

- Built an isolated virtual network using VirtualBox.
- Deployed Active Directory, DNS, and DHCP.
- Joined Windows endpoints to the domain.
- Integrated Sysmon for endpoint telemetry.
- Forwarded endpoint events to Wazuh.
- Configured Security Onion for network monitoring.
- Simulated security activity and investigated generated alerts.

## Lab Environment

The environment consisted of multiple Windows and Linux virtual machines integrated with centralised security monitoring.

![Ubuntu Linux Environment](Ubuntu.PNG)

## Security Testing & Investigation

Used Kali Linux to conduct controlled internal security testing, covering:

- Network enumeration
- Credential attacks
- Privilege escalation
- Lateral movement
- Persistence techniques

Investigated generated activity using endpoint telemetry and network monitoring alerts.

## Troubleshooting

Maintaining the environment presented several infrastructure challenges:

- Elasticsearch memory consumption and resource constraints.
- DNS configuration issues affecting Active Directory authentication.
- VM clock drift causing Kerberos authentication failures.
- High CPU and RAM utilisation across virtual machines.
- Virtualisation compatibility issues during migration to Apple Silicon.

The lab was eventually decommissioned due to hardware resource limitations and the difficulty of maintaining the full environment reliably.

## Outcome

Built and integrated a multi-system security monitoring environment combining Active Directory, Windows and Linux endpoints, endpoint telemetry, SIEM monitoring, and network detection.

The project provided practical experience with infrastructure deployment, log integration, security investigation, and troubleshooting across a self-hosted environment.
