# All Rules by ATT&CK Tactic & Technique
| initial-access | execution | persistence | privilege-escalation | defense-evasion | credential-access | discovery | lateral-movement | collection | exfiltration | command-and-control |
|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
| Drive-by Compromise  | AppleScript | .bash_profile and .bashrc | Access Token Manipulation | Access Token Manipulation | Account Manipulation | Account Discovery | AppleScript | Audio Capture | Automated Exfiltration  | Commonly Used Port  |
| Exploit Public-Facing Application  | CMSTP | Accessibility Features | Accessibility Features | BITS Jobs | Bash History | Application Window Discovery | Application Deployment Software  | Automated Collection | Data Compressed | Communication Through Removable Media  |
| Hardware Additions  | Command-Line Interface | Account Manipulation | AppCert DLLs  | Binary Padding | Brute Force | Browser Bookmark Discovery | Distributed Component Object Model  | Clipboard Data | Data Encrypted | Connection Proxy |
| Replication Through Removable Media  | Compiled HTML File | AppCert DLLs  | AppInit DLLs | Bypass User Account Control | Credential Dumping | File and Directory Discovery | Exploitation of Remote Services  | Data Staged | Data Transfer Size Limits | Custom Command and Control Protocol  |
| Spearphishing Attachment | Control Panel Items  | AppInit DLLs | Application Shimming | CMSTP | Credentials in Files | Network Service Scanning | Logon Scripts | Data from Information Repositories  | Exfiltration Over Alternative Protocol | Custom Cryptographic Protocol  |
| Spearphishing Link  | Dynamic Data Exchange | Application Shimming | Bypass User Account Control | Clear Command History | Credentials in Registry | Network Share Discovery | Pass the Hash | Data from Local System | Exfiltration Over Command and Control Channel  | Data Encoding |
| Spearphishing via Service  | Execution through API  | Authentication Package  | DLL Search Order Hijacking  | Code Signing  | Exploitation for Credential Access  | Network Sniffing | Pass the Ticket  | Data from Network Shared Drive  | Exfiltration Over Other Network Medium  | Data Obfuscation  |
| Supply Chain Compromise  | Execution through Module Load  | BITS Jobs | Dylib Hijacking  | Compiled HTML File | Forced Authentication  | Password Policy Discovery | Remote Desktop Protocol | Data from Removable Media  | Exfiltration Over Physical Medium  | Domain Fronting  |
| Trusted Relationship  | Exploitation for Client Execution  | Bootkit  | Exploitation for Privilege Escalation  | Component Firmware  | Hooking | Peripheral Device Discovery  | Remote File Copy | Email Collection | Scheduled Transfer  | Fallback Channels  |
| Valid Accounts  | Graphical User Interface  | Browser Extensions | Extra Window Memory Injection  | Component Object Model Hijacking | Input Capture | Permission Groups Discovery | Remote Services  | Input Capture |  | Multi-Stage Channels  |
|  | InstallUtil | Change Default File Association | File System Permissions Weakness  | Control Panel Items  | Input Prompt | Process Discovery | Replication Through Removable Media  | Man in the Browser  |  | Multi-hop Proxy  |
|  | LSASS Driver  | Component Firmware  | Hooking | DCShadow | Kerberoasting  | Query Registry | SSH Hijacking  | Screen Capture |  | Multiband Communication  |
|  | Launchctl | Component Object Model Hijacking | Image File Execution Options Injection | DLL Search Order Hijacking  | Keychain | Remote System Discovery | Shared Webroot  | Video Capture  |  | Multilayer Encryption  |
|  | Local Job Scheduling | Create Account | Launch Daemon | DLL Side-Loading  | LLMNR/NBT-NS Poisoning  | Security Software Discovery | Taint Shared Content  |  |  | Port Knocking  |
|  | Mshta | DLL Search Order Hijacking  | New Service | Deobfuscate/Decode Files or Information | Network Sniffing | System Information Discovery | Third-party Software  |  |  | Remote Access Tools  |
|  | [**PowerShell**](./T1086/T1086.md) | Dylib Hijacking  | Path Interception  | Disabling Security Tools | Password Filter DLL | System Network Configuration Discovery | Windows Admin Shares |  |  | Remote File Copy |
|  | Regsvcs/Regasm | External Remote Services  | Plist Modification | Exploitation for Defense Evasion  | Private Keys | System Network Connections Discovery | Windows Remote Management |  |  | Standard Application Layer Protocol |
|  | Regsvr32 | File System Permissions Weakness  | Port Monitors  | Extra Window Memory Injection  | Securityd Memory  | System Owner/User Discovery |  |  |  | Standard Cryptographic Protocol  |
|  | Rundll32 | Hidden Files and Directories | Process Injection | File Deletion | Two-Factor Authentication Interception  | System Service Discovery |  |  |  | Standard Non-Application Layer Protocol  |
|  | Scheduled Task | Hooking | SID-History Injection  | File Permissions Modification |  | System Time Discovery |  |  |  | Uncommonly Used Port |
|  | Scripting | Hypervisor | Scheduled Task | File System Logical Offsets  |  |  |  |  |  | Web Service  |
|  | Service Execution | Image File Execution Options Injection | Service Registry Permissions Weakness  | Gatekeeper Bypass |  |  |  |  |  |  |
|  | Signed Binary Proxy Execution | Kernel Modules and Extensions  | Setuid and Setgid | HISTCONTROL |  |  |  |  |  |  |
|  | Signed Script Proxy Execution | LC_LOAD_DYLIB Addition  | Startup Items | Hidden Files and Directories |  |  |  |  |  |  |
|  | Source | LSASS Driver  | Sudo | Hidden Users |  |  |  |  |  |  |
|  | Space after Filename | Launch Agent | Sudo Caching | Hidden Window  |  |  |  |  |  |  |
|  | Third-party Software  | Launch Daemon | Valid Accounts  | Image File Execution Options Injection |  |  |  |  |  |  |
|  | Trap | Launchctl | Web Shell | Indicator Blocking  |  |  |  |  |  |  |
|  | Trusted Developer Utilities | Local Job Scheduling |  | Indicator Removal from Tools  |  |  |  |  |  |  |
|  | User Execution  | Login Item  |  | Indicator Removal on Host |  |  |  |  |  |  |
|  | Windows Management Instrumentation | Logon Scripts |  | Indirect Command Execution |  |  |  |  |  |  |
|  | Windows Remote Management | Modify Existing Service |  | Install Root Certificate |  |  |  |  |  |  |
|  | XSL Script Processing | Netsh Helper DLL |  | InstallUtil |  |  |  |  |  |  |
|  |  | New Service |  | LC_MAIN Hijacking  |  |  |  |  |  |  |
|  |  | Office Application Startup |  | Launchctl |  |  |  |  |  |  |
|  |  | Path Interception  |  | Masquerading |  |  |  |  |  |  |
|  |  | Plist Modification |  | Modify Registry |  |  |  |  |  |  |
|  |  | Port Knocking  |  | Mshta |  |  |  |  |  |  |
|  |  | Port Monitors  |  | NTFS File Attributes |  |  |  |  |  |  |
|  |  | Rc.common |  | Network Share Connection Removal |  |  |  |  |  |  |
|  |  | Re-opened Applications |  | Obfuscated Files or Information |  |  |  |  |  |  |
|  |  | Redundant Access  |  | Plist Modification |  |  |  |  |  |  |
|  |  | Registry Run Keys / Startup Folder |  | Port Knocking  |  |  |  |  |  |  |
|  |  | SIP and Trust Provider Hijacking  |  | Process Doppelgänging  |  |  |  |  |  |  |
|  |  | Scheduled Task |  | Process Hollowing  |  |  |  |  |  |  |
|  |  | Screensaver |  | Process Injection |  |  |  |  |  |  |
|  |  | Security Support Provider |  | Redundant Access  |  |  |  |  |  |  |
|  |  | Service Registry Permissions Weakness  |  | Regsvcs/Regasm |  |  |  |  |  |  |
|  |  | Setuid and Setgid |  | Regsvr32 |  |  |  |  |  |  |
|  |  | Shortcut Modification  |  | Rootkit |  |  |  |  |  |  |
|  |  | Startup Items |  | Rundll32 |  |  |  |  |  |  |
|  |  | System Firmware  |  | SIP and Trust Provider Hijacking  |  |  |  |  |  |  |
|  |  | Time Providers  |  | Scripting |  |  |  |  |  |  |
|  |  | Trap |  | Signed Binary Proxy Execution |  |  |  |  |  |  |
|  |  | Valid Accounts  |  | Signed Script Proxy Execution |  |  |  |  |  |  |
|  |  | Web Shell |  | Software Packing  |  |  |  |  |  |  |
|  |  | Windows Management Instrumentation Event Subscription |  | Space after Filename |  |  |  |  |  |  |
|  |  | Winlogon Helper DLL |  | Template Injection  |  |  |  |  |  |  |
|  |  |  |  | Timestomp |  |  |  |  |  |  |
|  |  |  |  | Trusted Developer Utilities |  |  |  |  |  |  |
|  |  |  |  | Valid Accounts  |  |  |  |  |  |  |
|  |  |  |  | Web Service  |  |  |  |  |  |  |
|  |  |  |  | XSL Script Processing |  |  |  |  |  |  |
