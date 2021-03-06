# Event ID 4985: The state of a transaction has changed

## Description
This is an informational event from file system Transaction Manager.

## Data Dictionary
|Standard Name|Field Name|Type|Description|Sample Value|
|---|---|---|---|---|
|user_sid|SubjectUserSid|SID|SID of account through which the state of the transaction was changed.|`S-1-5-18`|
|user_name|SubjectUserName|UnicodeString|the name of the account that changed the state of the transaction.|`DC01$`|
|user_domain|SubjectDomainName|UnicodeString|domain or computer name.|`CONTOSO`|
|user_logon_id|SubjectLogonId|HexInt64|hexadecimal value that can help you correlate this event with recent events that might contain the same Logon ID|`0x3e7`|
|transaction_guid|TransactionId|GUID|unique GUID of the transaction. This field can help you correlate this event with other events that might contain the same Transaction ID, such as "4656(S, F): A handle to an object was requested."|`{17EF5E21-5E2C-11E5-810F-00155D987005}`|
|transaction_new_state|NewState|UInt32|identifier of the new state of the transaction.|`52`|
|transaction_resource_manager|ResourceManager|GUID|unique GUID-Identifier of the Resource Manager which associated with this transaction.|`{5F5ED427-FCCA-11E3-BD73-B54AB417B853}`|
|process_id|ProcessId|Pointer|hexadecimal Process ID of the process through which the state of the transaction was changed. Process ID (PID) is a number used by the operating system to uniquely identify an active process|`0x370`|
|process_path|ProcessName|UnicodeString|full path and the name of the executable for the process.|`C:\Windows\System32\svchost.exe`|

## References
* [MS Source](https://github.com/MicrosoftDocs/windows-itpro-docs/blob/master/windows/security/threat-protection/auditing/event-4964.md)
* [MS Security Auditing Category - Object Access](https://docs.microsoft.com/en-us/windows/security/threat-protection/auditing/advanced-security-audit-policy-settings#object-access)
* [MS Security Auditing Category - Privilege Use](https://docs.microsoft.com/en-us/windows/security/threat-protection/auditing/advanced-security-audit-policy-settings#privilege-use)
* [MS Security Auditing Sub-category - Audit File System](https://github.com/MicrosoftDocs/windows-itpro-docs/tree/master/windows/security/threat-protection/auditing/audit-file-system.md)
* [MS Security Auditing Sub-category - Audit Non Sensitive Privilege Use](https://github.com/MicrosoftDocs/windows-itpro-docs/tree/master/windows/security/threat-protection/auditing/audit-non-sensitive-privilege-use.md)
* [MS Security Auditing Sub-category - Audit Other Privilege Use Events](https://github.com/MicrosoftDocs/windows-itpro-docs/tree/master/windows/security/threat-protection/auditing/audit-other-privilege-use-events.md)
* [MS Security Auditing Sub-category - Audit Sensitive Privilege Use](https://github.com/MicrosoftDocs/windows-itpro-docs/tree/master/windows/security/threat-protection/auditing/audit-sensitive-privilege-use.md)

## Tags
* etw_level_Informational
* etw_task_task_0
* Object Access
* Privilege Use
* Audit File System
* Audit Non Sensitive Privilege Use
* Audit Other Privilege Use Events
* Audit Sensitive Privilege Use