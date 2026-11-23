
# On-Premises Security Lab

A self-hosted security monitoring lab built to explore Active Directory, endpoint telemetry, SIEM integration, and network threat detection.

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

- Configured an isolated virtual network using VirtualBox.
- Deployed Active Directory, DNS, and DHCP.
- Joined Windows endpoints to the domain.
- Integrated Sysmon for endpoint telemetry.
- Forwarded endpoint logs to Wazuh.
- Used Security Onion for network monitoring.
- Simulated security events and investigated alerts.

## Lab Environment

The lab ran across multiple virtual machines, combining Windows and Linux endpoints with centralised security monitoring.

![Ubuntu Linux Environment](Ubuntu.PNG)

## Attack Simulation

Used Kali Linux to simulate internal security activity, including:

- Network enumeration
- Credential attacks
- Privilege escalation
- Lateral movement
- Persistence techniques

Investigated attacker activity through endpoint telemetry and network monitoring alerts.

## Troubleshooting

The lab encountered several stability and resource issues:

- Elasticsearch consuming excessive memory.
- DNS misconfiguration affecting Active Directory authentication.
- VM clock drift causing Kerberos authentication failures.
- High CPU and RAM usage across virtual machines.
- Virtualisation compatibility issues during migration to Apple Silicon.

The environment was eventually decommissioned because the combined resource requirements made it impractical to maintain reliably on local hardware.

## Key Takeaways

- Active Directory relies on reliable DNS and time synchronisation.
- SIEM platforms require careful resource planning.
- Endpoint and network telemetry provide complementary visibility.
- Distributed infrastructure requires systematic troubleshooting.
- Smaller, modular deployments are easier to maintain and scale.
