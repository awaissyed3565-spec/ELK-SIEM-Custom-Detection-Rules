 # ELK SIEM – Custom Detection Rules & Security Monitoring Dashboard

## Project Overview

This cybersecurity internship project focuses on implementing a Security Information and Event Management (SIEM) solution using Elasticsearch, Kibana, Winlogbeat, and Microsoft Sysmon.

The project demonstrates centralized Windows event collection, custom security detection rules, alert investigation, and security monitoring dashboards.

## Objectives

- Deploy Elasticsearch and Kibana using Docker Desktop.
- Collect Windows Security and Sysmon events using Winlogbeat.
- Create custom detection rules for authentication attacks, DNS tunneling indicators, and suspicious PowerShell activity.
- Investigate security alerts using Kibana.
- Develop a custom SOC monitoring dashboard.

## Tools and Technologies

| Technology | Purpose |
|---|---|
| Elasticsearch 8.13.0 | Log storage and analysis |
| Kibana 8.13.0 | Security monitoring and dashboards |
| Winlogbeat 8.13.0 | Windows Event Log collection |
| Microsoft Sysmon 15.22 | Endpoint activity monitoring |
| Docker Desktop | Container deployment |
| Windows 11 | Host operating system |
| PowerShell | Configuration and testing |

## Custom Detection Rules

### 1. Multiple Failed Login Attempts
- Monitors Windows Security Event ID 4625.
- Identifies repeated authentication failures.
- **Result:** Successfully generated a security alert during testing.

### 2. DNS Tunneling Detection
- Investigates potentially suspicious DNS activity.
- Uses DNS-related Windows event telemetry.
- **Result:** Rule configured; successful alert detection requires further verification.

### 3. PowerShell Exploitation Detection
- Investigates suspicious PowerShell execution indicators.
- Uses Windows PowerShell event logging.
- **Result:** Rule configured; successful alert detection requires further verification.

## Security Monitoring Dashboard

Six Kibana visualizations were created:

1. Failed Login Attempts Over Time
2. Top Targeted Usernames – Failed Login Attempts
3. Privileged Logon Events Over Time
4. Network Connections Over Time – Sysmon Event ID 3
5. Top 10 Destination Ports
6. Top 10 Destination IP Addresses

## Testing Results

| Test Scenario | Result |
|---|---|
| Multiple Failed Login Attempts | PASS |
| DNS Activity Monitoring | Partially verified |
| PowerShell Detection | Further validation required |
| Sysmon Network Connection Monitoring | PASS |

## Key Learning Outcomes

- SIEM deployment and configuration
- Windows security log analysis
- Custom detection rule development
- Endpoint monitoring using Sysmon
- Security alert investigation
- Kibana dashboard development
- SOC detection engineering and troubleshooting

## Project Documentation

The repository will include the final internship report, relevant screenshots, and sanitized configuration examples.

## Disclaimer

This project was performed in a controlled laboratory environment for educational and defensive cybersecurity purposes.
