# Verbose error messages

Severity: Low  
CVSS: 3.6, https://nvd.nist.gov/vuln-metrics/cvss/v3-calculator?vector=AV:N/AC:L/PR:L/UI:N/S:U/C:L/I:N/A:N/CR:L/IR:X/AR:X/MAV:X/MAC:X/MPR:X/MUI:X/MS:X/MC:X/MI:X/MA:X&version=3.1

## Affected Assets

CHANGE ME!

## Description

The web server responds with verbose error messages. Information on the web server or framework versions is also present within the web server's responses.

Improper handling of errors can introduce a variety of security problems for a web site. The most common problem is when detailed internal error messages such as stack traces, database dumps, and error codes are displayed to the user or attacker. These messages reveal implementation details that should never be revealed. Such details can provide attackers important clues on potential flaws in the site and such messages are also disturbing to normal users.

## Supporting Evidence

CHANGE ME!

## Recommendation

It is recommended not to display verbose error messages or detailed technical information to users. Configure the web server to stop displaying verbose messages.

## Reference

* OWASP Testing Guide (WSTG-ERRH-01), https://owasp.org/www-project-web-security-testing-guide/stable/4-Web_Application_Security_Testing/08-Testing_for_Error_Handling/01-Testing_For_Improper_Error_Handling 
