# Remediation Roadmap

## Preventive Controls

* Application Whitelisting
* Windows Defender Application Control
* Endpoint Protection Platform
* Attack Surface Reduction Rules

## Detective Controls

* Sysmon Monitoring
* Wazuh Alerting
* EDR Monitoring
* SIEM Correlation Rules

## Response Actions

* Isolate Host
* Terminate Malicious Process
* Remove Malicious DLL
* Collect Memory Dump
* Perform Root Cause Analysis

## Lessons Learned

DLL Injection is a common malware technique used to evade detection by executing malicious code inside trusted processes.

Continuous monitoring with Sysmon and Wazuh provides visibility into this activity and improves incident detection capabilities.
