# brute-force-detection-splunk
# Overview

This project demonstrates detection of brute-force login attempts by monitoring Windows Security Event Logs in a Splunk SIEM environment. Real-time alerts were configured to identify multiple failed login attempts, enabling rapid incident awareness.

# Tools & Technologies

Splunk SIEM
Windows Event Logs (Event ID 4625 / 4624)
PowerShell (attack simulation)
Virtual Lab Environment

# Detection Logic

Monitors failed login attempts (Event ID 4625)
Flags accounts with multiple failed authentications within 5 minutes
Real-time alerts trigger on 5+ failed attempts, helping SOC teams detect brute-force attacks quickly

# Implementation Highlights

Log Ingestion – Forwarded Windows Security logs to Splunk for centralized monitoring
Detection Query – index=windows_logs sourcetype=WinEventLog:Security EventCode=4625
Alert Configuration – Real-time alerts for potential brute-force activity
Attack Simulation – Validated detection with PowerShell-generated failed logins

# Key Outcomes

Centralized log monitoring implemented
Effective brute-force detection rules created
Real-time alerting for SOC readiness
Detection validated through simulated attacks
Potential Enhancements
Detect password spraying attacks
Correlate attacker IP addresses
Build Splunk dashboards for authentication trends
Automate incident response workflows

# Conclusion

Demonstrates the ability to configure SIEM-based detection workflows and monitor authentication activity in Windows environments, providing practical SOC-ready skills in security monitoring, incident detection, and alerting.
