# ELK SIEM Configuration Documentation

## Overview

This folder documents the configuration of the ELK SIEM environment used for centralized Windows security monitoring.

## 1. Elasticsearch

- Version: 8.13.0
- Deployment: Docker Desktop
- Port: 9200
- Purpose: Centralized security event storage and indexing

## 2. Kibana

- Version: 8.13.0
- Deployment: Docker Desktop
- Port: 5601
- Purpose: Security event investigation, custom detection rules, alert monitoring, and dashboard visualization

## 3. Winlogbeat

- Version: 8.13.0
- Operating System: Windows 11
- Purpose: Collect Windows Event Logs and forward them to Elasticsearch

Configured event channels included:

- Application
- System
- Security
- Windows PowerShell
- Microsoft-Windows-PowerShell/Operational
- Microsoft-Windows-Sysmon/Operational

## 4. Microsoft Sysmon

- Version: 15.22
- Purpose: Enhanced endpoint activity monitoring
- Network Connection Event ID: 3

Sysmon network connection events were successfully forwarded to Elasticsearch using Winlogbeat and investigated through Kibana Discover.

## 5. Security Considerations

Configuration examples published in this repository must not contain passwords, API keys, authentication tokens, or other sensitive information.

Any configuration files shared publicly should be reviewed and sanitized before uploading.
