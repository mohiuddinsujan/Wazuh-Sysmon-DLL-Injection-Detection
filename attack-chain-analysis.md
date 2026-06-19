# Attack Chain Analysis

## Initial Access

The attacker obtains execution capability on the target endpoint.

## Execution

InjectProc is executed to perform DLL Injection.

Command:

InjectProc.exe dll_inj hello-world-x64.dll cmd.exe

## Process Injection

The malicious DLL path is written into the target process memory.

A remote thread is created to force the target process to load the DLL.

## Defense Evasion

The injected code executes within a legitimate process (cmd.exe), making detection more difficult.

## Detection Sources

* Sysmon Event ID 1 (Process Creation)
* Sysmon Event ID 7 (Image Loaded)
* Sysmon Event ID 8 (CreateRemoteThread)
* Sysmon Event ID 10 (Process Access)

## MITRE ATT&CK Mapping

Technique:
T1055.001 - Dynamic-Link Library Injection

Tactic:
Defense Evasion
Privilege Escalation
