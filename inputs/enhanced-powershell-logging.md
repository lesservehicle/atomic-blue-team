# Enhanced PowerShell Logging

Configuring enhanced PowerShell Logging requires:
- Ensuring you have the correct PowerShell version
- Enabling Module Logging
- Enabling Script Block Logging
- Enabling Transcription Logging
- Enabling Command Line Process Auditing
- Ensuring that Advanced Audit Policy settings are not overwritten


## Events
- Event ID 4103
- Event ID 4104
- [Event ID 4688\(S\): A new process has been created.](../../events/4688S/4688S.md) 
- Event ID 7045

## Output Files
Microsoft-Windows-PowerShell/Operational

## Compatible PowerShell Versions

### Windows 10

Windows 10 does not require any software updates to support enhanced PowerShell logging.

### Windows 7/8.1/2008/2012

#### Powershell 4.0
Powershell version 4.0 requires the following to enable enhanced logging for Windows 7/8.1/2008/2012:
- .NET 4.5
- Windows Management Framework (WMF) 4.0
- The appropriate WMF 4.0 update:
    - 8.1/2012 R2 – KB3000850
    - 2012 – KB3119938
    - 7/2008 R2 SP1 – KB3109118

#### Powershell 5.0
Powershell version 5.0 requires the following to enable enhanced logging for Windows 7/8.1/2008/2012:
- .NET 4.5
- Windows Management Framework (WMF) 4.0 (Windows 7/2008 only)
- Windows Management Framework (WMF) 5.0


## Module Logging

To enable module logging:

1. In the Windows PowerShell GPO settings, set **Turn on Module Logging** to enabled.
	 - Administrative Templates → Windows Components → Windows PowerShell → Turn on Module Logging
2. In the **Options** pane, click the button to show **Module Name**.
3. In the **Module Names** window, enter * to record all modules.
4. Click OK in the **Module Names** window.
5. Click OK in the **Module Logging** window.

Alternately you can set the following registry values:

```
HKLM\SOFTWARE\Wow6432Node\Policies\Microsoft\Windows\PowerShell\ModuleLogging → EnableModuleLogging = 1
HKLM\SOFTWARE\Wow6432Node\Policies\Microsoft\Windows\PowerShell\ModuleLogging\ModuleNames → * = *
```

## Script Block Logging

To enable script block logging, go to the Windows PowerShell GPO settings and set Turn on **PowerShell Script Block Logging** to enabled.

Alternately, you can set the following registry value:

```
HKLM\SOFTWARE\Wow6432Node\Policies\Microsoft\Windows\PowerShell\ScriptBlockLogging → EnableScriptBlockLogging = 1
```

## Command Line Process Auditing

*Only Windows 10 and Server 2012 R2/2016 include the Creator Process Name, which can be useful for detection of which process spawned the script, eg. if a malicious Word document is running a script.*

If you enable this policy setting the command line information for every process will be logged in plain text in the security event log as part of the Audit Process Creation event 4688, "a new process has been created," on the workstations and servers on which this policy setting is applied.

### Enable command line process auditing:

Enable the Audit Process Creation audit policy so 4688 events are generated. In Group Policy:
	- Computer Configuration → Windows Settings → Security Settings → Advanced Audit Policy Configuration → System Audit Policies → Detailed Tracking

### Enable command line in process creation:

Enable the **Include command line in process creation events** policy setting in group policy: 
	`Computer Configuration → Administrative Templates → System → Audit Process Creation`


Alternatively, set the following registry value:
	`HKLM\Software\Microsoft\Windows\CurrentVersion\Policies\System\Audit\ProcessCreationIncludeCmdLine → Enabled = 1`

## Ensure that Advanced Audit Policy Configuration settings are not overwritten

When you use Advanced Audit Policy Configuration settings, you need to confirm that these settings are not overwritten by basic audit policy settings. Event 4719 is logged when the settings are overwritten.

To ensure that Advanced Audit Policy Configuration settings are not overwritten

- Open the Group Policy Management console
- Right-click Default Domain Policy, and then click Edit.
- Double-click Computer Configuration, double-click Policies, and then double-click Windows Settings.
- Double-click Security Settings, double-click Local Policies, and then click Security Options.
- Double-click Audit: Force audit policy subcategory settings (Windows Vista or later) to override audit policy category settings, and then click Define this policy setting.
- Click Enabled, and then click OK.

## References

- Black Hills Information Security: https://www.blackhillsinfosec.com/powershell-logging-blue-team/
- FireEye: https://www.fireeye.com/blog/threat-research/2016/02/greater_visibilityt.html
- Splunk: https://docs.splunk.com/Documentation/UBA/4.3.2/GetDataIn/AddPowerShell
- Command Line Process Auditing: https://docs.microsoft.com/en-us/windows-server/identity/ad-ds/manage/component-updates/command-line-process-auditing
- Command Line Auditing: https://support.microsoft.com/en-us/help/3004375/microsoft-security-advisory-update-to-improve-windows-command-line-aud
- Audit Process Creation: https://docs.microsoft.com/en-us/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/dn319093(v=ws.11)
- Advanced Security Audit Policy Settings: https://docs.microsoft.com/en-us/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/dn319056%28v%3dws.11%29