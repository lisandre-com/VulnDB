# DLL Hijacking

Severity: Varies  
CVSS: N/A

## Affected Assets

CHANGE ME!

## Description

**DLL Search Order Hijacking** exploits the way Windows resolves DLLs when the application does not explicitly set the full path. Application XYZ is vulnerable to this attack. XYZ's application folder (C:\Program Files\XYZ) comes before C:\Windows\System32 in the DLL file search order. Placing a malicious DLL file in XYZ's application folder therefore results in the execution of the malicious DLL file.

**Relative Path DLL Hijacking** is a variation of the Search Order DLL Hijacking technique. The attacker writes (and typically renames) a legitimate executable file - alongside their malicious DLL - to a folder they have permissions to write to. This technique requires a legitimate executable that does not specify an absolute path for DLL files. If an absolute path is not specified, Windows will search for the DLL file following the predefined search order. 
Application XYZ is vulnerable to this attack. Copying the executable file to another folder and placing a malicious DLL file there results in the malicious DLL file being executed.

## Supporting Evidence

CHANGE ME!

## Recommendation

* Developers should require set paths for DLLs in applications.
* When possible, include hash values in manifest files to help prevent side-loading of malicious libraries.
* Disallow loading of remote DLLs. This is included by default in Windows Server 2012+ and is available by patch for XP+ and Server 2003+.
* Enable Safe DLL Search Mode to move the user's current folder later in the search order. This is included by default in modern versions of Windows; the associated Windows Registry key is located at HKLM\SYSTEM\CurrentControlSet\Control\Session Manager\SafeDLLSearchMode.
* Update software regularly to include patches that fix DLL side-loading vulnerabilities.

## Reference

* Hijack Execution Flow: DLL (T1574.001), https://attack.mitre.org/techniques/T1574/001/
