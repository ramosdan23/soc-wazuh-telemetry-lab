# Security Operations Virtual Lab (Wazuh & Splunk)

## Overview
A virtualized Security Operations Center (SOC) lab designed to ingest telemetry across multiple virtual endpoints, detect anomalous activity, and execute structured incident triage workflows.

## Environment Architecture
- **SIEM / Manager:** Wazuh Server / Splunk Free
- **Endpoints Monitored:**
  - Ubuntu Linux Server (Telemetry: `/var/log/auth.log`, `syslog`)
  - Windows 10/11 Enterprise (Telemetry: Sysmon, Windows Security Event Logs)
  - Kali Linux (Adversary simulation host)

## Use Cases & Simulations
1. **Unauthorized Access & Brute Force:** Simulating failed SSH and RDP authentication attempts (Windows Event ID 4625).
2. **Suspicious Process Execution:** Detecting encoded PowerShell commands and abnormal binary execution.
3. **Privilege Escalation:** Identifying unauthorized additions to local administrative groups.

## Incident Triage Reports
Structured markdown reports documenting detection queries, IoC extraction, and containment steps:
- [Report 001: SSH Brute-Force Triage](./reports/Report-001-SSH-BruteForce.md)
- [Report 002: Suspicious PowerShell Execution](./reports/Report-002-PowerShell.md)
- [Report 003: Unauthorized Privilege Escalation](./reports/Report-003-PrivilegeEscalation.md)
- [Report 004: Outbound C2 Beaconing](./reports/Report-004-C2-Beacon.md)
