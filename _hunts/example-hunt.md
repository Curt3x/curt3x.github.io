---
title: Hunting for suspicious PowerShell execution
date: 2026-10-05
tags: [Windows, PowerShell, T1059.001]
lab: Windows 10 endpoint with Sysmon, logs shipped to a SIEM in my home lab.
summary: Template report. Hypothesis, data sources, queries, findings and detections.
---
## Hypothesis
An attacker with a foothold would use encoded PowerShell commands to avoid simple detection.

## Data sources
Sysmon Event ID 1, PowerShell Script Block Logging (4104).

## Method
```text
process_name = "powershell.exe" AND command_line CONTAINS "-enc"
```
Explain the query and any filtering for false positives.

## Findings
What you found in the lab, with sanitized screenshots.

## MITRE ATT&CK mapping
| Technique | ID |
|---|---|
| Command and Scripting Interpreter: PowerShell | T1059.001 |

## Detection and recommendations
Detection rule idea and how you'd reduce noise.
