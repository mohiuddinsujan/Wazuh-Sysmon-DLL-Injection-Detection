# Detection Engineering

## Data Sources

### Sysmon

Microsoft Sysinternals Sysmon was deployed to collect endpoint telemetry.

### Wazuh Agent

The Wazuh agent was configured to collect Sysmon event logs.

Configuration:

<localfile>
    <location>Microsoft-Windows-Sysmon/Operational</location>
    <log_format>eventchannel</log_format>
</localfile>

## Detection Logic

The following behaviors were monitored:

* Process Creation
* DLL Loading
* Remote Thread Creation
* Process Access

## Investigation Steps

1. Review Sysmon Event ID 1
2. Review Sysmon Event ID 7
3. Review Sysmon Event ID 8
4. Review Sysmon Event ID 10
5. Correlate activity within Wazuh

## Alert Validation

Validate:

* Source Host
* Process Name
* Parent Process
* Command Line
* User Context
* Loaded DLL
